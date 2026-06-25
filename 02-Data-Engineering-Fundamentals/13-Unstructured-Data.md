# Unstructured Data

## What is Unstructured Data?

**Unstructured data** has **no predefined format or schema**. It cannot be organized into rows and columns.

It's the most common type of data — about **80% of all data** generated is unstructured.

---

## Examples

- 📷 Images and photos
- 🎥 Videos
- 📧 Emails
- 📄 PDFs and Word documents
- 🎵 Audio files
- 💬 Social media posts
- 📝 Free-form text

---

## Characteristics

- ❌ Cannot be stored in traditional databases (no rows/columns)
- ❌ Very hard to search and query directly
- ✅ Stored as files (often in S3)
- ✅ Can be processed with AI/ML to extract meaning

---

## How Unstructured Data is Handled on AWS

| Task | Service |
|------|---------|
| Store unstructured files | **Amazon S3** |
| Search through text | **Amazon OpenSearch** |
| Detect sensitive data (PII) | **Amazon Macie** |
| Analyze images | Amazon Rekognition (ML, not in exam) |

---

## For the Exam

- Unstructured data is usually stored in **S3**
- You often need to **convert unstructured to structured** for analytics
- Example: Parse log files (text) into a structured table

---

## Key Takeaway

> Unstructured data has no fixed format — images, videos, emails, PDFs. It makes up 80% of all data. On AWS, it's stored in S3 and sometimes processed into structured formats for analysis.

---

**Previous:** [Semi-Structured Data](./12-Semi-Structured-Data.md)
**Next:** [What is a Data Lake](./14-What-is-a-Data-Lake.md)
