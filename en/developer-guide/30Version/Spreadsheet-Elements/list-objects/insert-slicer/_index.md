---
title: "Insert a Slicer into an Excel ListObject – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Insert slicer"
type: docs
keywords: "Aspose.Cells, insert slicer, ListObject API, Excel REST API, cloud SDK"
url: /list-objects/insert-slicer/
description: "Learn how to add a slicer to an Excel ListObject using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, authentication, sample cURL request, and response JSON."
weight: 20
---

This REST API inserts a slicer for a list object on an Excel worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

> **NOTE:** The original documentation contained a double slash (`//`) after `v3.0`. The corrected URL above uses a single slash to avoid potential 404 errors.

### Prerequisites

- A valid Aspose Cloud subscription.  
- The Excel file must be uploaded to Aspose Cloud storage.  
- A ListObject must already exist in the target worksheet.  

### Authentication

The request must include an **Authorization** header with a JWT token.  
Obtain the token via the OAuth 2.0 client‑credentials flow:

```bash
POST https://api.aspose.cloud/connect/token
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>
```

The response contains an `access_token`. Use it as follows:

```
Authorization: Bearer <access_token>
```

### Request Parameters

| Parameter Name   | Type    | Location | Description                                                                 |
|------------------|---------|----------|-----------------------------------------------------------------------------|
| name             | String  | Path     | The name of the Excel file.                                                |
| sheetName        | String  | Path     | The name of the worksheet that contains the list object.                  |
| listObjectIndex  | Integer | Path     | The zero‑based index of the list object to which the slicer will be added.|
| columnIndex      | Integer | Query    | The zero‑based index of the column on which the slicer is based.           |
| destCellName     | String  | Query    | The cell reference (e.g., **A1**) where the slicer will be placed.        |
| folder           | String  | Query    | The folder in storage that contains the Excel file.                        |
| storageName      | String  | Query    | The name of the Aspose Cloud storage service.                              |

You can use the cURL command‑line tool to call the API:

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
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
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```
{{< /tab >}}
{{< /tabs >}}

### Response Codes

| HTTP Code | Meaning                     | Description                                                            |
|----------|-----------------------------|------------------------------------------------------------------------|
| 200      | OK                          | The slicer was inserted successfully.                                 |
| 400      | Bad Request                 | Missing or invalid parameters.                                         |
| 401      | Unauthorized                | Invalid or missing JWT token.                                          |
| 403      | Forbidden                   | Insufficient permissions to access the file or storage.               |
| 404      | Not Found                   | The specified file, worksheet, or list object does not exist.         |
| 500      | Internal Server Error       | An unexpected error occurred on the server side.                       |

### Error Handling

When an error occurs, the API returns a JSON object with an `ErrorMessage` field that describes the problem. Inspect the HTTP status code and the `ErrorMessage` to determine the corrective action.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the GitHub repository for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}

## Frequently Asked Questions

**Q: How do I obtain the JWT token required for the `Authorization` header?**  
A: Use the OAuth 2.0 client‑credentials flow:  

```bash
POST https://api.aspose.cloud/connect/token
Content-Type: application/x-www-form-urlencoded

grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>
```  

The response contains an `access_token`. Include it as `Bearer <access_token>` in the `Authorization` header.

**Q: What is the correct endpoint URL for inserting a slicer?**  
A: `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer` (note the single slash after `v3.0`).

**Q: What does the API return after a successful slicer insertion?**  
A: A JSON object with HTTP status `200`. Example:

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```