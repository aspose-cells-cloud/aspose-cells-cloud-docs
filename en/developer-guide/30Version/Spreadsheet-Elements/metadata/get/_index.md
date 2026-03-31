---
title: "Get metadata from Excel files"
second_title: "Document"
linktitle: "Get without using storage"
type: docs
url: /metadata/get/
keywords: "Aspose.Cells, Excel metadata, REST API, cloud SDK, get metadata"
description: "Retrieve built‑in or custom metadata from Excel workbooks using Aspose.Cells Cloud REST API. Includes request format, parameters, sample SDK code, and error handling."
weight: 23
---

This REST API retrieves **metadata** from one or more Excel files.  
The request must include an `Authorization: Bearer <access_token>` header obtained via the OAuth 2.0 client‑credentials flow.

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### Query Parameter

| Parameter Name | Type   | Description                                                                 |
|----------------|--------|-----------------------------------------------------------------------------|
| type           | string | `ALL` / `BuiltIn` / `Custom` – specifies which metadata groups to return.   |

### Request Body Parameter

| Parameter Name | Type      | Description                                                            |
|----------------|-----------|------------------------------------------------------------------------|
| excel file     | data file | The Excel file supplied as the first part of the multipart request.   |

### Response

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

The API returns standard HTTP status codes (e.g., **200** for success, **400** for a bad request, **401** for unauthorized access, **404** if the file is not found, and **500** for server errors) together with an error‑response JSON object when applicable.

### Cloud SDK Family

Using a SDK accelerates development by handling low‑level details. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}