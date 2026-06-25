# Semi-Structured Data

## What is Semi-Structured Data?

**Semi-structured data** has some organization, but it **doesn't follow a strict table format**. It uses tags, keys, or markers to separate elements.

Think of it like a notebook with loose headings — there's some structure, but each page can be different.

---

## Examples

### JSON (most common)
```json
{
  "name": "Tanishq",
  "age": 25,
  "skills": ["Python", "SQL", "AWS"],
  "address": {
    "city": "Delhi",
    "country": "India"
  }
}
```

### XML
```xml
<person>
  <name>Tanishq</name>
  <age>25</age>
</person>
```

---

## Characteristics

- ✅ Flexible — each record can have different fields
- ✅ Human-readable (JSON, XML)
- ✅ Great for APIs and web data
- ❌ Harder to query with plain SQL (but possible with tools like Athena)
- ❌ Less efficient for large-scale analytics

---

## Where You Find Semi-Structured Data

- API responses (JSON)
- Log files
- Configuration files
- NoSQL databases (DynamoDB stores JSON-like documents)
- Streaming data (Kinesis records are often JSON)

---

## Key Takeaway

> Semi-structured data has some organization (like JSON or XML) but no fixed schema. It's flexible but less efficient for analytics compared to structured data.

---

**Previous:** [Structured Data](./11-Structured-Data.md)
**Next:** [Unstructured Data](./13-Unstructured-Data.md)
