---  
title: "Refresh an Auto Filter in an Excel Worksheet"  
second_title: "Document"  
linktitle: "Refresh auto filter"  
type: docs  
url: /autofilter/refresh/  
aliases: [/refresh-an-autofilter/]  
weight: 100  
keywords: "Aspose.Cells Cloud, refresh autofilter, Excel API, AutoFilter refresh, REST API, spreadsheet"  
description: "Refresh an existing AutoFilter on an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL and SDK examples for C#, Java, Python, and more."  
---  

This REST API refreshes an auto‑filter on an Excel worksheet.

### What does **Refresh** do?

Calling the endpoint re‑applies the current filter criteria after the worksheet data has changed (e.g., rows added or removed). The operation does not modify the filter definition; it simply updates the view and returns a status response.

### Prerequisites  

- A valid Aspose Cloud account.  
- An OAuth 2.0 JWT token obtained from the Aspose authentication service.  
- The workbook must already contain an AutoFilter.  
- The file must be stored in Aspose Cloud storage (default or a custom `storageName`).  

### Authentication  

1. Register your application in the Aspose Cloud portal to obtain a client‑id and client‑secret.  
2. Request a JWT token using the client credentials.  
3. Include the token in the `Authorization` header of each request:  

```http
Authorization: Bearer <your‑jwt‑token>
```  

### REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

#### Request parameters  

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| **name**       | string | path     | Name of the Excel file (e.g., `Book1.xlsx`). |
| **sheetName**  | string | path     | Name of the worksheet that contains the filter. |
| **folder**     | string | query    | Folder path in storage where the file resides. |
| **storageName**| string | query    | Name of the storage (if not the default). |

You can use the **cURL** command‑line tool to call the API easily. The example below demonstrates a request with a valid JWT token.

#### cURL request and response  

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Possible errors  

| HTTP Status | Code | Description | Recommended action |
|-------------|------|-------------|--------------------|
| 400 | `BadRequest` | The request is malformed or required parameters are missing. | Verify all required path/query parameters. |
| 401 | `Unauthorized` | Invalid or missing JWT token. | Obtain a fresh token and include it in the `Authorization` header. |
| 404 | `NotFound` | The specified file or worksheet does not exist. | Check the `name`, `sheetName`, and `folder` values. |
| 500 | `InternalServerError` | An unexpected server error occurred. | Retry later or contact Aspose support with the request ID. |

### SDK examples  

*(The Cloud SDK Family section is unchanged.)*  

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}

### FAQ  

<details>  
<summary>How do I refresh an AutoFilter after adding new rows?</summary>  
Call `POST /cells/{name}/worksheets/{sheetName}/autoFilter/refresh` with a valid JWT token. The endpoint re‑applies the existing filter criteria to the updated data range.  
</details>  

<details>  
<summary>What response do I get if the file does not exist?</summary>  
The API returns **404** with the JSON body `{ "Code": 404, "Status": "File not found" }`.  
</details>  

<details>  
<summary>Can I refresh an AutoFilter on a workbook stored in a custom storage?</summary>  
Yes. Include the `storageName` query parameter that points to the custom storage location.  
</details>  

### Additional information  

- **Supported version:** Aspose.Cells Cloud **v3.0** and later.  
- **Reference links:**  
  - OpenAPI specification: <https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh>  
  - SDK documentation: <https://docs.aspose.cloud/cells/sdk/>  

---  

*Authored by an Aspose Cloud Engineer (2024). For security details, see the Aspose Cloud security whitepaper.*