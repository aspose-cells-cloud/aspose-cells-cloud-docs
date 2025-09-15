---
title: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and more"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and more"
linktitle: "Developer Center"
type: docs
url: /
description: "Aspose.Cells Cloud Web APIs support Spreadsheet/Excel to create, convert, merge, split, protect, and perform inner object operations, among other functions.  Aspose.Cells Cloud provides a complete document, supports RESTful interfaces, and code examples to help developers quickly integrate."
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Aspose.Cells Cloud Document
---

## What is Aspose.Cells Cloud APIs?

Aspose.Cells Cloud APIs are a set of Spreadsheet/Excel cloud services - no need to install Office, no need to configure servers, just send an HTTP request, and you can perform all common operations such as creating, editing, format conversion, data cleanup, charts, pivot tables, encryption, splitting, merging, watermarks, digital signatures, etc., anywhere and in any language.

## Why use Aspose.Cells Cloud APIs?

- Creating, editing, converting, and analyzing spreadsheets in cloud storage based on Aspose.Cells Cloud Web API services.
- Create, edit, convert, and analyze local spreadsheet files based on Aspose.Cells Cloud Web API services.
- Supported file formats are 30, such as xlsx, csv, ods, xlsb, etc.
- Operate spreadsheets directly through the Aspose.Cells Cloud Web API without the need for Microsoft Excel dependencies.
- Free 150 API calls per month.
- Stepwise charging, how much users use, how much they charge, the more they use, the more discounts they offer.
- **Short-code**:Things that can be done in one sentence.
  - **Convert XLSX to PDF** → ConvertSpreadsheetToPdf
  - **Delete extra spaces in the entire file** → TrimSpreadsheetContent
  - **Combine 10+ files into one report** → MergeSpreadsheets

## **How to use Aspose.Cells Cloud APIs?**

### Step 1: **Get API Credentials**  

- **[Register Aspose Cloud Account](https://dashboard.aspose.cloud/signup)**
- **[Get Client Credentials](https://dashboard.aspose.cloud/#/applications)**

### Step 2: **Call Spreadsheet Web APIs with SDK(recommended)**  

It is recommended to use the official SDK to simplify the authentication and request process.

#### **[Install SDK (using .NET as an example)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

#### Example: **Convert Excel to PDF with SDK**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### Description

- **Spreadsheet**: The Excel file name that must be in the local storage.
- **Format**: Target format. e.g. pdf, png, csv, json, etc.
- **Output file** will be saved to the local location. "EmployeeSalesSummary.pdf" is the output file name.

## **Core Functions**

Aspose.Cells Cloud offers the following key features to meet enterprise-level spreadsheet automation needs:

### **Spreadsheet Convert**

- **[Convert Spreadsheet to PDF file](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**
- **[Convert Spreadsheet Chart to Image](https://docs.aspose.cloud/cells/convert-chart-to-image/)**
- **[Save Spreadsheet As](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **Data Processing**

- **[Merge Spreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Split Spreadsheets](https://docs.aspose.cloud/cells/split-spreadsheet/)**
- **[Delete Spreadsheet blank rows](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[Delete Spreadsheet blank columns](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[Replace Spreadsheet content](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## Support SDKs(**Available SDKs**)

- Aspose.Cells Cloud offers [SDKs](https://github.com/aspose-cells-cloud)** in multiple languages, ready to use:

| Language | Installation Method | GitHub Repository |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Java SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [.NET SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Python SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Node.js SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [PHP SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [GoLang SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Ruby SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Perl SDK GitHub Repository](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API Endpoint**: [Aspose.Cells Cloud Spreadsheet Web API Reference](https://reference.aspose.cloud/cells/)

## **Code examples and open source projects**

All SDKs are open-source and include rich examples:

- [Java SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [.NET SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Python SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [Node.js SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [PHP SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [Go SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [Ruby SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Perl SDK Examples on Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
