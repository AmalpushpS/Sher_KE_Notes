
**NTFS (New Technology File System):**  
NTFS is the default file system for modern Windows OS. It offers features like security, encryption, disk limits, and detailed file info. It also works with Cluster Shared Volumes **(CSV)**, so multiple systems in a network can access the same storage, ensuring data is always available and safe.

NTFS includes a feature called [self-healing NTFS], which automatically detects and repairs minor file system corruption in the background, without requiring the volume to be taken offline. This proactive approach helps maintain data integrity and minimizes disruptions to users and applications.

**Granular Access Control (ACLs):**  
NTFS lets you set specific permissions for files and folders. You can choose who can read, write, or modify them, giving you detailed control over access.

**BitLocker Integration:**  
NTFS works with BitLocker to protect data using encryption. Even if someone removes the drive, they can’t access the data without permission, thanks to trusted platform module (TPM) security.

Before NTFS, there was  **FAT16/FAT32** (File Allocation Table) and **HPFS** (High Performance File System).
 
**Alternate Data Streams (ADS):**  
ADS is a feature in NTFS that lets a file store extra hidden data. File Explorer doesn’t show these streams, but you can view them using PowerShell or special tools.

While hackers can use **ADS** to hide malware.