# IAM Groups

## What is an IAM Group?

An **IAM Group** is a collection of IAM Users. It makes it easier to manage permissions for many users at once.

---

## How Groups Work

Instead of giving permissions to each user individually:

```
❌ Without Groups:
User A → Allow S3 access
User B → Allow S3 access
User C → Allow S3 access
(Tedious! What if you have 100 users?)

✅ With Groups:
Group "DataEngineers" → Allow S3 access
User A → Member of DataEngineers
User B → Member of DataEngineers
User C → Member of DataEngineers
(Change the group policy → all members updated!)
```

---

## Key Rules About Groups

1. A group can contain **many users**
2. A user can belong to **multiple groups**
3. Groups **cannot contain other groups** (no nesting)
4. There is **no default group** — you must create groups yourself
5. Groups are **only for users**, not for services or applications

---

## Common Group Examples

| Group Name | Permissions |
|------------|------------|
| Admins | Full access to everything |
| DataEngineers | S3, Glue, Redshift, Athena access |
| Analysts | Read-only access to Athena and QuickSight |
| Developers | EC2, Lambda, S3 access |

---

## Best Practice

> Always assign permissions to **Groups**, not to individual Users. This makes it much easier to manage permissions as your team grows.

---

## Key Takeaway

> IAM Groups let you manage permissions for multiple users at once. Always use Groups instead of assigning permissions to individual users.

---

**Previous:** [IAM Users](./10-IAM-Users.md)
**Next:** [IAM Roles](./12-IAM-Roles.md)
