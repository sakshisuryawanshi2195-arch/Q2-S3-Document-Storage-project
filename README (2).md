# Q2 – S3 Document Storage

## Objective

To create an Amazon S3-based document storage system for an organization. The system stores documents in organized folders, configures appropriate bucket access permissions, enables versioning, and demonstrates recovery of an earlier version of a file.

## AWS Service Used

- Amazon S3

## Bucket Details

| Configuration | Details |
|---|---|
| Bucket Name | `q2-document-storage-2026` |
| Region | Europe (Stockholm) – `eu-north-1` |
| Bucket Type | General Purpose |
| Object Ownership | ACLs Disabled |
| Block All Public Access | Enabled |
| Bucket Versioning | Enabled |
| Folder | `documents` |
| Document | `AWS-S3-Document.txt` |

---

# Architecture Diagram

The architecture diagram represents the S3 document storage system, organized folder storage, versioning, multiple file versions, and recovery of an earlier version.

### Architecture Diagram

> **INSERT ARCHITECTURE DIAGRAM HERE**

**File:** `q2-architecture-diagram.png`

---

# Implementation Steps

## 1. Create S3 Bucket

Created an Amazon S3 bucket named `q2-document-storage-2026` in the Europe (Stockholm) region.

- Bucket Type: General Purpose
- Region: `eu-north-1`
- Object Ownership: ACLs Disabled
- Block All Public Access: Enabled

### Screenshot 1 – S3 Bucket Created

> **INSERT SCREENSHOT HERE**

**File:** `q2-bucket-created.png`

---

## 2. Create Organized Folder and Upload Document

Created a folder named `documents` inside the S3 bucket for organized document storage.

The document `AWS-S3-Document.txt` was uploaded inside this folder.

### Folder Structure

```text
q2-document-storage-2026/
└── documents/
    └── AWS-S3-Document.txt
```

### Screenshot 2 – Organized Folder

> **INSERT SCREENSHOT HERE**

**File:** `q2-organized-folder.png`

---

## 3. Configure Bucket Access Permissions

Verified that **Block All Public Access** is enabled for the S3 bucket.

This prevents public access to the bucket and its objects.

### Screenshot 3 – Bucket Access Permissions

> **INSERT SCREENSHOT HERE**

**File:** `q2-block-public-access.png`

---

## 4. Enable Bucket Versioning

Enabled **Bucket Versioning** for the S3 bucket.

Versioning allows multiple versions of the same object to be maintained and allows an earlier version to be recovered when required.

### Screenshot 4 – Versioning Enabled

> **INSERT SCREENSHOT HERE**

**File:** `q2-versioning-enabled.png`

---

## 5. Upload a New Version

Updated the same `AWS-S3-Document.txt` file and uploaded it again using the same file name.

The updated document contained:

```text
AWS S3 Document Storage
Project: Q2
Versioning and document recovery
Version 2 - Updated document
```

Because versioning was enabled, Amazon S3 stored the updated document as a new version while preserving the previous version.

---

## 6. Verify Multiple File Versions

Verified that two versions of `AWS-S3-Document.txt` were available:

- Version 1 – Original document
- Version 2 – Updated document

### Screenshot 5 – Two Versions

> **INSERT SCREENSHOT HERE**

**File:** `q2-two-versions.png`

---

## 7. Recover Earlier Version

Selected the earlier version of `AWS-S3-Document.txt` and downloaded it.

The recovered document contained the original content without the Version 2 update.

This demonstrated successful recovery of an earlier version.

### Screenshot 6 – Earlier Version Recovered

> **INSERT SCREENSHOT HERE**

**File:** `q2-old-version-recovered.png`

---

# Configuration Details

| Configuration | Value |
|---|---|
| AWS Service | Amazon S3 |
| Bucket Name | `q2-document-storage-2026` |
| Region | Europe (Stockholm) |
| Region Code | `eu-north-1` |
| Bucket Type | General Purpose |
| Object Ownership | ACLs Disabled |
| Block All Public Access | Enabled |
| Bucket Versioning | Enabled |
| Folder | `documents` |
| Document | `AWS-S3-Document.txt` |

---

# Testing Results

The following tests were successfully performed:

1. S3 bucket was created successfully.
2. `documents` folder was created for organized storage.
3. `AWS-S3-Document.txt` was uploaded successfully.
4. Block All Public Access was verified.
5. Bucket Versioning was enabled successfully.
6. The same document was updated and uploaded again.
7. Two versions of the document were verified.
8. The earlier version was successfully downloaded and recovered.

---

# Result

**Q2 – S3 Document Storage was successfully implemented using Amazon S3.**

The project demonstrates organized document storage, appropriate bucket access permissions, versioning, and successful recovery of an earlier version of a document.
