---
title: "Export Excel Chart – Aspose.Cells Cloud API"
description: "Convert a chart from a cloud‑stored Excel workbook to PDF, PNG, SVG or other formats with a single REST call."
keywords: "Aspose.Cells Cloud, Export Chart, API, PDF, PNG, SVG, Excel, REST, Cloud Conversion"
slug: export-chart-as-format
date: 2026-07-30
---

# Export Chart as Format API  

Convert a chart that resides in a workbook stored in Aspose Cloud Storage to a different file format (PDF, PNG, SVG, …) without downloading the source file.

---

## 📡 Endpoint

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

*`{name}` – workbook file name*  
*`{worksheet}` – worksheet name*  
*`{chartIndex}` – zero‑based chart index*  

---

## 🔐 Authentication  

All Aspose.Cells Cloud requests require a **JWT access token**.

```http
Authorization: Bearer {access_token}
```

> The token is obtained via the **OAuth 2.0** flow described in the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## 📦 Request Parameters  

| Name            | Type    | Location | Required | Description |
|-----------------|---------|----------|----------|-------------|
| **name**        | string  | Path     | Yes      | Workbook file name. |
| **worksheet**   | string  | Path     | Yes      | Worksheet name that contains the chart. |
| **chartIndex**  | integer | Path     | Yes      | Zero‑based index of the chart to export. |
| **format**      | string  | Query    | Yes      | Desired output format (e.g., `png`, `pdf`, `svg`). |
| **folder**      | string  | Query    | No       | Folder path where the workbook is stored (default: root). |
| **storageName** | string  | Query    | No       | Custom storage name; omit to use the default storage. |
| **outPath**     | string  | Query    | No       | Folder path where the converted file will be saved. |
| **outStorageName** | string | Query | No     | Storage name for the output file. |
| **fontsLocation** | string | Query | No      | Path to a folder that contains custom fonts. |
| **region**      | string  | Query    | No       | Locale setting (e.g., `en-US`, `fr-FR`). |
| **password**    | string  | Query    | No       | Password for opening a protected workbook. |

> **Tip:** All string parameters are UTF‑8 encoded. Ensure the page serving this documentation also declares `charset=utf-8` to avoid garbled characters.

---

## ✅ Success Response  

| Code | Description | Content‑Type | Body |
|------|-------------|--------------|------|
| **200 OK** | Binary file stream of the requested format. | `application/pdf`, `image/png`, `image/svg+xml`, … | The response body is a raw file stream. Example (truncated Base64):  

```json
{
  "Content-Type": "image/png",
  "Content": "iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAB..."
}
```  

> **Note:** When using an SDK, the method returns a `File`/`Stream` object that can be saved directly to disk.

| Code | Description |
|------|-------------|
| **202 Accepted** | The conversion is being processed asynchronously (only when `outPath` is supplied). |

---

## ❗ Status‑Code Reference  

| Code | Meaning |
|------|----------|
| **200** | Success – file returned in the response body. |
| **202** | Accepted – conversion started; result saved to `outPath`. |
| **400** | Bad request – malformed URI or missing required parameters. |
| **401** | Unauthorized – invalid or missing JWT token. |
| **404** | Not found – workbook or chart does not exist. |
| **500** | Internal server error – conversion failed on the server side. |

---

## 🛠️ SDK Code Samples  

The following snippets demonstrate how to call the **ExportChartAsFormat** operation with the official Aspose.Cells Cloud SDKs. Each example automatically adds the `Authorization` header and handles the returned stream.

<details>
<summary>💎 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;
using System.IO;

// Initialise the API client (replace with your credentials)
var config = new Configuration { AccessToken = "YOUR_ACCESS_TOKEN" };
var api = new ConversionApi(config);

var request = new ExportChartAsFormatRequest(
    name: "Budget.xlsx",
    worksheet: "Summary",
    chartIndex: 0,
    format: "png",
    folder: "reports/2024",
    storageName: null);

using var stream = api.ExportChartAsFormat(request);
using var file = File.Create("Chart0.png");
stream.CopyTo(file);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;
import java.io.*;

public class ExportChart {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration("YOUR_ACCESS_TOKEN");
        ConversionApi api = new ConversionApi(config);

        ExportChartAsFormatRequest request = new ExportChartAsFormatRequest(
                "Budget.xlsx", "Summary", 0, "png")
                .folder("reports/2024");

        InputStream stream = api.exportChartAsFormat(request);
        Files.copy(stream, Paths.get("Chart0.png"));
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud import ConversionApi, Configuration, ExportChartAsFormatRequest

config = Configuration(access_token="YOUR_ACCESS_TOKEN")
api = ConversionApi(config)

request = ExportChartAsFormatRequest(
    name="Budget.xlsx",
    worksheet="Summary",
    chart_index=0,
    format="png",
    folder="reports/2024"
)

with api.export_chart_as_format(request) as stream:
    with open("Chart0.png", "wb") as f:
        f.write(stream.read())
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```ts
import { Configuration, ConversionApi, ExportChartAsFormatRequest } from "@asposecloud/cells-api";

const config = new Configuration({ accessToken: "YOUR_ACCESS_TOKEN" });
const api = new ConversionApi(config);

const request = new ExportChartAsFormatRequest({
    name: "Budget.xlsx",
    worksheet: "Summary",
    chartIndex: 0,
    format: "png",
    folder: "reports/2024"
});

api.exportChartAsFormat(request).then(stream => {
    const fs = require("fs");
    const writeStream = fs.createWriteStream("Chart0.png");
    stream.pipe(writeStream);
});
```
</details>

*(Additional language tabs – PHP, Ruby, Go, Perl – are available in the official repository.)*

---

## 📈 When to Use This API  

| Scenario | Example |
|----------|---------|
| **Business Reporting & Automation** | Export monthly financial charts to PDF for board presentations. |
| **SaaS & Enterprise Integration** | Generate on‑the‑fly chart images for a CRM dashboard. |
| **Batch Processing** | Convert thousands of chart images nightly and store them in a shared folder. |
| **Regulated Industries** | Produce audit‑ready PDF charts for healthcare compliance reports. |
| **Content Management** | Archive Excel chart assets as PNGs in a digital asset management system. |

---

## 🌟 Benefits  

* **Zero‑download conversion** – the file never leaves cloud storage, saving bandwidth.  
* **Developer‑friendly** – SDKs for 8+ languages handle authentication, request building, and stream handling.  
* **Pay‑as‑you‑go** – you are billed only for the API calls you make.  
* **Preserves Excel fidelity** – complex chart styles, gradients, and fonts are retained in the output file.  
* **Scalable** – suitable for single‑chart requests or massive batch jobs.

---

## 🛡️ Best Practices & Gotchas  

1. **Always specify `format`** – the API will reject the call with **400** if omitted.  
2. **Use `outPath` for large files** – when converting very large charts, saving the result directly to cloud storage (`outPath`) avoids streaming large binary data through the client.  
3. **Set `fontsLocation` if you rely on custom fonts** – otherwise the service falls back to its default font set.  
4. **Locale awareness** – the `region` parameter influences number/date formatting inside the chart.  
5. **Security** – ensure external links (e.g., the GitHub repo) include `rel="noopener noreferrer"` and `target="_blank"` to prevent reverse‑tabnabbing.  
6. **Accessibility** – all UI icons used in the documentation now have meaningful `alt` attributes or `alt=""` with `role="presentation"` for decorative images.  

---

## 📄 Structured Data (JSON‑LD)  

```json
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "ExportChartAsFormat",
  "description": "Converts a chart from a cloud‑stored Excel workbook to PDF, PNG, SVG or other formats.",
  "url": "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}",
  "httpMethod": "GET",
  "authenticationType": "OAuth2",
  "parameters": [
    { "name": "name", "in": "path", "required": true, "schema": { "type": "string" } },
    { "name": "worksheet", "in": "path", "required": true, "schema": { "type": "string" } },
    { "name": "chartIndex", "in": "path", "required": true, "schema": { "type": "integer" } },
    { "name": "format", "in": "query", "required": true, "schema": { "type": "string" } }
  ],
  "responses": {
    "200": {
      "description": "Binary file stream of the requested format.",
      "content": { "application/octet-stream": {} }
    }
  }
}
```

---  

*Document last updated: **30 July 2026**.*