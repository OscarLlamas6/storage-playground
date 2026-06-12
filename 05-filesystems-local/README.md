# 05-filesystems-local — Local Filesystems 🟢🟡🔴📁

The major local filesystems in use today, from legacy FAT/NTFS through the Linux mainstays (ext4, XFS, Btrfs, ZFS) to flash-aware and userspace filesystems.

**Layer(s) in the storage stack:** Local filesystems — sit on top of block devices, below VFS consumers.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟢📁
- [01-fat16-fat32-legacy-but-everywhere](./01-fat16-fat32-legacy-but-everywhere/) 🟢📁
- [02-exfat](./02-exfat/) 🟢📁
- [03-ntfs](./03-ntfs/) 🟢📁
- [04-ext2-no-journaling](./04-ext2-no-journaling/) 🟢📁
- [05-ext3-journaling-added](./05-ext3-journaling-added/) 🟢📁
- [06-ext4-current-linux-default](./06-ext4-current-linux-default/) 🟡📁
- [07-xfs-high-performance-default-rhel](./07-xfs-high-performance-default-rhel/) 🟡📁
- [08-btrfs-copy-on-write](./08-btrfs-copy-on-write/) 🟡📁
- [09-zfs-enterprise-grade](./09-zfs-enterprise-grade/) 🟡📁
- [10-f2fs-flash-friendly](./10-f2fs-flash-friendly/) 🟡📁
- [11-erofs-read-only-compressed](./11-erofs-read-only-compressed/) 🔴📁
- [12-apfs-apple](./12-apfs-apple/) 🔴📁
- [13-tmpfs-in-memory](./13-tmpfs-in-memory/) 🔴📁
- [14-overlayfs-union-filesystem](./14-overlayfs-union-filesystem/) 🔴📁
- [15-fuse-user-space-fs](./15-fuse-user-space-fs/) 🔴📁

**Prerequisites:** 01-fundamentals, 03-linux-storage-stack

**Key tool:** mkfs / mount
