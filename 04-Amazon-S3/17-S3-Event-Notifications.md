# S3 Event Notifications

## What are S3 Event Notifications?

S3 can **automatically trigger actions** when something happens in a bucket — like a file being uploaded, deleted, or restored.

---

## How It Works

```
File uploaded to S3 → S3 Event → Triggers Lambda/SQS/SNS/EventBridge
```

---

## Events You Can Listen For

| Event | When it fires |
|-------|---------------|
| `s3:ObjectCreated:*` | Any object is uploaded |
| `s3:ObjectCreated:Put` | Object uploaded via PUT |
| `s3:ObjectRemoved:*` | Any object is deleted |
| `s3:ObjectRestore:Completed` | Glacier restore is done |

---

## Where Can Events Go?

| Destination | Use Case |
|-------------|----------|
| **AWS Lambda** | Run code when a file arrives |
| **Amazon SQS** | Queue the event for processing |
| **Amazon SNS** | Send notifications |
| **Amazon EventBridge** | Route to many services (most flexible) |

---

## Data Engineering Example

```
CSV uploaded to s3://raw-data/sales/
    → S3 Event Notification
    → Triggers Lambda function
    → Lambda starts a Glue ETL job
    → Glue converts CSV to Parquet
    → Saves to s3://processed-data/sales/
```

---

## EventBridge vs Direct Notifications

| Feature | Direct (Lambda/SQS/SNS) | EventBridge |
|---------|------------------------|-------------|
| Destinations | 3 services only | 18+ services |
| Filtering | Basic prefix/suffix | Advanced pattern matching |
| Recommended | Simple use cases | Complex workflows |

---

## Key Takeaway

> S3 Event Notifications trigger actions when files are uploaded, deleted, or restored. Use Lambda for code execution, SQS for queuing, SNS for alerts, or EventBridge for complex routing. This is key for building event-driven data pipelines.

---

**Previous:** [S3 Access Control Lists](./16-S3-Access-Control-Lists.md)
**Next:** [S3 Transfer Acceleration](./18-S3-Transfer-Acceleration.md)
