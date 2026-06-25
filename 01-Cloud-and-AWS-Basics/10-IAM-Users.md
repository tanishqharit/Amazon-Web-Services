# IAM Users

## What is an IAM User?

An **IAM User** is an identity that represents **a person or application** that interacts with AWS.

Each IAM User has:
- A **username**
- **Credentials** (password and/or access keys)
- **Permissions** (what they can do)

---

## Root User vs IAM User

When you first create an AWS account, you get a **Root User**.

| Feature | Root User | IAM User |
|---------|-----------|----------|
| Created when | Account is created | You create manually |
| Access level | **Full access to everything** | Only what you allow |
| Should you use daily? | ❌ Never | ✅ Yes |
| Can be restricted? | No | Yes |

**Important Rule:** Never use the Root User for daily tasks. Create an IAM User for yourself.

---

## Types of Credentials

IAM Users can have two types of credentials:

### 1. Console Password
- Used to log in to the AWS Console (web browser)
- For **humans** who click through the UI

### 2. Access Keys
- Used for CLI and SDK access
- An **Access Key ID** + **Secret Access Key** pair
- For **programmatic access** (code, scripts)

---

## Best Practices

1. **One user per person** — don't share accounts
2. **Never use Root User** for daily work
3. **Enable MFA** (Multi-Factor Authentication) for extra security
4. **Rotate access keys** regularly

---

## Key Takeaway

> An IAM User represents a person or app. Always use IAM Users instead of the Root User. Users can have console passwords (for web) or access keys (for code).

---

**Previous:** [What is IAM](./09-What-is-IAM.md)
**Next:** [IAM Groups](./11-IAM-Groups.md)
