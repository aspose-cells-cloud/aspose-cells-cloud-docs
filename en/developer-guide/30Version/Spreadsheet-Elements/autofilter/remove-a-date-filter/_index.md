---
title: "Delete a Date Filter – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Delete date filter"
type: docs
url: /autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, delete date filter, Excel AutoFilter, REST API, SDK"
description: "Learn how to delete a date filter from an Excel worksheet using the Aspose.Cells Cloud REST API. Includes endpoint, parameters, HTTPS cURL example, response payload, and SDK code samples."
ArticleTitle: "Delete a Date Filter – Aspise.Cells Cloud API Documentation"
---

## REST API

This REST API deletes a date filter on an Excel worksheet.

**Prerequisites:** Ensure you have a valid JWT token, the workbook is stored in Aspose Cloud storage, and you have appropriate permissions to modify the worksheet.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name       | Type    | Location | Description                                                                                     |
|----------------------|---------|----------|-------------------------------------------------------------------------------------------------|
| name                 | string  | path     | Name of the Excel file.                                                                         |
| sheetName            | string  | path     | Worksheet name.                                                                                 |
| fieldIndex           | integer | query    | Zero‑based index of the column to which the filter is applied.                                 |
| dateTimeGroupingType | string  | query    | Grouping type for the date filter (e.g., Year, Month, Day).                                    |
| year                 | integer | query    | Year component of the filter (default 0).                                                       |
| month                | integer | query    | Month component of the filter (default 0).                                                      |
| day                  | integer | query    | Day component of the filter (default 0).                                                        |
| hour                 | integer | query    | Hour component of the filter (default 0).                                                       |
| minute               | integer | query    | Minute component of the filter (default 0).                                                     |
| second               | integer | query    | Second component of the filter (default 0).                                                     |
| folder               | string  | query    | Folder path in storage where the file is located.                                               |
| storageName          | string  | query    | Name of the Aspose Cloud storage.                                                               |

### **Response**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Http Status Codes**

The API returns standard HTTP status codes indicating the result of the delete operation.

| Code | Meaning | Description |
|------|---------|-------------|
| 200  | OK      | The date filter was successfully deleted; the response contains the operation status. |
| 400  | Bad Request | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized | Invalid or missing JWT token. |
| 413  | Payload Too Large | Uploaded file exceeds size limit. |
| 500  | Internal Server Error | Unexpected server error. |

## How to Use the DeleteWorksheetDateFilter API with SDKs

### DeleteWorksheetDateFilter API Specification

The <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}