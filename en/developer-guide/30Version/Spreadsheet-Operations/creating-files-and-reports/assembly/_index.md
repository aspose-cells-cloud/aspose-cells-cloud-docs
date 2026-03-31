---
title: "Assembling Data for the Creation of an Excel Report"
second_title: "Document"
linktitle: "Assembly Data"
type: docs
url: /assembly-data-for-the-creation-of-an-excel-report/
aliases: [/assembly/]
keywords: "Aspose.Cells, Excel report, data assembly, Cloud API, REST, SDK, cURL, PDF, ODS"
description: "Learn how to use Aspose.Cells Cloud’s Assembly API to merge data into Excel (XLSX, PDF, ODS) reports. Includes endpoint, parameters, cURL sample, SDK code, auth guide, and error handling."
weight: 40
---

This REST API assembles data **into** an Excel file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

The request parameters are:

| Parameter Name | Type   | Location                     | Description                                                                 |
|----------------|--------|------------------------------|-----------------------------------------------------------------------------|
| file           | file   | formData (multipart body)   | The spreadsheet file to upload.                                            |
| DataSource     | string | query string                 | Identifier of the data source that provides the data for the assembly.    |
| format         | string | query string                 | Desired output format (e.g., `xlsx`, `pdf`).                               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

> **Authentication** – Obtain a JWT token from `https://api.aspose.cloud/connect/token` using your client ID and secret, then include it in the `Authorization: Bearer <jwt token>` header. Tokens are valid for 1 hour and must be refreshed as needed.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

> **Error handling** – If the request fails, the API returns a standard HTTP error code (e.g., 400 Bad Request, 401 Unauthorized, 500 Internal Server Error) together with a JSON payload that contains `Code`, `Message`, and optional `Details` fields.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop against the API. An SDK abstracts low‑level details, allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}