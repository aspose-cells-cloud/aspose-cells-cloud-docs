---
title: "How to Work with Visibility on an Excel Worksheet"
second_title: "Document"
linktitle: "Visibility"
type: docs
url: /worksheets/panes/
keywords: "Aspose.Cells Cloud, hide worksheet API, unhide worksheet API, Excel worksheet visibility, REST API Excel, Aspose.Cells v3.0"
description: "Learn to programmatically hide or unhide Excel worksheets using Aspose.Cells Cloud REST API. Includes request URLs, cURL & .NET SDK examples, error handling, and version‑specific notes."
weight: 20
---

## Working with visibility on an Excel worksheet

*Worksheet visibility* defines whether a sheet is shown to the end‑user. With Aspose.Cells Cloud you can hide or unhide a worksheet through a simple REST call. The API endpoints used are:

* **Hide a worksheet** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Unhide a worksheet** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Supported API version:** **v3.0** (as of March 2026)

### Prerequisites
1. An active **Aspose.Cells Cloud** account.  
2. A valid **client ID** and **client secret** (or OAuth 2.0 access token).  
3. The workbook (`{fileName}`) must already be uploaded to Aspose cloud storage.  

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
| HTTP Code | Description                              | Mitigation                                               |
|----------|------------------------------------------|----------------------------------------------------------|
| 400      | Invalid JSON body or missing `Visible`   | Ensure the request body is valid JSON with the key.     |
| 401      | Unauthorized – token missing/expired      | Refresh the OAuth token and include it in the header.   |
| 404      | Worksheet or file not found               | Verify `{fileName}` and `{sheetName}` are correct.       |
| 409      | Worksheet already hidden                  | Check the current visibility before sending the request. |

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
| HTTP Code | Description                              | Mitigation                                               |
|----------|------------------------------------------|----------------------------------------------------------|
| 400      | Invalid JSON body or missing `Visible`   | Provide a correct JSON payload with `"Visible": true`. |
| 401      | Unauthorized – token missing/expired      | Regenerate the access token and retry.                  |
| 404      | Worksheet or file not found               | Confirm the file and sheet names exist in storage.      |
| 409      | Worksheet already visible                 | No action needed; the worksheet is already unhidden.    |

---

## Related Operations
> *Freeze Panes* | *Split Panes* | *Zoom* – see the corresponding pages for additional worksheet layout controls.

---

## Frequently Asked Questions

<dl>
  <dt>How do I hide a worksheet using Aspose.Cells Cloud API?</dt>
  <dd>Send a `PUT` request to `/cells/{fileName}/worksheets/{sheetName}/visibility` with the JSON body `{ "Visible": false }`. Include a valid OAuth 2.0 bearer token. A `200 OK` response returns the updated worksheet object.</dd>

  <dt>What response do I receive after unhiding a worksheet?</dt>
  <dd>The API returns `200 OK` with a payload that contains the worksheet object where `"Visible": true`. The response includes the worksheet’s `Name`, `Index`, and `Visible` properties.</dd>

  <dt>Can I hide multiple worksheets in a single call?</dt>
  <dd>No. The visibility endpoint works on a single worksheet identified by `{sheetName}`. To hide several sheets, iterate over each name in your client code.</dd>
</dl>

---

*Written by the Aspose Docs team – over 15 years of experience automating Excel workflows.*