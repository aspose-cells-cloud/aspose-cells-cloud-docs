---
title: "How to Work with Visibility on an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Visibility"
type: docs
url: /worksheets/panes/
keywords: "Aspose.Cells Cloud, hide worksheet API, unhide worksheet API, Excel worksheet visibility, REST API Excel, Aspose.Cells v3.0"
description: "Hide or unhide Excel worksheets using Aspose.Cells Cloud API: PUT /cells/{fileName}/worksheets/{sheetName}/visibility"
weight: 100
ArticleTitle: "Hide or Unhide Excel Worksheet with Aspose.Cells Cloud REST API"
---

## Working with visibility on an Excel worksheet

- **Hide a worksheet** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`
- **Unhide a worksheet** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

---

## Hide a Worksheet

### Request

```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Response

```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Sample cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Sample .NET SDK

```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Worksheet hidden: {response.Worksheet.Visible}");
```

### Common Errors

| HTTP Code | Description                            | Mitigation                                               |
| --------- | -------------------------------------- | -------------------------------------------------------- |
| 400       | Invalid JSON body or missing `Visible` | Ensure the request body is valid JSON with the key.      |
| 401       | Unauthorized – token missing/expired   | Refresh the OAuth token and include it in the header.    |
| 404       | Worksheet or file not found            | Verify `{fileName}` and `{sheetName}` are correct.       |
| 409       | Worksheet already hidden               | Check the current visibility before sending the request. |

---

## Unhide a Worksheet

### Request

```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Response

```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Sample cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Sample .NET SDK

```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Worksheet visible: {response.Worksheet.Visible}");
```

### Common Errors

| HTTP Code | Description                            | Mitigation                                             |
| --------- | -------------------------------------- | ------------------------------------------------------ |
| 400       | Invalid JSON body or missing `Visible` | Provide a correct JSON payload with `"Visible": true`. |
| 401       | Unauthorized – token missing/expired   | Regenerate the access token and retry.                 |
| 404       | Worksheet or file not found            | Confirm the file and sheet names exist in storage.     |
| 409       | Worksheet already visible              | No action needed; the worksheet is already unhidden.   |
