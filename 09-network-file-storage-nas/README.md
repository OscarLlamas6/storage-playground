# 09-network-file-storage-nas — Network File Storage (NAS) 🟡🔴🌐

File-level network storage: NFS (v3 through v4.2/pNFS), SMB/CIFS, Samba, WebDAV, and the operational concerns of NAS (HA, performance tuning, automounting).

**Layer(s) in the storage stack:** Network filesystems — sit above the network stack, presented through VFS like local filesystems.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡🌐
- [01-nas-vs-san](./01-nas-vs-san/) 🟡🌐
- [02-nfs-v3-fundamentals](./02-nfs-v3-fundamentals/) 🟡🌐
- [03-nfs-v4-and-v4-1-pnfs](./03-nfs-v4-and-v4-1-pnfs/) 🟡🌐
- [04-nfs-v4-2-new-features](./04-nfs-v4-2-new-features/) 🟡🌐
- [05-smb-cifs-protocol](./05-smb-cifs-protocol/) 🟡🌐
- [06-smb-multichannel](./06-smb-multichannel/) 🟡🌐
- [07-samba](./07-samba/) 🟡🌐
- [08-afp-apple-filing-protocol-legacy](./08-afp-apple-filing-protocol-legacy/) 🔴🌐
- [09-nfs-performance-tuning](./09-nfs-performance-tuning/) 🔴🌐
- [10-rdma-for-nfs-nfs-rdma](./10-rdma-for-nfs-nfs-rdma/) 🔴🌐
- [11-autofs-and-automounting](./11-autofs-and-automounting/) 🔴🌐
- [12-nas-ha-and-failover](./12-nas-ha-and-failover/) 🔴🌐
- [13-9p-plan9-protocol](./13-9p-plan9-protocol/) 🔴🌐
- [14-webdav](./14-webdav/) 🔴🌐

**Prerequisites:** 05-filesystems-local

**Key tool:** mount.nfs / smbclient
