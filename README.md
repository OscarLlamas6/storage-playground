# storage-playground

A comprehensive learning lab for storage systems at every level of the stack — physical devices, the Linux kernel storage stack, local filesystems, volume management, network storage protocols, distributed storage, cloud storage, container/Kubernetes storage, performance engineering, and emerging technologies. ~220 topics across 20 categories. Designed for 12-18 months of progressive study.

## The storage stack

```
┌─────────────────────────────────────────────────────────────┐
│  Applications (databases, object stores, user apps)          │
├─────────────────────────────────────────────────────────────┤
│  POSIX / io_uring / SPDK (I/O interfaces)                    │
├─────────────────────────────────────────────────────────────┤
│  VFS — Virtual Filesystem Layer                              │
├──────────────┬──────────────────────────────────────────────┤
│  Filesystems │ Network filesystems    │ Object storage       │
│  (ext4, ZFS, │ (NFS, SMB, CephFS,    │ (S3, RADOS, MinIO)  │
│  XFS, Btrfs) │ HDFS, GlusterFS)      │                      │
├──────────────┴──────────────────────────────────────────────┤
│  Volume Management (LVM, mdraid, dm-crypt, dm-multipath)     │
├─────────────────────────────────────────────────────────────┤
│  Block Layer (I/O schedulers, bio, device mapper)            │
├─────────────────────────────────────────────────────────────┤
│  Storage protocols  │ SAN (iSCSI, FC) │ NVMe-oF │ RDMA      │
├─────────────────────┴─────────────────┴─────────┴──────────┤
│  Physical devices (HDD, SSD, NVMe, ZNS, PMEM, CXL)          │
└─────────────────────────────────────────────────────────────┘
```

## Level and domain legend

- 🟢 Beginner | 🟡 Intermediate | 🔴 Advanced | 🔵 Expert
- 💾 Hardware | 🐧 Linux/Kernel | 📁 Filesystem | 🌐 Network | ☁️ Cloud | 🔬 Research

## Storage type quick reference

| Storage type   | Access model     | Examples                        | Best for                      |
|----------------|------------------|----------------------------------|-------------------------------|
| Block          | Fixed-size blocks| SAN, iSCSI, EBS, NVMe-oF        | Databases, VMs, raw I/O       |
| File           | Hierarchical FS  | NFS, SMB, EFS, NAS              | Shared files, home dirs       |
| Object         | Key-value + HTTP | S3, MinIO, Ceph RGW             | Unstructured data, backups    |
| Distributed FS | POSIX-like       | HDFS, GlusterFS, CephFS, Lustre | Big data, HPC, parallel I/O   |
| In-memory      | DRAM speed       | tmpfs, PMEM, CXL memory         | Caches, temp data              |

## Latency reference

| Storage medium        | Typical latency   | Typical IOPS (random 4K)  |
|-----------------------|-------------------|----------------------------|
| CPU L1 cache          | ~1 ns             | N/A                        |
| DRAM                  | ~100 ns           | N/A                        |
| NVMe SSD (local)      | ~100 µs           | 500K - 1M+                 |
| SATA SSD              | ~500 µs           | 50K - 100K                 |
| NVMe-oF (RDMA)        | ~200 µs           | 400K+                      |
| NVMe-oF (TCP)         | ~500 µs           | 200K+                      |
| iSCSI                 | ~1 ms             | 50K - 150K                 |
| HDD (7200 rpm)        | ~5-10 ms          | 100-200                    |
| NFS (LAN)             | ~1-5 ms           | 10K - 50K                  |
| Cloud block (EBS gp3) | ~1 ms             | up to 16K                  |
| Object storage (S3)   | ~50-200 ms        | Hundreds (first byte)      |
| Tape                  | ~30-60 sec        | Sequential only            |

## Recommended learning path

```
Months 1-2:   01 → 02 → 03            (fundamentals + hardware + Linux stack)
Months 3-4:   05 → 06                  (local filesystems + internals)
Months 5-6:   07 → 04                  (volume management + async I/O interfaces)
Months 7-8:   08 → 09                  (SAN/block storage + NAS/file storage)
Months 9-10:  10 → 11                  (object storage + distributed filesystems)
Months 11-12: 12 → 13                  (distributed block + cloud storage)
Months 13-14: 14 → 15                  (container/K8s storage + performance)
Months 15-16: 16 → 17                  (backup/DR + security)
Months 17-18: 18 → 19 → 20            (DB engines + advanced hardware + emerging)

Note: Category 03 (Linux storage stack) is a prerequisite for categories 04-07.
      Category 01 (fundamentals) is a prerequisite for everything.
```

## Categories

- [01-fundamentals](./01-fundamentals/) 🟢 — The foundational vocabulary and mental models for storage systems: how data goes from bits to blocks to files to objects, the storage hierarchy, and the core tradeoffs (latency, throughput, durability) that every other category builds on.
- [02-physical-storage-devices](./02-physical-storage-devices/) 🟢🟡💾 — The physical media that actually stores bits: HDD mechanics, NAND flash and SSD internals, NVMe, PCIe, persistent memory, and emerging device-level technologies like ZNS and SMR.
- [03-linux-storage-stack](./03-linux-storage-stack/) 🟡🔴🐧 — The Linux kernel's storage path from the VFS down to the block layer: page cache, I/O schedulers, device mapper, and the tools used to observe and debug it.
- [04-io-interfaces-and-async](./04-io-interfaces-and-async/) 🔴🔵🐧🔬 — How applications actually issue I/O: from blocking POSIX read/write through O_DIRECT and mmap, to modern async interfaces like io_uring and userspace stacks like SPDK/DPDK.
- [05-filesystems-local](./05-filesystems-local/) 🟢🟡🔴📁 — The major local filesystems in use today, from legacy FAT/NTFS through the Linux mainstays (ext4, XFS, Btrfs, ZFS) to flash-aware and userspace filesystems.
- [06-filesystem-internals](./06-filesystem-internals/) 🔴🔵📁 — The data structures and algorithms underneath filesystems: inodes, journaling, copy-on-write, extents, snapshots, dedup, compression, encryption, and consistency checking.
- [07-volume-management](./07-volume-management/) 🟡🔴🐧 — The layer between raw block devices and filesystems: partitioning, LVM, software RAID, thin provisioning, caching, encryption, and integrity verification at the device-mapper level.
- [08-block-storage-and-san](./08-block-storage-and-san/) 🟡🔴🌐 — Network-attached block storage: SAN architectures, Fibre Channel, iSCSI, and NVMe-oF over TCP/RDMA/InfiniBand, plus multipathing and LUN management.
- [09-network-file-storage-nas](./09-network-file-storage-nas/) 🟡🔴🌐 — File-level network storage: NFS (v3 through v4.2/pNFS), SMB/CIFS, Samba, WebDAV, and the operational concerns of NAS (HA, performance tuning, automounting).
- [10-object-storage](./10-object-storage/) 🟡🔴☁️ — The key-value/HTTP object storage model: the S3 API as the de facto standard, self-hosted alternatives (MinIO, Ceph RGW, Swift, SeaweedFS, Garage), and concerns like erasure coding, tiering, and security.
- [11-distributed-filesystems](./11-distributed-filesystems/) 🔴🔵🌐 — POSIX-like filesystems that span many machines: the GFS/HDFS lineage, HPC filesystems (Lustre, GPFS, BeeGFS), and modern entrants like Weka and DAOS.
- [12-distributed-block-storage](./12-distributed-block-storage/) 🔴🔵🌐 — Block devices backed by a distributed storage cluster: Ceph RBD and CRUSH, Kubernetes-native options (Longhorn, OpenEBS/Mayastor, Portworx), and DRBD-based replication.
- [13-cloud-storage](./13-cloud-storage/) 🟡🔴☁️ — Managed storage services from the big three clouds: block (EBS/PD/Managed Disks), file (EFS/Filestore/Azure Files), object (S3/GCS/Blob), and patterns for tiering and hybrid/multicloud.
- [14-container-and-kubernetes-storage](./14-container-and-kubernetes-storage/) 🟡🔴☁️ — How containers and Kubernetes consume storage: Docker volumes/bind mounts, the CSI spec, PVs/PVCs/StorageClasses, snapshots/cloning, and local vs shared (RWX) storage patterns.
- [15-storage-performance](./15-storage-performance/) 🟡🔴 — Cross-cutting performance engineering: benchmarking methodology, fio deep-dives, I/O patterns and queue depth, observability with iostat/blktrace/perf/eBPF, and recognizing anti-patterns.
- [16-backup-replication-dr](./16-backup-replication-dr/) 🟡🔴 — Data protection strategies: backup types and the 3-2-1 rule, snapshot-based and tool-based backup (restic, Borg, rsync/rclone), filesystem-level replication (ZFS/Btrfs send-receive, DRBD), and Kubernetes-native backup.
- [17-storage-security](./17-storage-security/) 🟡🔴 — Securing data at rest and in transit: dm-crypt/LUKS, filesystem-level encryption, key management (Tang/Clevis), self-encrypting drives, NFS/SMB security, object storage SSE, and immutable/WORM storage.
- [18-database-storage-engines](./18-database-storage-engines/) 🔴🔵 — How databases manage data on disk: B-trees and B+trees, LSM-trees, WAL and MVCC, and a tour of real engines (InnoDB, RocksDB, WiredTiger, Postgres heap, SQLite, columnar formats, vector indexes).
- [19-advanced-storage-hardware](./19-advanced-storage-hardware/) 🔴🔵💾🔬 — The cutting edge of storage hardware: NVMe 2.0 and ZNS deep-dives, computational storage, CXL memory pooling and cache coherence, RDMA/RoCE/InfiniBand, near-storage compute, and disaggregated architectures.
- [20-emerging-and-new](./20-emerging-and-new/) 🔵🔬 — A living category for new storage technologies, protocols, and hardware as they emerge: AI/GPU storage architectures, peer-to-peer storage, WASM, and the next generation of Linux-native filesystems.

## Comparison table

| Topic | Category | Level | Domain | Layer in stack | Key command | Status |
|-------|----------|-------|--------|-----------------|--------------|--------|

## Progress

### 01 - Fundamentals 🟢
- [ ] 🟢 00-fundamentals
- [ ] 🟢 01-bits-blocks-files-objects-the-abstractions
- [ ] 🟢 02-storage-hierarchy-registers-to-tape
- [ ] 🟢 03-latency-numbers-storage-edition
- [ ] 🟢 04-sequential-vs-random-io
- [ ] 🟢 05-iops-throughput-latency-the-triad
- [ ] 🟢 06-block-vs-file-vs-object-storage
- [ ] 🟢 07-posix-storage-api
- [ ] 🟢 08-durability-vs-availability-vs-performance
- [ ] 🟢 09-storage-in-the-context-of-cap-theorem

### 02 - Physical Storage Devices 🟢🟡💾
- [ ] 🟢💾 00-fundamentals
- [ ] 🟢💾 01-hdd-mechanics-platters-heads-sectors
- [ ] 🟢💾 02-hdd-seek-time-rotational-latency
- [ ] 🟢💾 03-ssd-nand-flash-cells-slc-mlc-tlc-qlc
- [ ] 🟢💾 04-ssd-wear-leveling-and-gc
- [ ] 🟢💾 05-ssd-write-amplification
- [ ] 🟢💾 06-nvme-protocol-and-queues
- [ ] 🟢💾 07-nvme-vs-sata-vs-sas
- [ ] 🟡💾 08-pcie-generations-and-bandwidth
- [ ] 🟡💾 09-smr-shingled-magnetic-recording
- [ ] 🟡💾 10-zns-zoned-namespaces
- [ ] 🟡💾 11-persistent-memory-pmem-optane
- [ ] 🟡💾 12-tape-storage-still-relevant
- [ ] 🟡💾 13-storage-class-memory
- [ ] 🟡💾 14-raid-hardware-controllers

### 03 - Linux Storage Stack 🟡🔴🐧
- [ ] 🟡🐧 00-fundamentals
- [ ] 🟡🐧 01-vfs-virtual-filesystem-layer
- [ ] 🟡🐧 02-page-cache-and-buffer-cache
- [ ] 🟡🐧 03-block-layer-overview
- [ ] 🟡🐧 04-bio-block-io-structure
- [ ] 🟡🐧 05-io-schedulers-mq-deadline-kyber-bfq
- [ ] 🟡🐧 06-device-mapper
- [ ] 🟡🐧 07-blktrace-and-blkparse
- [ ] 🔴🐧 08-iostat-iotop-sar
- [ ] 🔴🐧 09-sysfs-and-storage
- [ ] 🔴🐧 10-udev-and-device-management
- [ ] 🔴🐧 11-multipath-dm-multipath
- [ ] 🔴🐧 12-scsi-subsystem
- [ ] 🔴🐧 13-nvme-driver-internals

### 04 - I/O Interfaces & Async I/O 🔴🔵🐧🔬
- [ ] 🔴🐧 00-fundamentals
- [ ] 🔴🐧 01-posix-read-write-sync
- [ ] 🔴🐧 02-o-direct-bypassing-page-cache
- [ ] 🔴🐧 03-o-sync-and-fsync
- [ ] 🔴🐧 04-mmap-memory-mapped-io
- [ ] 🔴🐧 05-linux-aio
- [ ] 🔴🐧 06-io-uring-fundamentals
- [ ] 🔴🔬 07-io-uring-sqe-cqe-rings
- [ ] 🔵🔬 08-io-uring-vs-epoll-vs-aio
- [ ] 🔵🔬 09-spdk-userspace-storage
- [ ] 🔵🔬 10-dpdk-for-storage
- [ ] 🔵🔬 11-xnvme
- [ ] 🔵🔬 12-fio-benchmarking-tool
- [ ] 🔵🔬 13-libaio-vs-io-uring-benchmarks

### 05 - Local Filesystems 🟢🟡🔴📁
- [ ] 🟢📁 00-fundamentals
- [ ] 🟢📁 01-fat16-fat32-legacy-but-everywhere
- [ ] 🟢📁 02-exfat
- [ ] 🟢📁 03-ntfs
- [ ] 🟢📁 04-ext2-no-journaling
- [ ] 🟢📁 05-ext3-journaling-added
- [ ] 🟡📁 06-ext4-current-linux-default
- [ ] 🟡📁 07-xfs-high-performance-default-rhel
- [ ] 🟡📁 08-btrfs-copy-on-write
- [ ] 🟡📁 09-zfs-enterprise-grade
- [ ] 🟡📁 10-f2fs-flash-friendly
- [ ] 🔴📁 11-erofs-read-only-compressed
- [ ] 🔴📁 12-apfs-apple
- [ ] 🔴📁 13-tmpfs-in-memory
- [ ] 🔴📁 14-overlayfs-union-filesystem
- [ ] 🔴📁 15-fuse-user-space-fs

### 06 - Filesystem Internals 🔴🔵📁
- [ ] 🔴📁 00-fundamentals
- [ ] 🔴📁 01-inodes-and-directory-entries
- [ ] 🔴📁 02-superblock-and-metadata
- [ ] 🔴📁 03-journaling-modes-writeback-ordered-data
- [ ] 🔴📁 04-copy-on-write-cow-semantics
- [ ] 🔴📁 05-extents-vs-block-maps
- [ ] 🔴📁 06-fsck-and-consistency
- [ ] 🔴📁 07-snapshots-mechanisms
- [ ] 🔵📁 08-deduplication
- [ ] 🔵📁 09-compression-in-filesystems
- [ ] 🔵📁 10-encryption-at-filesystem-level
- [ ] 🔵📁 11-quotas-and-project-ids
- [ ] 🔵📁 12-acls-and-extended-attributes
- [ ] 🔵📁 13-filesystem-benchmarking

### 07 - Volume Management 🟡🔴🐧
- [ ] 🟡🐧 00-fundamentals
- [ ] 🟡🐧 01-partitioning-mbr-vs-gpt
- [ ] 🟡🐧 02-lvm-physical-volumes
- [ ] 🟡🐧 03-lvm-volume-groups
- [ ] 🟡🐧 04-lvm-logical-volumes
- [ ] 🟡🐧 05-lvm-snapshots
- [ ] 🟡🐧 06-lvm-thin-provisioning
- [ ] 🟡🐧 07-lvm-cache-lvmcache
- [ ] 🔴🐧 08-mdraid-software-raid
- [ ] 🔴🐧 09-raid-levels-0-1-5-6-10
- [ ] 🔴🐧 10-stratis-storage
- [ ] 🔴🐧 11-systemd-storage-daemon
- [ ] 🔴🐧 12-disk-encryption-luks-dm-crypt
- [ ] 🔴🐧 13-device-mapper-dm-verity-dm-integrity

### 08 - Block Storage & SAN 🟡🔴🌐
- [ ] 🟡🌐 00-fundamentals
- [ ] 🟡🌐 01-san-architecture
- [ ] 🟡🌐 02-fibre-channel-fc-basics
- [ ] 🟡🌐 03-fcoe-fc-over-ethernet
- [ ] 🟡🌐 04-iscsi-protocol
- [ ] 🟡🌐 05-iscsi-initiator-target-setup
- [ ] 🟡🌐 06-iscsi-vs-fc-comparison
- [ ] 🟡🌐 07-nvme-of-fundamentals
- [ ] 🔴🌐 08-nvme-of-over-tcp
- [ ] 🔴🌐 09-nvme-of-over-rdma-roce
- [ ] 🔴🌐 10-nvme-of-over-infiniband
- [ ] 🔴🌐 11-spdk-nvme-of-target
- [ ] 🔴🌐 12-multipath-for-san
- [ ] 🔴🌐 13-san-zoning-and-masking
- [ ] 🔴🌐 14-lun-management

### 09 - Network File Storage (NAS) 🟡🔴🌐
- [ ] 🟡🌐 00-fundamentals
- [ ] 🟡🌐 01-nas-vs-san
- [ ] 🟡🌐 02-nfs-v3-fundamentals
- [ ] 🟡🌐 03-nfs-v4-and-v4-1-pnfs
- [ ] 🟡🌐 04-nfs-v4-2-new-features
- [ ] 🟡🌐 05-smb-cifs-protocol
- [ ] 🟡🌐 06-smb-multichannel
- [ ] 🟡🌐 07-samba
- [ ] 🔴🌐 08-afp-apple-filing-protocol-legacy
- [ ] 🔴🌐 09-nfs-performance-tuning
- [ ] 🔴🌐 10-rdma-for-nfs-nfs-rdma
- [ ] 🔴🌐 11-autofs-and-automounting
- [ ] 🔴🌐 12-nas-ha-and-failover
- [ ] 🔴🌐 13-9p-plan9-protocol
- [ ] 🔴🌐 14-webdav

### 10 - Object Storage 🟡🔴☁️
- [ ] 🟡☁️ 00-fundamentals
- [ ] 🟡☁️ 01-object-storage-model-key-value
- [ ] 🟡☁️ 02-s3-api-the-de-facto-standard
- [ ] 🟡☁️ 03-s3-consistency-model
- [ ] 🟡☁️ 04-s3-multipart-uploads
- [ ] 🟡☁️ 05-s3-versioning-and-lifecycle
- [ ] 🟡☁️ 06-minio-self-hosted-s3
- [ ] 🟡☁️ 07-ceph-rados-object-storage
- [ ] 🔴☁️ 08-openstack-swift
- [ ] 🔴☁️ 09-seaweedfs
- [ ] 🔴☁️ 10-garage-distributed-object-store
- [ ] 🔴☁️ 11-object-storage-erasure-coding
- [ ] 🔴☁️ 12-object-storage-tiering
- [ ] 🔴☁️ 13-content-addressed-storage
- [ ] 🔴☁️ 14-object-storage-security

### 11 - Distributed Filesystems 🔴🔵🌐
- [ ] 🔴🌐 00-fundamentals
- [ ] 🔴🌐 01-gfs-google-filesystem-paper
- [ ] 🔴🌐 02-hdfs-hadoop-distributed-fs
- [ ] 🔴🌐 03-glusterfs
- [ ] 🔴🌐 04-lustre-hpc-filesystem
- [ ] 🔴🌐 05-gpfs-ibm-spectrum-scale
- [ ] 🔴🌐 06-beegfs-parallel-fs
- [ ] 🔵🌐 07-moosefs
- [ ] 🔵🌐 08-saunafs
- [ ] 🔵🌐 09-weka-io
- [ ] 🔵🌐 10-daos-distributed-async-object-store
- [ ] 🔵🌐 11-distributed-fs-consistency-models
- [ ] 🔵🌐 12-distributed-fs-metadata-servers

### 12 - Distributed Block Storage 🔴🔵🌐
- [ ] 🔴🌐 00-fundamentals
- [ ] 🔴🌐 01-ceph-architecture-overview
- [ ] 🔴🌐 02-ceph-rados
- [ ] 🔴🌐 03-ceph-rbd-block-device
- [ ] 🔴🌐 04-ceph-cephfs
- [ ] 🔴🌐 05-ceph-rgw-object-gateway
- [ ] 🔴🌐 06-ceph-crush-algorithm
- [ ] 🔴🌐 07-rook-ceph-on-kubernetes
- [ ] 🔵🌐 08-longhorn
- [ ] 🔵🌐 09-openebs-and-mayastor
- [ ] 🔵🌐 10-portworx
- [ ] 🔵🌐 11-linstor-drbd
- [ ] 🔵🌐 12-vitastor
- [ ] 🔵🌐 13-xatastor-zfs-nvme-of
- [ ] 🔵🌐 14-distributed-block-consistency-models

### 13 - Cloud Storage 🟡🔴☁️
- [ ] 🟡☁️ 00-fundamentals
- [ ] 🟡☁️ 01-aws-ebs-block-storage
- [ ] 🟡☁️ 02-aws-efs-elastic-file
- [ ] 🟡☁️ 03-aws-s3-deep-dive
- [ ] 🟡☁️ 04-aws-fsx-family
- [ ] 🟡☁️ 05-aws-storage-gateway
- [ ] 🟡☁️ 06-gcp-persistent-disk
- [ ] 🟡☁️ 07-gcp-filestore
- [ ] 🔴☁️ 08-gcp-cloud-storage
- [ ] 🔴☁️ 09-azure-managed-disks
- [ ] 🔴☁️ 10-azure-files
- [ ] 🔴☁️ 11-azure-blob-storage
- [ ] 🔴☁️ 12-cloud-storage-tiering
- [ ] 🔴☁️ 13-cloud-to-on-prem-hybrid
- [ ] 🔴☁️ 14-multicloud-storage-patterns

### 14 - Container & Kubernetes Storage 🟡🔴☁️
- [ ] 🟡☁️ 00-fundamentals
- [ ] 🟡☁️ 01-docker-volumes
- [ ] 🟡☁️ 02-docker-bind-mounts
- [ ] 🟡☁️ 03-docker-tmpfs
- [ ] 🟡☁️ 04-csi-container-storage-interface
- [ ] 🟡☁️ 05-kubernetes-persistent-volumes
- [ ] 🟡☁️ 06-kubernetes-persistent-volume-claims
- [ ] 🟡☁️ 07-kubernetes-storage-classes
- [ ] 🔴☁️ 08-kubernetes-statefulsets-and-storage
- [ ] 🔴☁️ 09-volume-snapshots-k8s
- [ ] 🔴☁️ 10-volume-cloning
- [ ] 🔴☁️ 11-local-storage-in-k8s
- [ ] 🔴☁️ 12-shared-storage-rwx-in-k8s
- [ ] 🔴☁️ 13-csi-driver-development
- [ ] 🔴☁️ 14-storage-capacity-tracking

### 15 - Storage Performance 🟡🔴
- [ ] 🟡 00-fundamentals
- [ ] 🟡 01-iops-throughput-latency-tradeoffs
- [ ] 🟡 02-fio-comprehensive-guide
- [ ] 🟡 03-io-patterns-sequential-random-mixed
- [ ] 🟡 04-queue-depth-and-parallelism
- [ ] 🟡 05-read-ahead-and-write-behind
- [ ] 🟡 06-iostat-deep-dive
- [ ] 🟡 07-blktrace-analysis
- [ ] 🔴 08-perf-for-storage
- [ ] 🔴 09-ebpf-storage-observability
- [ ] 🔴 10-storage-benchmarking-methodologies
- [ ] 🔴 11-write-amplification-measurement
- [ ] 🔴 12-latency-percentiles-p99-p9999
- [ ] 🔴 13-storage-performance-anti-patterns

### 16 - Backup, Replication & DR 🟡🔴
- [ ] 🟡 00-fundamentals
- [ ] 🟡 01-backup-strategies-full-incremental-diff
- [ ] 🟡 02-snapshot-based-backup
- [ ] 🟡 03-backup-3-2-1-rule
- [ ] 🟡 04-rpo-and-rto
- [ ] 🟡 05-rsync-and-rclone
- [ ] 🟡 06-restic
- [ ] 🟡 07-borg-backup
- [ ] 🔴 08-zfs-replication
- [ ] 🔴 09-btrfs-send-receive
- [ ] 🔴 10-drbd-block-replication
- [ ] 🔴 11-velero-k8s-backup
- [ ] 🔴 12-kasten-k10
- [ ] 🔴 13-backup-verification
- [ ] 🔴 14-disaster-recovery-patterns

### 17 - Storage Security 🟡🔴
- [ ] 🟡 00-fundamentals
- [ ] 🟡 01-encryption-at-rest-overview
- [ ] 🟡 02-dm-crypt-and-luks
- [ ] 🟡 03-luks2-and-argon2
- [ ] 🟡 04-filesystem-level-encryption-fscrypt
- [ ] 🟡 05-encrypted-filesystems-ecryptfs
- [ ] 🟡 06-key-management-tang-clevis
- [ ] 🟡 07-tpm-and-secure-boot-for-storage
- [ ] 🔴 08-self-encrypting-drives-sed-opal
- [ ] 🔴 09-nfs-security-kerberos
- [ ] 🔴 10-smb-signing-and-encryption
- [ ] 🔴 11-object-storage-sse-sse-c-sse-kms
- [ ] 🔴 12-ransomware-protection-patterns
- [ ] 🔴 13-storage-audit-and-compliance
- [ ] 🔴 14-immutable-storage-worm

### 18 - Database Storage Engines 🔴🔵
- [ ] 🔴 00-fundamentals
- [ ] 🔴 01-b-tree-the-dominant-structure
- [ ] 🔴 02-b-plus-tree
- [ ] 🔴 03-lsm-tree-log-structured-merge
- [ ] 🔴 04-write-ahead-log-wal
- [ ] 🔴 05-mvcc-multi-version-concurrency
- [ ] 🔴 06-innodb-storage-engine
- [ ] 🔴 07-rocksdb-lsm-in-production
- [ ] 🔵 08-wiredtiger-mongodb
- [ ] 🔵 09-postgres-heap-and-toast
- [ ] 🔵 10-sqlite-btree-internals
- [ ] 🔵 11-columnar-storage-parquet-orc
- [ ] 🔵 12-time-series-storage-tsm
- [ ] 🔵 13-vector-storage-for-llm
- [ ] 🔵 14-compaction-strategies

### 19 - Advanced Storage Hardware 🔴🔵💾🔬
- [ ] 🔴💾 00-fundamentals
- [ ] 🔴💾 01-nvme-2-0-features
- [ ] 🔴💾 02-zns-zoned-namespaces-deep-dive
- [ ] 🔴💾 03-computational-storage-devices
- [ ] 🔴💾 04-cxl-compute-express-link
- [ ] 🔴💾 05-cxl-memory-pooling
- [ ] 🔴💾 06-cxl-3-0-cache-coherence
- [ ] 🔴🔬 07-rdma-remote-direct-memory-access
- [ ] 🔵🔬 08-roce-rdma-over-ethernet
- [ ] 🔵🔬 09-infiniband
- [ ] 🔵🔬 10-smart-ssds-and-near-storage-compute
- [ ] 🔵🔬 11-disaggregated-storage-architectures
- [ ] 🔵🔬 12-800g-ethernet-for-storage
- [ ] 🔵🔬 13-storage-class-memory-optane-successor

### 20 - Emerging & New 🔵🔬
- [ ] 🔵🔬 00-fundamentals
- [ ] 🔵🔬 01-ai-storage-architectures
- [ ] 🔵🔬 02-llm-kv-cache-storage
- [ ] 🔵🔬 03-gpu-storage-direct-gds
- [ ] 🔵🔬 04-software-defined-storage-trends
- [ ] 🔵🔬 05-wasm-and-storage
- [ ] 🔵🔬 06-p2p-storage-ipfs-iroh-blobs
- [ ] 🔵🔬 07-bcachefs-new-linux-fs
- [ ] 🔵🔬 08-zfs-on-linux-2026-state
- [ ] 🔵🔬 09-placeholder-new-topic

## Recommended resources

- [Linux Storage Stack Diagram (Werner Fischer)](https://www.thomas-krenn.com/en/wiki/Linux_Storage_Stack_Diagram)
- [Linux Kernel docs — block layer](https://www.kernel.org/doc/html/latest/block/)
- [Linux Kernel docs — filesystems](https://www.kernel.org/doc/html/latest/filesystems/)
- [Ceph documentation](https://docs.ceph.com/)
- [ZFS on Linux (OpenZFS)](https://openzfs.github.io/openzfs-docs/)
- [NVMe Spec (NVMe Express)](https://nvmexpress.org/specifications/)
- [io_uring — Efficient I/O with io_uring (Jens Axboe)](https://kernel.dk/io_uring.pdf)
- [SPDK documentation](https://spdk.io/doc/)
- [The NFS Book — Solaris/Linux NFS deep dive](https://www.oreilly.com/library/view/managing-nfs-and/1565925106/)
- [Database Internals — Alex Petrov (storage engines)](https://www.databass.dev/)
- [Designing Data-Intensive Applications — Kleppmann (Ch. 3, storage engines)](https://dataintensive.net/)
- [StorageNewsletter.com — industry news](https://www.storagenewsletter.com/)

## Companion repositories

> This repo covers storage systems in depth.
>
> For caching layers (Redis, CDN, eviction policies): `cache-playground`
>
> For distributed systems theory (consensus, replication, consistency): `distributed-systems-playground`
>
> For Kubernetes storage operators in practice (Longhorn, Rook, CSI): `k8s-playground`
>
> For networking protocols (NFS/SMB at protocol level, iSCSI): `networking-playground`
>
> For Linux kernel internals beyond storage: `compute-isolation-playground`

## 20 - Emerging & New: a living category

> This is a living category. As new storage technologies, protocols, or hardware emerge during your study period, add them here as new subfolders. Particularly active areas in 2026: CXL 3.0 entering mainstream data centers, NVMe-oF over TCP replacing iSCSI in new deployments, bcachefs maturing as a Linux-native CoW filesystem, AI/GPU storage architectures (GPUDirect Storage), and disaggregated storage becoming the default in hyperscale environments.
