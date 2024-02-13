**On NFS Server:**

**Update Package Repositories:**
This command updates the package repositories on your Ubuntu system to ensure you have the latest package information.

```bash
sudo apt update
```
**Install NFS Server Package:**

This command installs the NFS server package (nfs-kernel-server) on your Ubuntu system, which allows your system to act as an NFS server and share directories over the network.
```bash
sudo apt install nfs-kernel-server
```
**Create Directory to Share:**

This command creates a directory (/nfs/share) on your system that you want to share via NFS. You can replace /nfs/share with the path to the directory you want to share.

```bash
sudo mkdir -p /nfs/share
```
**Configure NFS Exports:**

This command opens the exports file (/etc/exports) in the Nano text editor, allowing you to specify which directories to share and define the access permissions for NFS clients.

```bash
sudo vi /etc/exports
```

**Add a line in the following format:**
Add a line in the following format to the exports file:
/path/to/directory client_IP(options)

 In the exports file, you need to specify the directory you want to share (/nfs/share in this example), followed by the IP address or network range of the NFS clients allowed to access the share (* allows access from any IP), and the access permissions and options for the share (rw for read-write access, sync for synchronous writes, no_subtree_check to disable subtree checking).
```bash
/nfs/share *(rw,sync,no_subtree_check)
```
**Restart NFS Server:**
After making changes to the exports file, you need to restart the NFS server service (nfs-kernel-server) for the changes to take effect and the shared directories to become available to NFS clients.
sudo systemctl restart nfs-kernel-server


