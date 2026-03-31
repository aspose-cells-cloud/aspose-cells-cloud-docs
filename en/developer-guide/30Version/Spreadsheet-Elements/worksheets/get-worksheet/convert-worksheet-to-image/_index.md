---  
title: "Convert Worksheet to PDF, PNG, CSV & More – Aspose.Cells Cloud API"  
second_title: "Document"  
linktitle: "Convert worksheet"  
type: docs  
url: /worksheets/conversion/  
aliases:  
  - /convert-worksheet-to-image/  
  - /worksheets/to-image/  
keywords: "Aspose.Cells, worksheet conversion, REST API, cURL, SDK, PDF, PNG, CSV"  
description: "Learn how to convert a single worksheet from an Excel workbook to PDF, PNG, CSV, and 15+ other formats using Aspose.Cells Cloud REST API. Includes cURL example, SDK snippets, and full parameter reference."  
weight: 130  
---  

**Worksheet conversion API** – The `GET /cells/{name}/worksheets/{sheetName}` endpoint converts a single worksheet (a sheet inside an Excel workbook) to another file type.

Supported **importable** formats (the worksheet can be read from):  

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT  

Supported **export‑only** formats (the worksheet can be saved as):  

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS  

## REST API  

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) describes the publicly accessible interface.  

### Prerequisites & Authentication  

* Obtain a JWT token from the Aspose Cloud authentication service.  
* Include the token in the request header:  

```bash
-H "Authorization: Bearer <jwt token>"
```  

* The API version used in the examples is **v3.0**.

### Parameters  

| Parameter | Type | Required | Default | Allowed Values | Description |
|-----------|------|----------|---------|----------------|-------------|
| **format** | string | Yes | – | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (see supported list) | Target output format. |
| **verticalResolution** | integer | No | 96 | 72‑600 | Vertical DPI for image output. |
| **horizontalResolution** | integer | No | 96 | 72‑600 | Horizontal DPI for image output. |
| **password** | string | No | – | – | Password for opening a protected workbook. |
| **folder** | string | No | – | – | Cloud folder where the source workbook is stored. |
| **storage** | string | No | – | – | Name of the storage (e.g., “Default”). |

### Response  

| Status Code | Description | Return Type |
|------------|-------------|------------|
| **200** | Conversion succeeded; binary stream of the converted file is returned. | `application/octet-stream` |
| **400** | Bad request – missing or invalid parameters. | JSON error object |
| **401** | Unauthorized – invalid or missing JWT token. | JSON error object |
| **404** | Not found – workbook or worksheet does not exist. | JSON error object |
| **500** | Internal server error – unexpected failure. | JSON error object |

#### Example Request (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Example Response  

```
Converted Image (binary stream)
```

## Cloud SDK Family  

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Frequently Asked Questions  

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What HTTP method is used to convert a worksheet with Aspose.Cells Cloud?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The endpoint uses the **GET** method on `/cells/{name}/worksheets/{sheetName}` with the `format` query parameter specifying the desired output type."
      }
    },
    {
      "@type": "Question",
      "name": "Which image formats can a worksheet be exported to?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The API supports PNG, JPEG, BMP, SVG, TIFF, and EMF for image export."
      }
    },
    {
      "@type": "Question",
      "name": "How do I authenticate the request to the worksheet conversion endpoint?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Include an `Authorization: Bearer <jwt token>` header obtained from the Aspose Cloud authentication service."
      }
    }
  ]
}
```

---  