# 07-volume-management — Volume Management 🟡🔴🐧

The layer between raw block devices and filesystems: partitioning, LVM, software RAID, thin provisioning, caching, encryption, and integrity verification at the device-mapper level.

**Layer(s) in the storage stack:** Between physical/block devices and filesystems.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡🐧
- [01-partitioning-mbr-vs-gpt](./01-partitioning-mbr-vs-gpt/) 🟡🐧
- [02-lvm-physical-volumes](./02-lvm-physical-volumes/) 🟡🐧
- [03-lvm-volume-groups](./03-lvm-volume-groups/) 🟡🐧
- [04-lvm-logical-volumes](./04-lvm-logical-volumes/) 🟡🐧
- [05-lvm-snapshots](./05-lvm-snapshots/) 🟡🐧
- [06-lvm-thin-provisioning](./06-lvm-thin-provisioning/) 🟡🐧
- [07-lvm-cache-lvmcache](./07-lvm-cache-lvmcache/) 🟡🐧
- [08-mdraid-software-raid](./08-mdraid-software-raid/) 🔴🐧
- [09-raid-levels-0-1-5-6-10](./09-raid-levels-0-1-5-6-10/) 🔴🐧
- [10-stratis-storage](./10-stratis-storage/) 🔴🐧
- [11-systemd-storage-daemon](./11-systemd-storage-daemon/) 🔴🐧
- [12-disk-encryption-luks-dm-crypt](./12-disk-encryption-luks-dm-crypt/) 🔴🐧
- [13-device-mapper-dm-verity-dm-integrity](./13-device-mapper-dm-verity-dm-integrity/) 🔴🐧

**Prerequisites:** 03-linux-storage-stack

**Key tool:** lvm / mdadm
