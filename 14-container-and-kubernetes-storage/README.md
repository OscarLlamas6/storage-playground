# 14-container-and-kubernetes-storage — Container & Kubernetes Storage 🟡🔴☁️

How containers and Kubernetes consume storage: Docker volumes/bind mounts, the CSI spec, PVs/PVCs/StorageClasses, snapshots/cloning, and local vs shared (RWX) storage patterns.

**Layer(s) in the storage stack:** Orchestration-level storage abstractions, sitting on top of cloud/distributed/local storage.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡☁️
- [01-docker-volumes](./01-docker-volumes/) 🟡☁️
- [02-docker-bind-mounts](./02-docker-bind-mounts/) 🟡☁️
- [03-docker-tmpfs](./03-docker-tmpfs/) 🟡☁️
- [04-csi-container-storage-interface](./04-csi-container-storage-interface/) 🟡☁️
- [05-kubernetes-persistent-volumes](./05-kubernetes-persistent-volumes/) 🟡☁️
- [06-kubernetes-persistent-volume-claims](./06-kubernetes-persistent-volume-claims/) 🟡☁️
- [07-kubernetes-storage-classes](./07-kubernetes-storage-classes/) 🟡☁️
- [08-kubernetes-statefulsets-and-storage](./08-kubernetes-statefulsets-and-storage/) 🔴☁️
- [09-volume-snapshots-k8s](./09-volume-snapshots-k8s/) 🔴☁️
- [10-volume-cloning](./10-volume-cloning/) 🔴☁️
- [11-local-storage-in-k8s](./11-local-storage-in-k8s/) 🔴☁️
- [12-shared-storage-rwx-in-k8s](./12-shared-storage-rwx-in-k8s/) 🔴☁️
- [13-csi-driver-development](./13-csi-driver-development/) 🔴☁️
- [14-storage-capacity-tracking](./14-storage-capacity-tracking/) 🔴☁️

**Prerequisites:** 05-filesystems-local, 13-cloud-storage

**Key tool:** kubectl
