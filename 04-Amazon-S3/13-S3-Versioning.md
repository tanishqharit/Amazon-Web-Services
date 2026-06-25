# S3 Versioning

## What is S3 Versioning?

**S3 Versioning** keeps **multiple versions** of an object in the same bucket. If you overwrite or delete a file, the old version is still saved.

---

## How It Works

```
Upload file.csv (Version 1) → Stored
Upload file.csv again (Version 2) → Both Version 1 and 2 are stored
Delete file.csv → A "delete marker" is added, but both versions still exist
```

---

## Key Rules

| Rule | Detail |
|------|--------|
| **Enabled at bucket level** | Applies to all objects in the bucket |
| **Cannot be disabled** | Once enabled, can only be "suspended" (not turned off) |
| **Each version has a unique ID** | You can retrieve any version by ID |
| **Storage cost** | You pay for ALL versions stored |

---

## Why Use Versioning?

1. **Accidental deletion protection** — recover deleted files
2. **Accidental overwrite protection** — go back to a previous version
3. **Audit trail** — see how a file changed over time
4. **Required for replication** — S3 replication needs versioning

---

## MFA Delete

For extra security, you can enable **MFA Delete**:
- Requires multi-factor authentication to **permanently delete** a version
- Prevents accidental or malicious deletion
- Only the root account can enable/disable MFA Delete

---

## Key Takeaway

> Versioning keeps all versions of a file. Once enabled, it can't be fully disabled. It protects against accidental deletes and overwrites. Be aware that all versions cost storage.

---

**Previous:** [S3 Lifecycle Policies](./12-S3-Lifecycle-Policies.md)
**Next:** [S3 Encryption](./14-S3-Encryption.md)
