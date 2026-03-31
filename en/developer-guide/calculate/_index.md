---
title: "Aspose.Cells Cloud Web API – Calculate SUM, COUNT, AVERAGE, MIN, MAX & Basic Math Operations"
second_title: "Document"
ArticleTitle: "Boost Your Data Skills: Learn Key Excel Calculations – Add, Subtract, Multiply, Divide & More"
linktitle: "Calculate"
type: docs
url: /calculate/
keywords: "Aspose.Cells, Excel calculation API, SUM, COUNT, AVERAGE, MIN, MAX, REST"
description: "Learn how to use Aspose.Cells Cloud REST API to calculate SUM, COUNT, AVERAGE, MIN, MAX and basic math operations on Excel worksheets. Includes request examples, responses, and error handling."
weight: 20
---

Automatically perform calculations such as **SUM**, **COUNT**, **AVERAGE**, **MIN**, and **MAX** on Excel worksheets via the Aspose.Cells Cloud REST API—no manual filtering or local spreadsheet software required. The API is supported in **Aspose.Cells Cloud v3.0**, uses standard authentication (OAuth 2.0 or JWT), returns results in JSON format, and provides clear error codes for invalid ranges or authentication issues. For detailed request syntax, see the official REST API reference.

- **[Calculate by Cell Color](https://docs.aspose.cloud/cells/aggregate-cells-by-color/)** – Retrieve totals grouped by background or font color in a single request.  
- **[Spreadsheet Quick Calculate](https://docs.aspose.cloud/cells/math-calculate/)** – Compute SUM, COUNT, AVERAGE, MIN, MAX (and basic arithmetic) across any range instantly.

| Formula | Description | API endpoint |
|---------|-------------|--------------|
| **SUM** | Adds all numeric values in the specified range. | `POST /cells/{file}/worksheets/{sheet}/calculate/sum` |
| **COUNT** | Counts numeric cells in the range. | `POST /cells/{file}/worksheets/{sheet}/calculate/count` |
| **AVERAGE** | Calculates the mean of numeric cells. | `POST /cells/{file}/worksheets/{sheet}/calculate/average` |
| **MIN** | Returns the smallest numeric value. | `POST /cells/{file}/worksheets/{sheet}/calculate/min` |
| **MAX** | Returns the largest numeric value. | `POST /cells/{file}/worksheets/{sheet}/calculate/max` |

For the complete API specification, error‑handling details, and code samples, visit the [Aspose.Cells Cloud REST API reference](https://api.aspose.cloud/cells/).