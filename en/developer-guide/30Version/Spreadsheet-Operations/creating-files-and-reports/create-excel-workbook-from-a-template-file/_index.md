---  
title: "How to Create an Excel Workbook with a Template File"  
second_title: "Document"  
linktitle: "Template File"  
type: docs  
url: /create-an-excel-file-with-template-file/  
aliases:  
  - /create-excel-workbook-from-a-template-file/  
  - /workbook/new-from-a-template-file/  
  - /workbook/create/template-file/  
keywords: "Excel template API, Aspose.Cells create workbook, Excel workbook template, REST API, Aspose.Cells Cloud"  
description: "Learn how to generate Excel workbooks from template files using the Aspose.Cells Cloud REST API. Includes prerequisites, authentication steps, cURL examples, error‑handling details, and SDK code snippets."  
weight: 30  
---  

**Prerequisites**  

Before calling the API, complete the following steps:

1. **Obtain an access token** – request a JWT/OAuth token from the `/connect/token` endpoint.  
2. **Upload the template file** (`templateFile`) and the data file (`dataFile`) to your Aspose Cloud storage.  
3. (Optional) Note the **storage name** and **folder path** if you are using a custom storage service.

### Authentication  

All API calls must include the `Authorization` header:

```http
Authorization: Bearer {access_token}
```

Replace `{access_token}` with the token obtained in the previous step.

---  

This REST API creates a **workbook** from a **template file**. It generates a new Excel workbook based on the supplied template and data.

### Query Parameters  

**Query Parameters** – key‑value pairs that control workbook creation.

| Parameter Name | Type    | Description |
|----------------|---------|-------------|
| `templateFile` | string  | Name of the template file stored in the cloud. |
| `dataFile`     | string  | Name of the data file (e.g., XML, JSON) used to populate the template. |
| `isWriteOver`  | boolean | Flag indicating whether to overwrite an existing file. Pass `true` or `false` **without** quotes. |
| `folder`       | string  | Folder path where the original workbook resides. |
| `storageName`  | string  | Name of the storage service. |

### Request Body Parameter  

**Request Body** – contains the data file for Smart‑Marker placeholders.  

| Parameter Name | Type | Description |
|----------------|------|-------------|
| `data`         | file | File containing the data for the **smart‑marker** template (XML or JSON). |

> **Smart‑marker**: a placeholder syntax that Aspose.Cells replaces with values from the supplied data file.

## REST API  

**REST API** – endpoint that creates the workbook.

| **API**          | **Type** | **Description**                                 | **Swagger Link** |
|------------------|----------|-------------------------------------------------|------------------|
| `/cells/{name}`  | PUT      | Create a new Excel workbook from a template file | [PutWorkbookCreate](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&dataFile=Sample_Data.xml&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "OK",
  "Workbook": {
    "FileName": "newworkbook.xlsx",
    "Links": [
      {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Names": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Settings": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "IsWriteProtected": "false",
    "IsProtected": "false",
    "IsEncryption": "false",
    "Password": ""
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Error Handling  

| HTTP Status | Meaning                         | Example Body |
|-------------|---------------------------------|--------------|
| **200**     | Workbook created successfully   | `{ "Status": "OK", "Workbook": { … } }` |
| **400**     | Bad request – missing/invalid parameters | `{ "error": "Invalid isWriteOver value." }` |
| **401**     | Unauthorized – invalid or missing token | `{ "error": "Authentication required." }` |
| **404**     | Not found – template or data file not found | `{ "error": "File not found." }` |
| **500**     | Internal server error           | `{ "error": "Unexpected server error." }` |

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details, letting you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateTemplate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateTemplate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateTemplate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateTemplate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateTemplate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateTemplate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateTemplate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateTemplate.go" >}}

{{< /tab >}}

{{< /tabs >}}