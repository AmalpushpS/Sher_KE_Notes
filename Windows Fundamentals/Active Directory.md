
- A **Windows Domain** is a network setup where all users and computers are managed **centrally** using **Active Directory (AD)**.
    
- The server that controls this setup is called a **Domain Controller (DC)**.

*Active Directory Domain Services (AD DS)*

- Stores **all network objects** (users, computers, printers, etc.).
    
- Acts as a **central directory** for the domain.
###### Users

- Represent **people** (employees) or **services** (like SQL Server).
    
- Service users have **limited access** – only what the service needs.
    

---

##### Machines

- Every computer that joins the domain gets a **machine account**.
    
- Machine accounts = computer name + `$` (e.g., `DC01$`).
    
- Passwords auto-generated & rotated (very complex).
    
- Computers can’t be accessed directly by users (normally).
    

---

### 🔐 **Security Groups**

- Used to **grant permissions** to files, printers, etc.
    
- Easier management: add users to groups instead of assigning individually.
    
- Groups can include **users**, **machines**, or even other groups.
    

#### 🔸 **Important Default Groups:**

|Group Name|Purpose|
|---|---|
|**Domain Admins**|Full control over the domain.|
|**Server Operators**|Manage Domain Controllers (limited).|
|**Backup Operators**|Access any file (for backups).|
|**Account Operators**|Can create/edit user accounts.|
|**Domain Users**|All user accounts.|
|**Domain Computers**|All joined computers.|
|**Domain Controllers**|All Domain Controller servers.|