---
title: "How to merge multiple files through Aspose.Cells Cloud"
linktitle: "How to merge multiple files"
type: docs
url: /how-to-merge-multiple-files
description: "How to merge multiple files through Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, How to merge multiple files through Aspose.Cells Cloud
---

## Introduction

The Aspose.Cells Cloud API is a potent cloud-based solution crafted for the creation, editing, and conversion of spreadsheet files. In this article, we will walk you through the process of using the Aspose.Cells Cloud API for file format merged, including typical use cases and example code.

## Overview

The Aspose.Cells Cloud API provides two robust APIs for merge multiple spreadsheet files into a file with kind of formats. The supported formats include **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF**, and more. By leveraging the Aspose.Cells Cloud API, you can effortlessly merge multiple spreadsheet files into a file with widely used formats, catering to a diverse range of requirements.

Numerous APIs are available for file merged, generally compatible with various online environments. Below is a detailed description of these APIs:

- **[Merge multi Excel files into an Excel file.](https://reference.aspose.cloud/cells/#/LightCells/PostMerge)**. For guidance on how to call this API, please refer to the  [development guide](https://docs.aspose.cloud/cells/merge/multi-files/).
- **[Merge an Excel Workbooks into other Excel file](https://reference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge)**. For guidance on how to call this API, please refer to the  [development guide](https://docs.aspose.cloud/cells/workbook/merge/).

# How to merge multiple files a file through Aspose.Cells Cloud

The Aspose.Cells Cloud API provides [multiple SDKs](https://github.com/aspose-cells-cloud) for different programming languages. Choose the SDK that aligns with your preferred programming language and follow the accompanying documentation for installation and initialization. Alternatively, you can craft your own SDK according to the [API reference](https://reference.aspose.cloud/cells/). In this section, we'll use C# as an example to detail the process of file merged.

## Registration and Obtaining API Key

Before getting started, you need to [register an Aspose Cloud account](https://id.containerize.com/signup) and [obtain an API key for authentication](https://dashboard.aspose.cloud/applications). By logging into the official Aspose Cloud website, you can create a free account and obtain an API key for authentication purposes.

For more in-depth operations, please refer to the following documents: [Quick Start with Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Installing and Initializing the Aspose.Cells Cloud SDK

Install the Aspose.Cells-Cloud NuGet package in your .NET project, you can use the NuGet Package Manager Console or the NuGet Package Manager in Visual Studio.
Here's how you can install the package using the Package Manager Console:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Creates a new instance of the CellsApi class, initializing it with your client ID and client secret. Below are the details of the aforementioned code snippet:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Make sure to replace YOUR_API_KEY, YOUR_APP_SID, and YOUR_APP_KEY with your actual API key, application SID, and application key.

## Construct the API Request and Call the API

This creates a new instance of the PostMergeRequest, initializing it with your desired file format and files. It then calls the merged API with this merge request. The merged function supports extended query parameters, too. Below are the details of the aforementioned code snippet:

```CSharp

using System.Collections.Generic;

PostMergeRequest request = new PostMergeRequest();

request.Format = "pdf";
request.mergeToOneSheet = true;
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

cellsInstance.PostMerge(request);

```

## Use Cases

The multiple files **merged** feature of the Aspose.Cells Cloud API is useful in various practical use cases. Here are some common scenarios:

- **Merge multiple Excel files into an Excel file** for data analysis and storage.
- **Merge data files into an Excel file** for data analysis.
- **Merge multiple images files into a PDF file** for easy sharing.
- **Merge multiple files into a html file** for display and embedding in web pages.

## Conclusion

With Aspose.Cells Cloud API, you can easily perform merged into a file for multiple spreadsheet files. By making simple API calls and setting appropriate merged options, you can efficiently fulfill various file merged requirements. Integrate Aspose.Cells Cloud API into your applications to enhance productivity and save development time.

Please note that the above example code is for demonstration purposes only, and you would need to replace it with valid authentication credentials and file paths when using it in practice. Additionally, Aspose.Cells Cloud API offers many other features, such as spreadsheet creation, editing, manipulation, and data processing. Detailed API documentation and example code can be found on [developer guide of the official Aspose website](/developer-guide/).

We hope this article helps you understand how to use Aspose.Cells Cloud API for file merge. Best of luck with your implementation!
