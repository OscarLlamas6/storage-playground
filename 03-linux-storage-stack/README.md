# 03-linux-storage-stack — Linux Storage Stack 🟡🔴🐧

The Linux kernel's storage path from the VFS down to the block layer: page cache, I/O schedulers, device mapper, and the tools used to observe and debug it.

**Layer(s) in the storage stack:** Kernel — VFS down through the block layer.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡🐧
- [01-vfs-virtual-filesystem-layer](./01-vfs-virtual-filesystem-layer/) 🟡🐧
- [02-page-cache-and-buffer-cache](./02-page-cache-and-buffer-cache/) 🟡🐧
- [03-block-layer-overview](./03-block-layer-overview/) 🟡🐧
- [04-bio-block-io-structure](./04-bio-block-io-structure/) 🟡🐧
- [05-io-schedulers-mq-deadline-kyber-bfq](./05-io-schedulers-mq-deadline-kyber-bfq/) 🟡🐧
- [06-device-mapper](./06-device-mapper/) 🟡🐧
- [07-blktrace-and-blkparse](./07-blktrace-and-blkparse/) 🟡🐧
- [08-iostat-iotop-sar](./08-iostat-iotop-sar/) 🔴🐧
- [09-sysfs-and-storage](./09-sysfs-and-storage/) 🔴🐧
- [10-udev-and-device-management](./10-udev-and-device-management/) 🔴🐧
- [11-multipath-dm-multipath](./11-multipath-dm-multipath/) 🔴🐧
- [12-scsi-subsystem](./12-scsi-subsystem/) 🔴🐧
- [13-nvme-driver-internals](./13-nvme-driver-internals/) 🔴🐧

**Prerequisites:** 01-fundamentals, 02-physical-storage-devices

**Key tool:** blktrace / iostat
