**For Ubuntu/Debian:**

**Update Package Repositories:**
This command updates the package repositories on your Ubuntu system to ensure you have the latest package information.
```bash
sudo apt update
```
This command updates the package repositories on your Ubuntu system to ensure you have the latest package information.

**Install NFS Server Package:**

This command installs the NFS server package (nfs-kernel-server) on your Ubuntu system, which allows your system to act as an NFS server and share directories over the network.
```bash
sudo apt install nfs-kernel-server
```
**Create Directory to Share:**

Create a directory that you want to share via NFS. For example:

```bash
sudo mkdir -p /nfs/share
```
**Configure NFS Exports:**

Edit the exports file to specify which directories to share and the access permissions.

```bash
sudo vi /etc/exports
```

**Add a line in the following format:**

For example:
/path/to/directory client_IP(options)
```bash
/nfs/share *(rw,sync,no_subtree_check)
```
