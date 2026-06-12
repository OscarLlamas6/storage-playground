# 15-storage-performance — Storage Performance 🟡🔴

Cross-cutting performance engineering: benchmarking methodology, fio deep-dives, I/O patterns and queue depth, observability with iostat/blktrace/perf/eBPF, and recognizing anti-patterns.

**Layer(s) in the storage stack:** Cross-cutting — applies to every layer from physical devices to distributed storage.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡
- [01-iops-throughput-latency-tradeoffs](./01-iops-throughput-latency-tradeoffs/) 🟡
- [02-fio-comprehensive-guide](./02-fio-comprehensive-guide/) 🟡
- [03-io-patterns-sequential-random-mixed](./03-io-patterns-sequential-random-mixed/) 🟡
- [04-queue-depth-and-parallelism](./04-queue-depth-and-parallelism/) 🟡
- [05-read-ahead-and-write-behind](./05-read-ahead-and-write-behind/) 🟡
- [06-iostat-deep-dive](./06-iostat-deep-dive/) 🟡
- [07-blktrace-analysis](./07-blktrace-analysis/) 🟡
- [08-perf-for-storage](./08-perf-for-storage/) 🔴
- [09-ebpf-storage-observability](./09-ebpf-storage-observability/) 🔴
- [10-storage-benchmarking-methodologies](./10-storage-benchmarking-methodologies/) 🔴
- [11-write-amplification-measurement](./11-write-amplification-measurement/) 🔴
- [12-latency-percentiles-p99-p9999](./12-latency-percentiles-p99-p9999/) 🔴
- [13-storage-performance-anti-patterns](./13-storage-performance-anti-patterns/) 🔴

**Prerequisites:** Hands-on exposure to at least one layer in 02-14

**Key tool:** fio
