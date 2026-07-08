---
title: "Hide pivot field item in a pivot table"
second_title: "Document"
linktitle: Hide
type: docs
url: /pivot-tables/hide-pivot-field-item/
aliases: [/hide-pivot-field-item/]
keywords: "Aspose.Cells, hide pivot field item, PivotTable API, REST API, cloud SDK"
description: "Learn how to hide a pivot field item in a pivot table using Aspose.Cells Cloud REST API. Includes request details, cURL example, and SDK code snippets for multiple languages."
weight: 110
ArticleTitle: "Hide Pivot Field Item in a Pivot Table – Aspose.Cells Cloud API Guide"
---

Before calling the API, ensure you have:

* A valid **JWT access token** (obtainable via the Aspose Cloud authentication flow).  
* The target workbook uploaded to your Aspose Cloud storage.  
* The worksheet and pivot table already created.

These prerequisites prevent authentication errors and “resource not found” responses.

This REST API hides a pivot field item in a pivot table.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Request parameters**

| Parameter Name  | Type    | Location | Description                                                                                      |
| --------------- | ------- | -------- | ------------------------------------------------------------------------------------------------ |
| name            | string  | path     | Name of the Excel file.                                                                          |
| sheetName       | string  | path     | Worksheet that contains the pivot table.                                                         |
| pivotTableIndex | integer | path     | Index of the pivot table within the worksheet.                                                   |
| pivotFieldType  | string  | query    | Type of the pivot field (Row, Column, Page, Data, etc.).                                         |
| fieldIndex      | integer | query    | Zero‑based index of the pivot field to modify.                                                   |
| itemIndex       | integer | query    | Index of the specific item within the field to hide.                                             |
| isHide          | boolean | query    | Set to **true** to hide the item; **false** to show it.                                          |
| needReCalculate | boolean | query    | Indicates whether the pivot table should be recalculated after the change. Default is **false**. |
| folder          | string  | query    | Folder path where the workbook is stored.                                                        |
| storageName     | string  | query    | Name of the storage service.                                                                     |

**Quick reference of required query parameters**

- **pivotFieldType** – type of the field (e.g., `Row`).  
- **fieldIndex** – zero‑based index of the field to modify.  
- **itemIndex** – zero‑based index of the item to hide/show.  
- **isHide** – `true` to hide, `false` to show.  
- **needReCalculate** – optional, defaults to `false`.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
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
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Response details**

| Status Code | Description                              |
| ----------- | ---------------------------------------- |
| 200         | The item was hidden successfully.       |
| 400         | Bad request – missing or invalid parameters. |
| 401         | Unauthorized – invalid or missing JWT token. |
| 500         | Server error – the operation could not be completed. |

## Cloud SDK Family

Using an SDK is the fastest way to develop against the API. SDKs handle low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to hide a pivot field item using various SDKs.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Prepare the workbook and worksheet
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Upload the workbook
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Create the worksheet that will contain the pivot table
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Create a second worksheet with sample data
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Import sample data into Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Truncated for brevity
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Add a pivot table to PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Hide a specific row field item
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}