---
title: "Remove Duplicate Rows from a ListObject – Aspose.Cells Cloud API Documentation"
second_title: "Document"
linktitle: "Remove duplicates"
type: docs
keywords: "remove duplicates, listobject, Aspose.Cells Cloud API, Excel, REST"
url: /list-objects/remove-duplicates/
description: "Learn how to delete duplicate rows from a ListObject in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes endpoint, parameters, authentication, and sample requests and responses."
weight: 20
---

This REST API removes duplicate rows from a **ListObject** in an Excel worksheet.

## REST API

### Prerequisites
To call this endpoint you must obtain a JWT access token from the Aspose Cloud OAuth service and include it in the `Authorization` header:

```http
Authorization: Bearer <jwt token>
```

### Request

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

The request parameters are:

| Parameter Name   | Type    | Location | Description                                                   |
|------------------|---------|----------|---------------------------------------------------------------|
| **name**         | String  | Path     | The name of the Excel file.                                    |
| **sheetName**    | String  | Path     | The name of the worksheet that contains the list object.      |
| **listObjectIndex** | Integer | Path | The zero‑based index of the list object to process.           |
| **folder**       | String  | Query    | (Optional) The folder path where the file is stored.          |
| **storageName**  | String  | Query    | (Optional) The name of the storage service.                   |

### Sample Request (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "Duplicate rows were successfully removed."
}
```

{{< /tab >}}
{{< /tabs >}}

### Response
On success the service returns a JSON object similar to the example above. The fields are:

- **Code** – HTTP status code (`200` for success).  
- **Status** – Textual description of the status.  
- **DuplicateRowsRemoved** – Number of rows that were eliminated.  
- **Message** – Additional information about the operation.

### Error Codes
| HTTP Status | Meaning                              | When it occurs |
|-------------|--------------------------------------|----------------|
| 400         | Bad Request                          | Missing or invalid parameters. |
| 401         | Unauthorized                         | No token supplied or token is expired/invalid. |
| 404         | Not Found                            | Specified file, worksheet, or list object does not exist. |
| 500         | Internal Server Error                | Unexpected server‑side failure. |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check the GitHub repository for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}