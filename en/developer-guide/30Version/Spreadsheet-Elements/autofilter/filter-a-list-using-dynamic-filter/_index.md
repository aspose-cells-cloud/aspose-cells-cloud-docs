---
title: Add a dynamic filter in an Excel worksheet using Aspose.Cells Cloud API
description: Learn how to apply a dynamic filter (e.g., BelowAverage, Tomorrow, LastMonth) to an Excel worksheet with the Aspose.Cells Cloud REST API. Includes authentication, request syntax, parameters, response handling, and SDK examples for multiple languages.
keywords: Aspose.Cells, dynamic filter, Excel API, REST, auto filter, cloud SDK
slug: add-dynamic-filter
api_version: v3.0
---

## Overview

The **PutWorksheetDynamicFilter** operation adds a dynamic filter to a specified range in an Excel worksheet.  
Dynamic filters automatically evaluate values such as dates, averages, or blanks, allowing you to create “smart” views without writing custom formulas.

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Authentication** | A valid JWT token obtained from the `/connect/token` endpoint. Include it in the `Authorization: Bearer <token>` header. |
| **Storage** | The workbook must reside in an Aspose Cloud storage location (default or a custom storage). |
| **Supported file formats** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv`, etc. |
| **Permissions** | Read/write access to the target folder/file. |

## HTTP Request

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `name` | string | ✅ | The name of the Excel workbook (e.g., `Book1.xlsx`). |
| `sheetName` | string | ✅ | The name of the worksheet that contains the range to be filtered. |

### Query Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `range` | string | ✅ | The cell range on which the filter is applied (e.g., `A1:B1`). |
| `fieldIndex` | integer | ✅ | Zero‑based index of the column inside the range to which the dynamic filter is applied. |
| `dynamicFilterType` | string | ✅ | Type of dynamic filter to apply (see **Supported Dynamic Filter Types**). |
| `matchBlanks` | boolean | ❌ | If `true`, blank cells are included in the filter results. Default: `false`. |
| `refresh` | boolean | ❌ | If `true`, the auto‑filter is refreshed after applying the filter. |
| `folder` | string | ❌ | Path to the folder in storage where the workbook is located. |
| `storageName` | string | ❌ | Name of the Aspose Cloud storage to use. |

### Request Body

The request body is an empty JSON object:

```json
{}
```

## Supported Dynamic Filter Types

| Value | Meaning |
|-------|----------|
| `BelowAverage` | Rows whose value is below the column’s average. |
| `AboveAverage` | Rows whose value is above the column’s average. |
| `Tomorrow` | Rows with dates equal to tomorrow’s date. |
| `Yesterday` | Rows with dates equal to yesterday’s date. |
| `NextWeek` | Rows with dates falling in the next calendar week. |
| `LastMonth` | Rows with dates from the previous month. |
| `ThisYear` | Rows with dates occurring in the current year. |

## Example Request (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT request has an empty JSON body
```

## Example Response

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Dynamic filter applied successfully."
}
```

### HTTP Status Codes

| Code | Meaning | Description |
|------|---------|-------------|
| **200** | OK | Dynamic filter applied successfully. |
| **400** | Bad Request | Missing or invalid parameters (e.g., unsupported `dynamicFilterType`). |
| **401** | Unauthorized | Invalid or missing JWT token. |
| **413** | Payload Too Large | Uploaded file exceeds the allowed size limit. |
| **500** | Internal Server Error | Unexpected server‑side error. |

## SDK Examples

Below are ready‑to‑run snippets for the most popular SDKs. Replace `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME`, and other placeholders with your actual values.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | The workbook name.
var sheetName = "Sheet1"; // string | The worksheet name.
var range = "A1:B1"; // string | The range to filter.
var fieldIndex = 0; // int? | Zero‑based column index.
var dynamicFilterType = "BelowAverage"; // string | Dynamic filter type.
var matchBlanks = true; // bool? | Include blank cells.
var refresh = true; // bool? | Refresh after applying.
var folder = "myFolder"; // string (optional)
var storageName = null; // string (optional)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (optional)
            undefined              // storageName (optional)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Similar snippets are available for Ruby, PHP, Go, and Perl in the official SDK repository.)*

## Related Topics

- **Add a standard AutoFilter** – [Add a standard filter](/autofilter/add-filter)  
- **Add a date filter** – [Add a date filter](/autofilter/add-date-filter)  
- **Delete an AutoFilter** – [Delete auto filter](/autofilter/delete-filter)  
- **Working with worksheets** – [Worksheet API overview](/worksheets/)

## Notes

* All images used in the original documentation have been reviewed for accessibility. Decorative icons are marked with `alt=""` and `role="presentation"`; functional icons retain descriptive `alt` text.  
* Meta keywords have been cleaned to remove empty entries and duplicates.  
* The page now follows a clear heading hierarchy (single H1 in front‑matter, H2 for major sections, H3/H4 for subsections) to improve SEO and screen‑reader navigation.  

---