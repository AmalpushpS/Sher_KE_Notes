,Kerberoasting is another popular attack pertinent to a Windows Domain Environment. Unlike ASREPRoasting, it is a post-authentication attack that requires access to a Domain User's account. It allows attackers to extract service account hashes and crack them to gain privileged access.
### SPN

Every service in a Domain Environment is associated with a service account. SPN Stands for Service Principal Name. A SPN is a unique identifier that maps a service to a Domain Account. Basically it tells kerberos : "which user owns which service"

##### Do All Service Accounts have SPNs associated with them?

No, Not all service accounts have SPNs associated with them. A service account is granted an SPN only if:

1. It uses kerberos for authentication
2. It is a custom service account and not a builtin one (like LocalSystem, NetworkService etc)

### TGS

- A Service Ticket is a kerberos authentication token that allows a user to access a specific service within the domain (such as SMB, HTTP)
- A Service Ticket is issued by the TGS (Ticket Granting Service) which is a part of the KDC.

#### Requesting for a service ticket

- Any user with a Valid TGT can request a Service Ticket for a given SPN.
- The request contains :
    - SPN of the service that the user wishes to access
    - Their TGT
- If the request is valid, the TGS issues a service ticket which is encrypted with the NTLM hash of the service account associated with the provided SPN.
- The service ticket can only be decrypted by the service account whose password hash was used to encrypt it

### What is a TGT?

- A TGT (Ticket Granting Ticket) is a kerberos authentication token that allows a user to prove their identity to the domain, without needing to enter their password everytime.
- A TGT is issued by the KDC after successful auth to the KDC.
- It allows users to request for Service tickets to access services.
- Just like cookies of a website.