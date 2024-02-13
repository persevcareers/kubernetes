**For Ubuntu/Debian:**

**Update Package Repositories:**
```bash
sudo apt update
```
Explanation: This command updates the package repositories on your Ubuntu system to ensure you have the latest package information.

**Install NFS Server Package:**

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
