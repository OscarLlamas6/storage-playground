# 10-object-storage — Object Storage 🟡🔴☁️

The key-value/HTTP object storage model: the S3 API as the de facto standard, self-hosted alternatives (MinIO, Ceph RGW, Swift, SeaweedFS, Garage), and concerns like erasure coding, tiering, and security.

**Layer(s) in the storage stack:** Object storage — an HTTP API layer, often backed by its own distributed storage engine.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡☁️
- [01-object-storage-model-key-value](./01-object-storage-model-key-value/) 🟡☁️
- [02-s3-api-the-de-facto-standard](./02-s3-api-the-de-facto-standard/) 🟡☁️
- [03-s3-consistency-model](./03-s3-consistency-model/) 🟡☁️
- [04-s3-multipart-uploads](./04-s3-multipart-uploads/) 🟡☁️
- [05-s3-versioning-and-lifecycle](./05-s3-versioning-and-lifecycle/) 🟡☁️
- [06-minio-self-hosted-s3](./06-minio-self-hosted-s3/) 🟡☁️
- [07-ceph-rados-object-storage](./07-ceph-rados-object-storage/) 🟡☁️
- [08-openstack-swift](./08-openstack-swift/) 🔴☁️
- [09-seaweedfs](./09-seaweedfs/) 🔴☁️
- [10-garage-distributed-object-store](./10-garage-distributed-object-store/) 🔴☁️
- [11-object-storage-erasure-coding](./11-object-storage-erasure-coding/) 🔴☁️
- [12-object-storage-tiering](./12-object-storage-tiering/) 🔴☁️
- [13-content-addressed-storage](./13-content-addressed-storage/) 🔴☁️
- [14-object-storage-security](./14-object-storage-security/) 🔴☁️

**Prerequisites:** 01-fundamentals

**Key tool:** aws s3 / mc (MinIO client)
