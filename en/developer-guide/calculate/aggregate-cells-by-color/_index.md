---
url: /aggregate-cells-by-color/
title: "Aggregate Excel Cells by Color | Aspose.Cells Cloud API"
date: 2024-05-10
lastmod: 2024-05-10
description: "Perform color-based aggregation—sum, count, average, min, max—on Excel ranges using Aspose.Cells Cloud API v4.0. Secure, scalable, and SDK-ready."
keywords: ["Aspose.Cells Cloud", "Excel API", "color aggregation", "sum by color", "count by color", "aggregate cells", "background color", "font color"]
canonical: "https://docs.aspose.cloud/cells/aggregate-cells-by-color/"
weight: 100
---

# Aggregate Excel Cells by Color

The **Aggregate by Color API** enables efficient, color-driven data analysis in Excel workbooks. It performs calculations—such as *sum*, *count*, *average*, *min*, and *max*—on cells grouped by either their **background (fill)** or **font** color, without requiring manual filtering or custom parsing logic.

> 💡 **Use Case Example**: In a sales report where Q1, Q2, and Q3 are highlighted in red, green, and blue, this API instantly computes totals, averages, and extremum values per quarter.

---

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

> ✅ **Authenticated**: Requires JWT token via `Authorization: Bearer <access_token>`.  
> 🔒 **Secure**: All requests use HTTPS. External links include `rel="noopener noreferrer"` for tabnabbing protection.

---

## Request Parameters

| Parameter      | Type   | Location   | Required | Description |
|:---------------|:-------|:-----------|:---------|:------------|
| `Spreadsheet`  | File   | FormData   | Yes      | Excel workbook to process. Max size: **100 MB**. |
| `Worksheet`    | String | Query      | No       | Name of the worksheet containing the target range. |
| `Range`        | String | Query      | No       | A1-style range (e.g., `A1:B10`). Defaults to entire sheet if omitted. |
| `Operation`    | String | Query      | No       | Aggregation method: `Sum`, `Count`, `Average`, `Min`, `Max`. Default: `Sum`. |
| `ColorPosition`| String | Query      | No       | Color basis: `Background` (fill) or `Font`. Default: `Background`. |
| `Region`       | String | Query      | Yes      | Locale/regional setting (e.g., `en-US`, `fr-FR`). Affects number/date parsing and formatting. |
| `Password`     | String | Query      | No       | Password for protected workbooks. Omit if unprotected. |

### Enumerations

#### `Operation`
| Value      | Description |
|:-----------|:------------|
| `Sum`      | Total of cell values |
| `Count`    | Number of cells with matching color |
| `Average`  | Mean value |
| `Min`      | Smallest value |
| `Max`      | Largest value |

#### `ColorPosition`
| Value      | Description |
|:-----------|:------------|
| `Background`| Uses cell fill color |
| `Font`      | Uses font color |

---

## Example Request

### cURL Example (with best practices)

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background&Region=en-US" \
  -H "Authorization: Bearer <access_token>" \
  -H "Content-Type: multipart/form-data" \
  -F "Spreadsheet=@./example.xlsx"
```

> ⚠️ **Notes**  
> - Replace `example.xlsx` with your local file (≤100 MB).  
> - Use `Region` values matching your data locale (e.g., `en-US`, `de-DE`, `ja-JP`).  
> - For protected files, add `&Password=your_password`.

---

## Response Schema

### `AggregateResultByColorResponse`

| Field             | Type                    | Description |
|:------------------|:------------------------|:------------|
| `Code`            | Integer                 | HTTP status code (e.g., `200`). |
| `Status`          | String                  | Human-readable status (e.g., `"OK"`). |
| `AggregateResults`| Array of `AggregateResultByColor` | List of results grouped by color. |

### `AggregateResultByColor`

| Field     | Type    | Description |
|:----------|:--------|:------------|
| `Color`   | String  | Hex color code (e.g., `"#FF0000"`). |
| `Count`   | Integer | Number of matching cells. |
| `Sum`     | Number  | Total value sum. |
| `Average` | Number  | Mean value. |
| `Min`     | Number  | Minimum value. |
| `Max`     | Number  | Maximum value. |

### Example Response

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.81,
      "Min": 5.00,
      "Max": 80.00
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.00,
      "Average": 30.00,
      "Min": 10.00,
      "Max": 50.00
    }
  ]
}
```

---

## HTTP Status Codes

| Code | Meaning               | Resolution |
|:-----|:----------------------|:-----------|
| 200  | OK                    | Success. Results in response body. |
| 400  | Bad Request           | Invalid parameter (e.g., malformed range, unsupported operation). |
| 401  | Unauthorized          | Missing/invalid JWT token or workbook password. |
| 413  | Payload Too Large     | File exceeds 100 MB limit. Use cloud storage for larger files. |
| 404  | Not Found             | Worksheet or range not found in workbook. |
| 500  | Internal Server Error | Server-side processing failure (e.g., corrupted file). |

---

## Use Cases

### ✅ Ideal Applications
- **Sales Dashboards**: Sum Q1/Q2/Q3 performance by colored sections.
- **Budget Tracking**: Count expenses by category (e.g., red = overbudget).
- **Inventory Reports**: Find max/min stock levels per color-coded risk tier.
- **Survey Analysis**: Average scores grouped by response tone (font color).

> 📊 **Why Color-Based Aggregation?**  
> Eliminates manual filtering, reduces error risk, and surfaces insights instantly—no formulas or pivot tables needed.

---

## Implementation Guides

### SDK Examples

Use our [Aspose.Cells Cloud SDKs](https://github.com/aspose-cells-cloud) to simplify integration. Below are concise examples for key languages:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go">}}
{{<tab tabNum="1">}}
```csharp
// C# (Aspose.Cells.Cloud.SDK)
var cellsApi = new CellsApi("client_id", "client_secret");
var response = cellsApi.AggregateCellsByColor(
    "example.xlsx",
    worksheet: "Sheet1",
    range: "A1:B10",
    operation: "Sum",
    colorPosition: "Background",
    region: "en-US"
);
```
{{</tab}}  
{{<tab tabNum="2">}}
```java
// Java (Aspose.Cells.Cloud.SDK)
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
AggregateResultByColorResponse response = cellsApi.aggregateCellsByColor(
    "example.xlsx",
    "Sheet1",
    "A1:B10",
    "Sum",
    "Background",
    "en-US"
);
```
{{</tab}}  
{{<tab tabNum="3">}}
```php
// PHP (Aspose.Cells.Cloud.SDK)
$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->aggregateCellsByColor(
    "example.xlsx",
    "Sheet1",
    "A1:B10",
    "Sum",
    "Background",
    "en-US"
);
```
{{</tab}}  
{{<tab tabNum="4">}}
```ruby
# Ruby (Aspose.Cells.Cloud.SDK)
cells_api = AsposeCellsCloud::CellsApi.new('client_id', 'client_secret')
response = cells_api.aggregate_cells_by_color(
  'example.xlsx',
  worksheet: 'Sheet1',
  range: 'A1:B10',
  operation: 'Sum',
  color_position: 'Background',
  region: 'en-US'
)
```
{{</tab}}  
{{<tab tabNum="5">}}
```typescript
// Node.js (Aspose.Cells.Cloud.SDK)
const cellsApi = new CellsApi("client_id", "client_secret");
const response = await cellsApi.aggregateCellsByColor(
  "example.xlsx",
  { worksheet: "Sheet1", range: "A1:B10", operation: "Sum", colorPosition: "Background", region: "en-US" }
);
```
{{</tab}}  
{{<tab tabNum="6">}}
```python
# Python (Aspose.Cells.Cloud.SDK)
api = CellsApi("client_id", "client_secret")
response = api.aggregate_cells_by_color(
    "example.xlsx",
    worksheet="Sheet1",
    range="A1:B10",
    operation="Sum",
    color_position="Background",
    region="en-US"
)
```
{{</tab}}  
{{<tab tabNum="7">}}
```perl
# Perl (Aspose.Cells.Cloud.SDK)
my $cells_api = AsposeCellsCloud::CellsApi->new(
    -sid => "client_id",
    -secret => "client_secret"
);
my $response = $cells_api->aggregate_cells_by_color(
    "example.xlsx",
    Worksheet => "Sheet1",
    Range => "A1:B10",
    Operation => "Sum",
    ColorPosition => "Background",
    Region => "en-US"
);
```
{{</tab}}  
{{<tab tabNum="8">}}
```go
// Go (Aspose.Cells.Cloud.SDK)
cellsAPI, _, _ := NewCellsApiUsingCredentials("client_id", "client_secret")
response, _, err := cellsAPI.AggregateCellsByColor(
    context.Background(),
    "example.xlsx",
    &cellsAPI.AggregateCellsByColorOpts{
        Worksheet:     optional.NewString("Sheet1"),
        Range:         optional.NewString("A1:B10"),
        Operation:     optional.NewString("Sum"),
        ColorPosition: optional.NewString("Background"),
        Region:        optional.NewString("en-US"),
    },
)
```
{{</tab}}  
{{</tabs>}}

> 🔗 **Get SDKs**: [GitHub Repository](https://github.com/aspose-cells-cloud)  
> 🔗 **API Reference**: [Aspose.Cells Cloud API v4.0](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor)

---

## Best Practices

### ✅ Do
- Use `Region` matching your data locale to avoid parsing errors.
- Upload large files (>100 MB) to cloud storage first, then use `Path` parameter (contact support for details).
- Include `Password` for protected files to avoid `401` errors.

### ❌ Don’t
- Use generic file paths like `/path/to/workbook.xlsx` in examples (copy-paste errors).
- Omit `Region` (causes inconsistent number/date handling).
- Rely on `keywords` for SEO—focus on semantic content instead.

---

## Visual Guide

> 📸 **Image 1**: Excel range `A1:B10` with color-coded categories (red = Q1, green = Q2, blue = Q3).  
> *Alt text*: "Sample Excel range with color-coded data for aggregation (Q1 in red, Q2 in green, Q3 in blue)."

> 📸 **Image 2**: API request/response preview in Postman showing `#FF0000` results.  
> *Alt text*: "Postman request for summing red cells (Q1) with response showing count=12, sum=345.67."

> 📸 **Image 3**: Flowchart: *“How Aggregate by Color Works”*  
> 1. Upload workbook → 2. Specify range/color → 3. Select operation → 4. Return grouped results.

*(Add these images in `/images/aggregate-by-color-*.png` for optimal UX.)*

---

## Related Resources

- [Upload Files to Cloud Storage](/upload-files/) *(internal link)*  
- [Aspose.Cells Cloud SDKs](/sdks/) *(internal link)*  
- [Compare: Built-in Excel Functions vs. Aggregate API](/comparison/) *(internal link)*  
- [Error Handling in Aspose.Cells Cloud](/error-handling/) *(internal link)*

---