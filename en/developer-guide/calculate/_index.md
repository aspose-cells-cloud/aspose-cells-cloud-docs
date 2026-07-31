---
title: "Aspose.Cells Cloud Web API – Calculate SUM, COUNT, AVERAGE, MIN, MAX & Basic Math Operations"
second_title: "Document"
ArticleTitle: "Boost Your Data Skills: Learn Key Excel Calculations – Add, Subtract, Multiply, Divide & More"
linktitle: "Calculate"
type: docs
url: /calculate/
keywords: "Aspose.Cells Cloud, Excel calculation API, SUM, COUNT, AVERAGE, MIN, MAX, basic math operations, REST API, spreadsheet calculations"
description: "Learn how to use Aspose.Cells Cloud REST API to calculate SUM, COUNT, AVERAGE, MIN, MAX and basic arithmetic operations on Excel worksheets. Includes request syntax, sample code, responses, and error handling."
weight: 20
---

Automatically perform calculations such as **SUM**, **COUNT**, **AVERAGE**, **MIN**, and **MAX** on Excel worksheets via the Aspose.Cells Cloud REST API—no manual filtering or local spreadsheet software required. The API is supported in **Aspose.Cells Cloud**, uses standard authentication (OAuth 2.0 or JWT), returns results in JSON format, and provides clear error codes for invalid ranges or authentication issues. For detailed request syntax, see the official REST API reference.

- **[Calculate by Cell Color](https://docs.aspose.cloud/cells/aggregate-cells-by-color/)** – Retrieve totals grouped by background or font color in a single request.  
- **[Spreadsheet Quick Calculate](https://docs.aspose.cloud/cells/math-calculate/)** – Compute SUM, COUNT, AVERAGE, MIN, MAX (and basic arithmetic) across any range instantly.  

For the complete API specification, error‑handling details, and additional code samples, visit the [Aspose.Cells Cloud REST API reference](https://api.aspose.cloud/cells/).

**API reference** – The core endpoint for performing calculations is:

| Method | Endpoint | Required Headers | Key Parameters |
|--------|----------|------------------|----------------|
| POST   | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/calculate` | `Authorization: Bearer {access_token}`<br>`Accept: application/json` | `range` – Excel range to calculate (e.g., `A1:D10`)<br>`functions` – Comma‑separated list of functions to apply (`SUM,COUNT,AVERAGE,MIN,MAX`)<br>`includeBasicMath` – `true` to enable addition, subtraction, multiplication, division |

**Sample request (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/calculate" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{
           "range": "A1:D10",
           "functions": "SUM,COUNT,AVERAGE,MIN,MAX",
           "includeBasicMath": true
         }'
```

**Typical successful response**

```json
{
  "SUM": 452.75,
  "COUNT": 20,
  "AVERAGE": 22.6375,
  "MIN": 3.5,
  "MAX": 98.0,
  "BASIC_MATH": {
    "ADD": 1234.5,
    "SUBTRACT": 567.8,
    "MULTIPLY": 34567.0,
    "DIVIDE": 12.34
  }
}
```

**Possible status codes**

- `200 OK` – Calculation succeeded.  
- `400 Bad Request` – Invalid range or malformed parameters.  
- `401 Unauthorized` – Missing or invalid authentication token.  
- `404 Not Found` – Specified file or worksheet does not exist.  
- `500 Internal Server Error` – Unexpected server error.

For more examples and advanced scenarios, see the dedicated **Calculate** endpoint documentation: [Calculate endpoint details](/calculate/).