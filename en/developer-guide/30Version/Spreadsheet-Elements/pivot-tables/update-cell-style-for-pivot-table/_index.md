---
title: "Update Cell Style for Pivot Table"
second_title: "Document"
linktitle: Format
type: docs
url: /pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, pivot table style, update cell style API, REST API, Excel API, spreadsheet formatting, cloud SDK, cell style, pivot table"
description: "Learn how to update the style of a specific cell in an Aspose.Cells Cloud pivot table via the REST API. Includes endpoint, parameters, authentication, cURL example, Go SDK code snippet, and SEO‑optimized guidance."
weight: 90
ArticleTitle: "Update Cell Style for Pivot Table - Aspose.Cells Cloud API Documentation"
---

This REST API updates the **style** of a cell in a pivot table.

**Prerequisites / Authentication**  
To call this endpoint you must have a valid Aspose Cloud JWT access token. Obtain the token through the OAuth 2.0 flow described in the [Authentication Guide](/authentication/). Include the token in the request header:

```http
Authorization: Bearer <jwt token>
```

The JWT token is required for all Aspose.Cells Cloud API calls.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Request parameters**

| Parameter Name  | Type    | Location | Description                                                                                             |
| --------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------- |
| name            | string  | path     | Document name (required).                                                                               |
| sheetName       | string  | path     | Worksheet name (required).                                                                              |
| pivotTableIndex | integer | path     | Index of the pivot table (required).                                                                    |
| column          | integer | query    | Zero‑based column index of the cell to format (required).                                               |
| row             | integer | query    | Zero‑based row index of the cell to format (required).                                                  |
| style           | object  | body     | Style DTO (data‑transfer object) that defines the new cell style.                                       |
| needReCalculate | boolean | query    | Indicates whether the pivot table should be recalculated after styling. The default value is **false**. |
| folder          | string  | query    | Folder where the document is stored (optional).                                                         |
| storageName     | string  | query    | Name of the storage (optional).                                                                         |
| Method          | string  | N/A      | HTTP method used for the request (**POST**).                                                             |

The <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

**Response**  
On success the service returns HTTP 200 with an empty body indicating that the style has been applied. In case of an error, a JSON payload with an error code and message is returned.

| HTTP Status | Description                                    |
|------------|------------------------------------------------|
| 200        | Style applied successfully.                    |
| 400        | Bad request – e.g., invalid column/row index.  |
| 401        | Unauthorized – missing or invalid JWT token.   |
| 404        | Not found – specified document, worksheet, or pivot table does not exist. |
| 500        | Internal server error – unexpected condition.  |

The response body is empty on success.

For more information, see the **Get Pivot Table** API documentation.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details, allowing you to focus on your business logic. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code example demonstrates how to call Aspose.Cells web services using the **Go** SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Update Cell Style for Pivot Table",
  "description": "Guide to updating the style of a specific cell in an Aspose.Cells Cloud pivot table using the REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, pivot table, cell style, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>