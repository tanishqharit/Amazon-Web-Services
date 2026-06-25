# S3 Transfer Acceleration

## What is Transfer Acceleration?

**S3 Transfer Acceleration** speeds up **long-distance uploads** to S3 by routing data through AWS **Edge Locations**.

---

## How It Works

```
Without Acceleration:
User in India → Upload directly to S3 in us-east-1 → Slow (long distance)

With Acceleration:
User in India → Upload to nearest Edge Location (Mumbai) → AWS backbone network → S3 in us-east-1 → Fast!
```

AWS's internal network is much faster than the public internet.

---

## When to Use

- Uploading large files from **far away** from the S3 bucket's Region
- Global users uploading to a central bucket
- When upload speed is critical

---

## Key Facts

- Must be **enabled on the bucket**
- Uses a special endpoint: `bucketname.s3-accelerate.amazonaws.com`
- Extra cost per GB transferred
- Only helps for **long-distance** uploads (not useful if you're already close)

---

## Key Takeaway

> Transfer Acceleration uses Edge Locations to speed up uploads over long distances. Enable it when users upload from far away. It costs extra but significantly improves speed.

---

**Previous:** [S3 Event Notifications](./17-S3-Event-Notifications.md)
**Next:** [S3 Multipart Upload](./19-S3-Multipart-Upload.md)
