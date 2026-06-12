# 16-backup-replication-dr — Backup, Replication & DR 🟡🔴

Data protection strategies: backup types and the 3-2-1 rule, snapshot-based and tool-based backup (restic, Borg, rsync/rclone), filesystem-level replication (ZFS/Btrfs send-receive, DRBD), and Kubernetes-native backup.

**Layer(s) in the storage stack:** Cross-cutting — operates on top of filesystems, volumes, and object storage.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡
- [01-backup-strategies-full-incremental-diff](./01-backup-strategies-full-incremental-diff/) 🟡
- [02-snapshot-based-backup](./02-snapshot-based-backup/) 🟡
- [03-backup-3-2-1-rule](./03-backup-3-2-1-rule/) 🟡
- [04-rpo-and-rto](./04-rpo-and-rto/) 🟡
- [05-rsync-and-rclone](./05-rsync-and-rclone/) 🟡
- [06-restic](./06-restic/) 🟡
- [07-borg-backup](./07-borg-backup/) 🟡
- [08-zfs-replication](./08-zfs-replication/) 🔴
- [09-btrfs-send-receive](./09-btrfs-send-receive/) 🔴
- [10-drbd-block-replication](./10-drbd-block-replication/) 🔴
- [11-velero-k8s-backup](./11-velero-k8s-backup/) 🔴
- [12-kasten-k10](./12-kasten-k10/) 🔴
- [13-backup-verification](./13-backup-verification/) 🔴
- [14-disaster-recovery-patterns](./14-disaster-recovery-patterns/) 🔴

**Prerequisites:** 05-filesystems-local, 10-object-storage

**Key tool:** restic / rsync
