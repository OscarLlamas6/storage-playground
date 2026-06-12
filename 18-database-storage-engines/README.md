# 18-database-storage-engines — Database Storage Engines 🔴🔵

How databases manage data on disk: B-trees and B+trees, LSM-trees, WAL and MVCC, and a tour of real engines (InnoDB, RocksDB, WiredTiger, Postgres heap, SQLite, columnar formats, vector indexes).

**Layer(s) in the storage stack:** Application-level storage engines, built on top of files/block devices via the local filesystem.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🔴
- [01-b-tree-the-dominant-structure](./01-b-tree-the-dominant-structure/) 🔴
- [02-b-plus-tree](./02-b-plus-tree/) 🔴
- [03-lsm-tree-log-structured-merge](./03-lsm-tree-log-structured-merge/) 🔴
- [04-write-ahead-log-wal](./04-write-ahead-log-wal/) 🔴
- [05-mvcc-multi-version-concurrency](./05-mvcc-multi-version-concurrency/) 🔴
- [06-innodb-storage-engine](./06-innodb-storage-engine/) 🔴
- [07-rocksdb-lsm-in-production](./07-rocksdb-lsm-in-production/) 🔴
- [08-wiredtiger-mongodb](./08-wiredtiger-mongodb/) 🔵
- [09-postgres-heap-and-toast](./09-postgres-heap-and-toast/) 🔵
- [10-sqlite-btree-internals](./10-sqlite-btree-internals/) 🔵
- [11-columnar-storage-parquet-orc](./11-columnar-storage-parquet-orc/) 🔵
- [12-time-series-storage-tsm](./12-time-series-storage-tsm/) 🔵
- [13-vector-storage-for-llm](./13-vector-storage-for-llm/) 🔵
- [14-compaction-strategies](./14-compaction-strategies/) 🔵

**Prerequisites:** 01-fundamentals, 05-filesystems-local

**Key tool:** sqlite3 / rocksdb tools
