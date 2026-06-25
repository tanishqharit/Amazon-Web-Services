# S3 Lifecycle Policies

## What are Lifecycle Policies?

**Lifecycle policies** are rules that automatically move or delete objects based on their **age**. This helps save money without manual work.

---

## How It Works

You define rules like:
```
After 30 days  → Move from Standard to Standard-IA
After 90 days  → Move to Glacier Flexible Retrieval
After 365 days → Move to Deep Archive
After 2555 days (7 years) → Delete permanently
```

AWS applies these rules **automatically** every day.

---

## Two Types of Actions

### 1. Transition Actions
Move objects to a cheaper storage class.

```
Standard → Standard-IA → Glacier → Deep Archive
```

### 2. Expiration Actions
Delete objects after a certain time.

```
After 365 days → Delete the object
After 30 days → Delete old versions (if versioning is on)
```

---

## Example Lifecycle Policy

| Rule | Action |
|------|--------|
| Current objects after 30 days | Transition to Standard-IA |
| Current objects after 90 days | Transition to Glacier |
| Current objects after 365 days | Delete |
| Incomplete multipart uploads after 7 days | Delete |

---

## For the Exam

- "Automatically move data to cheaper storage" → **Lifecycle Policy**
- "Delete old data after X days" → **Lifecycle Expiration**
- "Clean up incomplete uploads" → **Lifecycle Policy on multipart uploads**

---

## Key Takeaway

> Lifecycle policies automatically move or delete objects based on age. They save money by transitioning data from hot to cold storage over time. Set them up and forget — AWS handles the rest.

---

**Previous:** [S3 Glacier Deep Archive](./11-S3-Glacier-Deep-Archive.md)
**Next:** [S3 Versioning](./13-S3-Versioning.md)
