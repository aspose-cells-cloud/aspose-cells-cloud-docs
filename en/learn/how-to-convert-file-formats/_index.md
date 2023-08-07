---
title: "How to convert file formats through Aspose.Cells Cloud"
type: docs
url: /how-to-convert-file-formats
description: "How to convert file formats through Aspose.Cells Cloud."
weight: 10
---

## Introduction
The Aspose.Cells Cloud API is a potent cloud-based solution crafted for the creation, editing, and conversion of spreadsheet files. In this article, we will walk you through the process of using the Aspose.Cells Cloud API for file format conversion, including typical use cases and example code.

## Overview

The Aspose.Cells Cloud API provides a robust set of APIs for converting spreadsheet files between different formats. The supported formats include **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF**, and more. By leveraging the Aspose.Cells Cloud API, you can effortlessly convert spreadsheet files to other widely used formats, catering to a diverse range of requirements.

Numerous APIs are available for file conversion, generally compatible with various online environments. Below is a detailed description of these APIs:

- **[Get an Excel file with the specified format](https://reference.aspose.cloud/cells/#/Conversion/GetWorkbook)**. For guidance on how to call this API, please refer to the  [development guide](https://docs.aspose.cloud/cells/export-different-formats/).
- **[Convert Excel file to other format file](https://reference.aspose.cloud/cells/#/Conversion/PutConvertWorkbook)**. For guidance on how to call this API, please refer to the  [development guide](https://docs.aspose.cloud/cells/convert/excel-to-different-formats/).
- **[Save Excel file as other format file](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs)**. For guidance on how to call this API, please refer to the  [development guide](https://docs.aspose.cloud/cells/saveas-other-formats/).
- **[Export Excel files](https://reference.aspose.cloud/cells/#/LightCells/PostExport)**. For guidance on how to call this API, please refer to the [development guide](https://docs.aspose.cloud/cells/export/excel-to-different-formats/).


# How to convert file formats through Aspose.Cells Cloud

The Aspose.Cells Cloud API provides [multiple SDKs](https://github.com/aspose-cells-cloud) for different programming languages. Choose the SDK that aligns with your preferred programming language and follow the accompanying documentation for installation and initialization. Alternatively, you can craft your own SDK according to the [API reference](https://reference.aspose.cloud/cells/). In this section, we'll use C# as an example to detail the process of file conversion.


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

## Construct the API Request and Call the API.

This creates a new instance of the PutConvertWorkbookRequest, initializing it with your desired file format and files. It then calls the conversion API with this conversion request. Below are the details of the aforementioned code snippet:


```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;

cellsInstance.PutConvertWorkbook(request);

```

The Convert function includes a lesser-known feature: extended query parameters. This feature primarily serves to allow for the setting of additional saving parameters to cater to the diverse needs of customers. Specific parameters can be saved in the corresponding format according to the Aspose.Cells API reference, such as the PDFSaveOptions.

So, how do you set these extended query parameters? Let's explore the following code snippet:

```CSharp

using System.Collections.Generic;

PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();

request.Format = "pdf";
IDictionary<string, System.IO.Stream> mapFiles =new Dictionary<string, System.IO.Stream>(); 
mapFiles.Add("Book1.xlsx", File.OpenRead(@"c:\testdata\Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead(@"c:\testdata\Book2.xlsx"));
request.Files = mapFiles;
request.extendQueryParameterMap = new  Dictionary<string, string>();
request.extendQueryParameterMap.Add("OnePagePerSheet","false");
request.extendQueryParameterMap.Add("CalculateFormula","true");
cellsInstance.PutConvertWorkbook(request);

```

## Use Cases

The file **format conversion** feature of the Aspose.Cells Cloud API is useful in various practical use cases. Here are some common scenarios:

- **Convert Excel files to PDF format** for sharing and printing across different devices.
- **Convert spreadsheet files to HTML format** for display and embedding in web pages.
- **Convert CSV files to Excel format** for further editing and analysis in spreadsheet applications.
- **Convert spreadsheet files to other formats** to meet specific business requirements or data exchange needs.

## Conclusion

With Aspose.Cells Cloud API, you can easily perform file format conversions for spreadsheet files, whether it's converting **Excel** files to **PDF**, **HTML**, or converting **CSV** files to **Excel** format. By making simple API calls and setting appropriate conversion options, you can efficiently fulfill various file format conversion requirements. Integrate Aspose.Cells Cloud API into your applications to enhance productivity and save development time.

Please note that the above example code is for demonstration purposes only, and you would need to replace it with valid authentication credentials and file paths when using it in practice. Additionally, Aspose.Cells Cloud API offers many other features, such as spreadsheet creation, editing, manipulation, and data processing. Detailed API documentation and example code can be found on [developer guide of the official Aspose website](/developer-guide/).

We hope this article helps you understand how to use Aspose.Cells Cloud API for file format conversion. Best of luck with your implementation!

