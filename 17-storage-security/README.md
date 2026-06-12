# 17-storage-security — Storage Security 🟡🔴

Securing data at rest and in transit: dm-crypt/LUKS, filesystem-level encryption, key management (Tang/Clevis), self-encrypting drives, NFS/SMB security, object storage SSE, and immutable/WORM storage.

**Layer(s) in the storage stack:** Cross-cutting — applies at the device, volume, filesystem, network, and object storage layers.

## Subfolders

- [00-fundamentals](./00-fundamentals/) 🟡
- [01-encryption-at-rest-overview](./01-encryption-at-rest-overview/) 🟡
- [02-dm-crypt-and-luks](./02-dm-crypt-and-luks/) 🟡
- [03-luks2-and-argon2](./03-luks2-and-argon2/) 🟡
- [04-filesystem-level-encryption-fscrypt](./04-filesystem-level-encryption-fscrypt/) 🟡
- [05-encrypted-filesystems-ecryptfs](./05-encrypted-filesystems-ecryptfs/) 🟡
- [06-key-management-tang-clevis](./06-key-management-tang-clevis/) 🟡
- [07-tpm-and-secure-boot-for-storage](./07-tpm-and-secure-boot-for-storage/) 🟡
- [08-self-encrypting-drives-sed-opal](./08-self-encrypting-drives-sed-opal/) 🔴
- [09-nfs-security-kerberos](./09-nfs-security-kerberos/) 🔴
- [10-smb-signing-and-encryption](./10-smb-signing-and-encryption/) 🔴
- [11-object-storage-sse-sse-c-sse-kms](./11-object-storage-sse-sse-c-sse-kms/) 🔴
- [12-ransomware-protection-patterns](./12-ransomware-protection-patterns/) 🔴
- [13-storage-audit-and-compliance](./13-storage-audit-and-compliance/) 🔴
- [14-immutable-storage-worm](./14-immutable-storage-worm/) 🔴

**Prerequisites:** 05-filesystems-local, 07-volume-management

**Key tool:** cryptsetup
