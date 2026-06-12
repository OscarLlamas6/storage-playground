# 04-io-interfaces-and-async — I/O Interfaces & Async I/O 🔴🔵🐧🔬

How applications actually issue I/O: from blocking POSIX read/write through O_DIRECT and mmap, to modern async interfaces like io_uring and userspace stacks like SPDK/DPDK.

**Layer(s) in the storage stack:** Between applications and the kernel/userspace storage drivers.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🔴🐧
- [01-posix-read-write-sync](./01-posix-read-write-sync/) 🔴🐧
- [02-o-direct-bypassing-page-cache](./02-o-direct-bypassing-page-cache/) 🔴🐧
- [03-o-sync-and-fsync](./03-o-sync-and-fsync/) 🔴🐧
- [04-mmap-memory-mapped-io](./04-mmap-memory-mapped-io/) 🔴🐧
- [05-linux-aio](./05-linux-aio/) 🔴🐧
- [06-io-uring-fundamentals](./06-io-uring-fundamentals/) 🔴🐧
- [07-io-uring-sqe-cqe-rings](./07-io-uring-sqe-cqe-rings/) 🔴🔬
- [08-io-uring-vs-epoll-vs-aio](./08-io-uring-vs-epoll-vs-aio/) 🔵🔬
- [09-spdk-userspace-storage](./09-spdk-userspace-storage/) 🔵🔬
- [10-dpdk-for-storage](./10-dpdk-for-storage/) 🔵🔬
- [11-xnvme](./11-xnvme/) 🔵🔬
- [12-fio-benchmarking-tool](./12-fio-benchmarking-tool/) 🔵🔬
- [13-libaio-vs-io-uring-benchmarks](./13-libaio-vs-io-uring-benchmarks/) 🔵🔬

**Prerequisites:** 03-linux-storage-stack

**Key tool:** fio / io_uring
