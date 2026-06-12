# 12-distributed-block-storage — Distributed Block Storage 🔴🔵🌐

Block devices backed by a distributed storage cluster: Ceph RBD and CRUSH, Kubernetes-native options (Longhorn, OpenEBS/Mayastor, Portworx), and DRBD-based replication.

**Layer(s) in the storage stack:** Distributed block storage — presents a block device interface backed by a cluster over the network.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🔴🌐
- [01-ceph-architecture-overview](./01-ceph-architecture-overview/) 🔴🌐
- [02-ceph-rados](./02-ceph-rados/) 🔴🌐
- [03-ceph-rbd-block-device](./03-ceph-rbd-block-device/) 🔴🌐
- [04-ceph-cephfs](./04-ceph-cephfs/) 🔴🌐
- [05-ceph-rgw-object-gateway](./05-ceph-rgw-object-gateway/) 🔴🌐
- [06-ceph-crush-algorithm](./06-ceph-crush-algorithm/) 🔴🌐
- [07-rook-ceph-on-kubernetes](./07-rook-ceph-on-kubernetes/) 🔴🌐
- [08-longhorn](./08-longhorn/) 🔵🌐
- [09-openebs-and-mayastor](./09-openebs-and-mayastor/) 🔵🌐
- [10-portworx](./10-portworx/) 🔵🌐
- [11-linstor-drbd](./11-linstor-drbd/) 🔵🌐
- [12-vitastor](./12-vitastor/) 🔵🌐
- [13-xatastor-zfs-nvme-of](./13-xatastor-zfs-nvme-of/) 🔵🌐
- [14-distributed-block-consistency-models](./14-distributed-block-consistency-models/) 🔵🌐

**Prerequisites:** 07-volume-management, 08-block-storage-and-san

**Key tool:** rbd / ceph
