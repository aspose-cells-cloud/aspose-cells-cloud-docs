---
title: "Update a shape on an Excel worksheet"
second_title: "Document"
linktitle: "Update"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "update shape Excel API, Aspose.Cells Cloud, Excel shape update, REST API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Learn how to update a shape in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes HTTPS endpoint, authentication details, DTO schema, step‑by‑step usage, cURL example, and SDK code samples for multiple languages."
weight: 31
---

This REST API updates a shape on an Excel worksheet.

## Prerequisites

- **Authentication** – Obtain a JWT access token via the OAuth 2.0 client‑credentials flow. The token must be included in the `Authorization: Bearer <accessToken>` header of every request.  
- **API version** – The examples use **v3.0** of the Aspose.Cells Cloud API (verify that this is the latest version for your account).  
- **Storage configuration** – Ensure the workbook is stored in an Aspose Cloud storage location that you have access to (default storage is used if `storageName` is omitted).

## Authentication

```http
Authorization: Bearer <accessToken>
```

Replace `<accessToken>` with the JWT token you obtained in the prerequisites step. The token must have the **Cells** scope.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### Request parameters

| Parameter Name | Type    | Location | Description |
|----------------|---------|----------|-------------|
| **name** | string | path | The name of the workbook file. |
| **sheetName** | string | path | The name of the worksheet that contains the shape. |
| **shapeindex** | integer | path | The zero‑based index of the shape within the worksheet. |
| **dto** | object | body | The shape data‑transfer object that contains the updated properties (see *DTO Schema* below). |
| **folder** | string | query | The folder where the workbook is stored. |
| **storageName** | string | query | The name of the Aspose Cloud storage. |

### DTO Schema

The `dto` object contains the properties that can be updated. All fields are optional unless otherwise noted.

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| **Name** | string | No | New name for the shape. |
| **UpperLeftRow** | integer | No | Row index of the shape’s upper‑left corner. |
| **UpperLeftColumn** | integer | No | Column index of the shape’s upper‑left corner. |
| **Width** | integer | No | Width of the shape (in points). |
| **Height** | integer | No | Height of the shape (in points). |
| **RotationAngle** | integer | No | Rotation angle in degrees. |
| **IsHidden** | boolean | No | `true` to hide the shape. |
| **IsLocked** | boolean | No | `true` to lock the shape. |
| **Font** | object | No | Font settings (see OpenAPI spec for sub‑properties). |
| **...** | … | No | Additional properties such as `HtmlText`, `AlternativeText`, `ZOrderPosition`, etc. |
> For a complete list, refer to the official OpenAPI specification: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### Request headers

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>`  *(the JWT token from the *Authentication* step)*

### Request body (example)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## Step‑by‑Step Usage

1. **Obtain a JWT token** – Follow the *Authentication* prerequisites.  
2. **Upload the workbook** (if it does not already exist) to the desired folder in Aspose Cloud storage.  
3. **Create the DTO** – Populate the JSON body with the properties you wish to modify.  
4. **Call the API** – Use the cURL command‑line tool (or an SDK) shown below.  
5. **Verify the response** – A successful call returns a `200` status code and a JSON payload confirming the update.

## Example with cURL (command‑line tool)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Error handling** – The API may return the following status codes:

| Code | Meaning | Typical cause |
|------|---------|---------------|
| 400 | Bad Request | Invalid JSON or missing required fields. |
| 401 | Unauthorized | Missing or invalid JWT token. |
| 404 | Not Found | Workbook, worksheet, or shape index does not exist. |
| 500 | Internal Server Error | Unexpected server‑side problem. |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}