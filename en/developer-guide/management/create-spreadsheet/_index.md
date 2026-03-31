---  
title: "Create Spreadsheet API – Aspose.Cells Cloud (v5.0) | Generate Excel Files"  
second_title: "Document"  
ArticleTitle: "How to Create New Excel Spreadsheets – Generate Blank or Template‑Based Files"  
linktitle: "Create Spreadsheet"  
type: docs  
url: /create-spreadsheet/  
keywords: "create spreadsheet api, Aspose.Cells Cloud, generate Excel, Excel template API, cloud spreadsheet creation, Excel generation API, workbook creator, dynamic spreadsheet API"  
description: "Learn how to create blank or template‑based Excel workbooks with Aspose.Cells Cloud API (v5.0). Includes endpoint, parameters, error codes, authentication steps, and SDK examples."  
weight: 100  
---  

Programmatically create new Excel spreadsheets using Aspose.Cells Cloud API. Generate blank workbooks or instantiate files from custom templates. The RESTful API enables automated Excel file creation, perfect for report generation, document automation, and data‑processing workflows.  

## Prerequisites  

- An active Aspose Cloud account.  
- Configured cloud storage (e.g., **MyDrive**) linked to your Aspose account.  
- A valid API key (client ID and client secret).  

## Authentication  

Aspose.Cells Cloud uses OAuth 2.0. Obtain an access token with the client ID and client secret, then include the token in the **Authorization** header of each request.

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

The response contains the token:

```json
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOi...",
  "expires_in": 3600,
  "token_type": "Bearer"
}
```

Save the `access_token` value and use it as shown in the examples below.  

## **Create Spreadsheet API**  

### Endpoint  

```http
PUT https://api.aspose.cloud/v5.0/cells/spreadsheet/create
```  

### Request Parameters  

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| **format** | String | Query | **Required**. File format for the new spreadsheet (e.g., `XLSX`, `XLS`, `ODS`, `CSV`). |
| **template** | String | Query | **Optional**. Name of a template file stored in your cloud storage (e.g., `invoice_template.xlsx`). If omitted, a blank workbook is created. |
| **outPath** | String | Query | **Optional**. Target folder path in cloud storage for the generated file. If `null` or omitted, the spreadsheet is saved to the default location. |
| **outStorageName** | String | Query | **Required**. Identifier of the configured cloud storage (e.g., `MyDrive`). |
| **region** | String | Query | **Optional**. Locale setting (e.g., `fr-FR`) that determines default date, number, and currency formats. |
| **password** | String | Query | **Optional**. Password for an encrypted template file. Leave empty if the template is not protected. |

### Response  

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```  

### Error Codes  

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid access token or incorrect client ID/secret.  
- **404 Not Found** – The specified spreadsheet or template file is not accessible.  
- **500 Server Error** – An internal error occurred while processing the request.  

### Sample cURL Request  

```bash
curl -X PUT "https://api.aspose.cloud/v5.0/cells/spreadsheet/create?format=XLSX&outPath=NewBook.xlsx&outStorageName=MyDrive" \
     -H "Authorization: Bearer $ACCESS_TOKEN"
```  

### Rollback / Cleanup  

To delete a spreadsheet that was created unintentionally, call the **Delete File** endpoint:

```bash
curl -X DELETE "https://api.aspose.cloud/v5.0/storage/file/NewBook.xlsx?storageName=MyDrive" \
     -H "Authorization: Bearer $ACCESS_TOKEN"
```  

## Where should we use the Create Spreadsheet API?  

- **Initialization of the Automated Reporting System** – Create a new blank workbook or generate a report file from a standard template at the start of each daily/weekly automation cycle.  
- **User Self‑service Portal** – Allow customers to select a template (quotation, project schedule, etc.) and instantly download a customized Excel file.  
- **Batch Data Export and Distribution** – Produce separate workbooks with a uniform format for each exported data set, simplifying downstream distribution and processing.  

## Why should you use the Create Spreadsheet API?  

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and providing comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces development effort.  
- **Reduced Labor Costs** – Eliminates the need for dedicated staff to consolidate documents manually.  
- **Pay‑per‑Use** – No upfront investment; you only pay for the API calls you actually use.  
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility concerns.  

## How to Use the Create Spreadsheet API with SDKs  

### Create Spreadsheet API Specification  

The [Create Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.  

### Use Aspose.Cells Cloud SDKs  

Using an SDK is the fastest way to develop, as it abstracts low‑level details and lets you build the spreadsheet with concise code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.  

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}