# 06-filesystem-internals — Filesystem Internals 🔴🔵📁

The data structures and algorithms underneath filesystems: inodes, journaling, copy-on-write, extents, snapshots, dedup, compression, encryption, and consistency checking.

**Layer(s) in the storage stack:** Internal mechanisms of local filesystems (below the FS API, above the block layer).

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🔴📁
- [01-inodes-and-directory-entries](./01-inodes-and-directory-entries/) 🔴📁
- [02-superblock-and-metadata](./02-superblock-and-metadata/) 🔴📁
- [03-journaling-modes-writeback-ordered-data](./03-journaling-modes-writeback-ordered-data/) 🔴📁
- [04-copy-on-write-cow-semantics](./04-copy-on-write-cow-semantics/) 🔴📁
- [05-extents-vs-block-maps](./05-extents-vs-block-maps/) 🔴📁
- [06-fsck-and-consistency](./06-fsck-and-consistency/) 🔴📁
- [07-snapshots-mechanisms](./07-snapshots-mechanisms/) 🔴📁
- [08-deduplication](./08-deduplication/) 🔵📁
- [09-compression-in-filesystems](./09-compression-in-filesystems/) 🔵📁
- [10-encryption-at-filesystem-level](./10-encryption-at-filesystem-level/) 🔵📁
- [11-quotas-and-project-ids](./11-quotas-and-project-ids/) 🔵📁
- [12-acls-and-extended-attributes](./12-acls-and-extended-attributes/) 🔵📁
- [13-filesystem-benchmarking](./13-filesystem-benchmarking/) 🔵📁

**Prerequisites:** 05-filesystems-local

**Key tool:** debugfs / xfs_db
