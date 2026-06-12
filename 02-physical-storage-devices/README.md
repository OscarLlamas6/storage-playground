# 02-physical-storage-devices — Physical Storage Devices 🟢🟡💾

The physical media that actually stores bits: HDD mechanics, NAND flash and SSD internals, NVMe, PCIe, persistent memory, and emerging device-level technologies like ZNS and SMR.

**Layer(s) in the storage stack:** Physical devices — the bottom of the storage stack.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟢💾
- [01-hdd-mechanics-platters-heads-sectors](./01-hdd-mechanics-platters-heads-sectors/) 🟢💾
- [02-hdd-seek-time-rotational-latency](./02-hdd-seek-time-rotational-latency/) 🟢💾
- [03-ssd-nand-flash-cells-slc-mlc-tlc-qlc](./03-ssd-nand-flash-cells-slc-mlc-tlc-qlc/) 🟢💾
- [04-ssd-wear-leveling-and-gc](./04-ssd-wear-leveling-and-gc/) 🟢💾
- [05-ssd-write-amplification](./05-ssd-write-amplification/) 🟢💾
- [06-nvme-protocol-and-queues](./06-nvme-protocol-and-queues/) 🟢💾
- [07-nvme-vs-sata-vs-sas](./07-nvme-vs-sata-vs-sas/) 🟢💾
- [08-pcie-generations-and-bandwidth](./08-pcie-generations-and-bandwidth/) 🟡💾
- [09-smr-shingled-magnetic-recording](./09-smr-shingled-magnetic-recording/) 🟡💾
- [10-zns-zoned-namespaces](./10-zns-zoned-namespaces/) 🟡💾
- [11-persistent-memory-pmem-optane](./11-persistent-memory-pmem-optane/) 🟡💾
- [12-tape-storage-still-relevant](./12-tape-storage-still-relevant/) 🟡💾
- [13-storage-class-memory](./13-storage-class-memory/) 🟡💾
- [14-raid-hardware-controllers](./14-raid-hardware-controllers/) 🟡💾

**Prerequisites:** 01-fundamentals

**Key tool:** smartctl / nvme-cli
