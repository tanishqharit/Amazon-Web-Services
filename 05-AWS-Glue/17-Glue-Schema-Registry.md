# Glue Schema Registry

## What is the Schema Registry?

The **Glue Schema Registry** is a central place to store, validate, and manage **schemas for streaming data** (Avro, JSON Schema, Protobuf).

---

## Why It's Needed

In streaming, producers send data continuously. Without schema enforcement:
- A producer might change the data format without telling consumers
- Consumers break because they expect a different schema
- Bad data enters the pipeline

Schema Registry **enforces a contract** between producers and consumers.

---

## How It Works

```
Producer → Registers schema in Registry → Sends data
Consumer → Reads schema from Registry → Knows how to read data
```

If a producer tries to send data that doesn't match the schema → **rejected**.

---

## Schema Evolution

Schemas can change over time (add columns, change types). The Registry supports:

| Mode | What's allowed |
|------|---------------|
| **None** | No changes allowed |
| **Forward** | New schema can read old data |
| **Backward** | Old schema can read new data |
| **Full** | Both forward and backward |

---

## Supported Formats

- Apache Avro
- JSON Schema
- Protocol Buffers (Protobuf)

---

## Integration

Works with:
- Amazon Kinesis Data Streams
- Amazon MSK (Kafka)
- AWS Lambda
- AWS Glue ETL jobs

---

## Key Takeaway

> The Glue Schema Registry manages schemas for streaming data. It ensures producers and consumers agree on data format. Supports schema evolution so changes don't break pipelines.

---

**Previous:** [Glue Data Quality](./16-Glue-Data-Quality.md)
**Next:** [Glue Elastic Views](./18-Glue-Elastic-Views.md)
