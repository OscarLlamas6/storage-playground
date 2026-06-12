# 11-distributed-filesystems — Distributed Filesystems 🔴🔵🌐

POSIX-like filesystems that span many machines: the GFS/HDFS lineage, HPC filesystems (Lustre, GPFS, BeeGFS), and modern entrants like Weka and DAOS.

**Layer(s) in the storage stack:** Distributed filesystems — a network-spanning filesystem layer, often presented via FUSE or a custom client.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🔴🌐
- [01-gfs-google-filesystem-paper](./01-gfs-google-filesystem-paper/) 🔴🌐
- [02-hdfs-hadoop-distributed-fs](./02-hdfs-hadoop-distributed-fs/) 🔴🌐
- [03-glusterfs](./03-glusterfs/) 🔴🌐
- [04-lustre-hpc-filesystem](./04-lustre-hpc-filesystem/) 🔴🌐
- [05-gpfs-ibm-spectrum-scale](./05-gpfs-ibm-spectrum-scale/) 🔴🌐
- [06-beegfs-parallel-fs](./06-beegfs-parallel-fs/) 🔴🌐
- [07-moosefs](./07-moosefs/) 🔵🌐
- [08-saunafs](./08-saunafs/) 🔵🌐
- [09-weka-io](./09-weka-io/) 🔵🌐
- [10-daos-distributed-async-object-store](./10-daos-distributed-async-object-store/) 🔵🌐
- [11-distributed-fs-consistency-models](./11-distributed-fs-consistency-models/) 🔵🌐
- [12-distributed-fs-metadata-servers](./12-distributed-fs-metadata-servers/) 🔵🌐

**Prerequisites:** 05-filesystems-local, 09-network-file-storage-nas

**Key tool:** hdfs / mount.glusterfs
