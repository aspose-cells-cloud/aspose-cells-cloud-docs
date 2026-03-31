---
title: "Export OLE Object – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "OLE Object"
type: docs
url: /export-excel-ole-object/
aliases: [ /export/excel-ole-object/]
keywords: "export OLE object, Aspose.Cells API, Excel OLE export, cloud spreadsheet API"
description: "Learn how to export OLE objects from an Excel workbook using the Aspose.Cells Cloud REST API. Includes authentication details, request parameters, response schema, error handling, and SDK examples."
weight: 20
---

- **REST API**

| **API** | **Type** | **Description** | **Swagger Link** |
| ------- | -------- | --------------- | ---------------- |
| /cells/export | POST | Exports an Excel workbook containing OLE objects to the specified output format. | [PostExport](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### What is an OLE object?

An **OLE (Object Linking and Embedding) object** embeds external content—such as Word documents, PowerPoint slides, images, or other files—inside an Excel workbook. When exported, the embedded content is extracted and saved in the requested output format.

### Authentication

Aspose.Cells Cloud uses **OAuth 2.0**. Obtain an access token from the `/connect/token` endpoint and include it in the `Authorization` header of every request:

```http
Authorization: Bearer <access_token>
```

### Endpoint Overview

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`  

* `objectType` – Must be set to `oleobject`.  
* `format` – Desired output format (e.g., `pdf`, `png`, `jpeg`, `docx`, `pptx`).  

### Request Parameters

| Parameter | Location | Type | Required | Description |
|-----------|----------|------|----------|-------------|
| `file` | Form‑data | file | Yes | The Excel workbook (`.xlsx`, `.xls`, etc.) that contains the OLE objects. |
| `outputFormat` | Query | string | Yes | Target format for the exported objects (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType` | Query | string | Yes | Fixed value `oleobject`. |
| `Authorization` | Header | string | Yes | Bearer token obtained via OAuth 2.0. |

#### Sample cURL request

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### Response

A successful request returns a JSON object that lists the exported files:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### Error Codes

| HTTP Status | Description | Example JSON |
|-------------|-------------|--------------|
| **400** | Bad request – missing or invalid parameters. | `{ "error": { "code": "BadRequest", "message": "The 'file' field is required." } }` |
| **401** | Unauthorized – invalid or missing access token. | `{ "error": { "code": "Unauthorized", "message": "Access token is missing or invalid." } }` |
| **500** | Internal server error – unexpected failure on the server side. | `{ "error": { "code": "InternalError", "message": "An unexpected error occurred." } }` |

### Common Errors & Remedies

| Situation | Cause | Remedy |
|-----------|-------|--------|
| **File size exceeds limit** | Uploaded file > 100 MB. | Upload the file to Aspose Cloud storage first and reference it via the `Path` parameter, or reduce the file size. |
| **Unsupported output format** | `format` query value not in the allowed list. | Use one of the supported formats: `pdf`, `png`, `jpeg`, `docx`, `pptx`. |
| **Missing Authorization header** | No bearer token supplied. | Obtain a token from `/connect/token` and include `Authorization: Bearer <token>` in the request. |

### FAQ

**Q:** *What formats can OLE objects be exported to?*  
**A:** Use the `format` query parameter. Supported values are `pdf`, `png`, `jpeg`, `docx`, and `pptx`.

**Q:** *How do I specify the output format?*  
**A:** Append `&format={outputFormat}` to the request URL, e.g., `?objectType=oleobject&format=pdf`.

**Q:** *What is the maximum size of the Excel file I can upload?*  
**A:** The API accepts files up to **100 MB** for the `POST /cells/export` operation.

---

- **Cloud SDK Family**

Using an SDK is the best way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}