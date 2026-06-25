# AWS CLI Basics

## What is the AWS CLI?

The **AWS CLI (Command Line Interface)** is a tool that lets you manage AWS services by **typing commands** in your terminal.

Instead of clicking buttons in the Console, you type commands like:

```bash
aws s3 ls
```

This lists all your S3 buckets.

---

## Why Use the CLI?

| Console (Web) | CLI (Commands) |
|---------------|----------------|
| Click buttons | Type commands |
| Good for learning | Good for automation |
| Slow for repetitive tasks | Fast for repetitive tasks |
| Visual | Scriptable |

---

## Installing the CLI

```bash
# macOS
brew install awscli

# Or download from:
# https://aws.amazon.com/cli/
```

Verify it's installed:

```bash
aws --version
```

---

## Setting Up the CLI

You need to configure it with your credentials:

```bash
aws configure
```

It will ask for:
1. **Access Key ID** — from your IAM User
2. **Secret Access Key** — from your IAM User
3. **Default Region** — e.g., `us-east-1`
4. **Output format** — `json` (recommended)

---

## Common CLI Commands for Data Engineers

```bash
# List S3 buckets
aws s3 ls

# Copy file to S3
aws s3 cp myfile.csv s3://my-bucket/

# List Glue databases
aws glue get-databases

# Describe a Redshift cluster
aws redshift describe-clusters
```

---

## Key Takeaway

> The AWS CLI lets you manage AWS by typing commands. It's great for automation and scripting. For learning, use the Console first, then gradually use the CLI.

---

**Previous:** [Principle of Least Privilege](./14-Principle-of-Least-Privilege.md)
**Next:** [AWS SDKs](./16-AWS-SDKs.md)
