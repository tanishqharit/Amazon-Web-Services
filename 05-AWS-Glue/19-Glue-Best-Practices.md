# Glue Best Practices

## Performance

1. **Use Parquet/ORC output** — columnar formats for faster downstream queries
2. **Partition output data** — by date, region, etc. for faster queries
3. **Right-size workers** — G.1X for standard, G.2X for memory-heavy jobs
4. **Enable auto-scaling** — let Glue adjust workers based on load
5. **Use push-down predicates** — filter data at the source, not after loading
6. **Avoid small files** — coalesce output to ~128 MB-1 GB per file

## Cost

1. **Use Job Bookmarks** — avoid reprocessing data
2. **Set timeouts** — kill runaway jobs before they cost too much
3. **Use Python Shell** for small tasks — much cheaper than Spark
4. **Monitor DPU usage** — scale down when processing is small
5. **Use Glue 4.0** — faster startup and better performance

## Data Quality

1. **Enable Glue Data Quality rules** on critical datasets
2. **Profile data with DataBrew** before building ETL logic
3. **Use Schema Registry** for streaming to enforce schemas

---

## Exam Tips for Glue

| Question Pattern | Answer |
|-----------------|--------|
| "Discover schema automatically" | Crawlers |
| "Central metadata store" | Data Catalog |
| "Process only new data" | Job Bookmarks |
| "Visual ETL without code" | Glue Studio |
| "Data cleaning for analysts" | DataBrew |
| "Enforce streaming schema" | Schema Registry |
| "Small task, API call" | Python Shell job |
| "Large-scale ETL" | Spark job |
| "Glue can't access S3 from VPC" | S3 VPC Gateway Endpoint |

---

## Key Takeaway

> Master Glue = master Domain 1 of the exam. Know when to use each component (Crawlers, Catalog, ETL, Bookmarks, Studio, DataBrew, Schema Registry). Always think Parquet output + partitioning + bookmarks for optimal pipelines.

---

**Previous:** [Glue Elastic Views](./18-Glue-Elastic-Views.md)
**Next:** [Section 06 — Amazon Kinesis](../06-Amazon-Kinesis/01-What-is-Amazon-Kinesis.md)
