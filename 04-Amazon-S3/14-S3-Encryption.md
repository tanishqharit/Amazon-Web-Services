# S3 Encryption

## Why Encrypt Data?

Encryption converts data into unreadable code. Even if someone steals the file, they can't read it without the encryption key.

AWS provides encryption for data **at rest** (stored) and **in transit** (moving).

---

## Encryption at Rest (4 options)

### 1. SSE-S3 (Server-Side Encryption with S3-managed keys)
- **Default** encryption for all new buckets
- AWS manages the keys completely
- You do nothing — it just works

### 2. SSE-KMS (Server-Side Encryption with KMS keys)
- You use **AWS KMS** to manage keys
- You can control who has access to the key
- Provides **audit trail** (CloudTrail logs key usage)
- ⚠️ KMS has API rate limits (can throttle at high volume)

### 3. SSE-C (Server-Side Encryption with Customer-provided keys)
- YOU provide the encryption key with every request
- AWS doesn't store your key
- Must use HTTPS
- Rarely used

### 4. Client-Side Encryption
- YOU encrypt data before uploading to S3
- AWS never sees unencrypted data
- You manage everything

---

## Comparison

| Method | Who manages keys? | Audit trail? | Exam frequency |
|--------|-------------------|-------------|----------------|
| SSE-S3 | AWS | No | Medium |
| SSE-KMS | You (via KMS) | Yes (CloudTrail) | ⭐ High |
| SSE-C | You (fully) | No | Low |
| Client-Side | You (fully) | No | Low |

---

## Encryption in Transit

- S3 supports **HTTPS** (TLS/SSL) for data in transit
- You can enforce HTTPS-only via a bucket policy
- Always use HTTPS for sensitive data

---

## For the Exam

- Default encryption → **SSE-S3**
- Need audit trail / key control → **SSE-KMS**
- "Customer manages keys" → **SSE-C** or **Client-Side**

---

## Key Takeaway

> S3 encrypts all data by default using SSE-S3. For more control and audit trails, use SSE-KMS. The exam heavily tests SSE-KMS because of its integration with CloudTrail.

---

**Previous:** [S3 Versioning](./13-S3-Versioning.md)
**Next:** [S3 Bucket Policies](./15-S3-Bucket-Policies.md)
