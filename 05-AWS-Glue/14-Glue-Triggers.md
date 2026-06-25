# Glue Triggers

## What is a Trigger?

A **Glue Trigger** starts a Glue job or crawler. It defines **when** something should run.

---

## Types of Triggers

| Type | When it fires |
|------|--------------|
| **Schedule** | At a specific time (cron expression) |
| **On-demand** | When you manually start it |
| **Conditional** | When another job succeeds or fails |
| **EventBridge** | When an event occurs (e.g., S3 file upload) |

---

## Schedule Trigger Example

```
Run every day at 2 AM UTC: cron(0 2 * * ? *)
Run every hour: cron(0 * * * ? *)
Run every Monday: cron(0 0 ? * MON *)
```

---

## Conditional Trigger Example

```
Job A completes successfully → Trigger starts Job B
Job A fails → Trigger sends notification
```

---

## Key Takeaway

> Triggers control when Glue jobs and crawlers run. Use schedules for regular processing, conditional triggers for job dependencies, and EventBridge for event-driven pipelines.

---

**Previous:** [Glue Workflows](./13-Glue-Workflows.md)
**Next:** [Glue Connections](./15-Glue-Connections.md)
