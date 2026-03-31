---  
title: "Add watermark to Excel files"  
second_title: "Document"  
linktitle: "Add Watermark to Excel Files"  
type: docs  
url: /add-watermark-into-excel-files/  
aliases: [ /watermark/ ]  
keywords: "add watermark to Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"  
description: "Learn how to add a text watermark to Excel workbooks using Aspose.Cells Cloud REST API (v3.0). Includes cURL example, required parameters, and response details."  
weight: 39  
---  

This REST API adds a **watermark** to Excel files.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/watermark
```  

The request parameters are:

| Parameter Name | Type   | Location                     | Description                                                                 |
|----------------|--------|------------------------------|-----------------------------------------------------------------------------|
| `file`         | file   | formData (multipart body)   | The Excel file to which the watermark will be applied.                     |
| `text`         | string | query                        | The watermark text to display.                                              |
| `color`        | string | query                        | The watermark colour in ARGB hex format (e.g., `004433ff`).                |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The example below shows a complete request, including the required authentication header. Replace `<your‑jwt‑token>` with a valid JWT access token obtained from the Aspose authentication endpoint.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

The JSON response contains a **Files** array. For each file object:

* **Filename** – name of the processed workbook.  
* **FileSize** – size of the file in bytes.  
* **FileContent** – Base64‑encoded content of the watermarked Excel file; decode it to obtain the actual file.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details, allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}