---
title: "Aspose.Cells Cloud SDK for C#: Convert, merge, split, protect, search, replace, and more."
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for C#: Convert, merge, split, protect, search, replace, and more."
type: docs
url: /available-sdks/aspose-cells-cloud-net/
description: "Aspose.Cells Cloud supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Net
---

The SDK is open-source and licensed under the MIT License. You can access the Net library source code for Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **How to use Net library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Net is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Net programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Net to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for Go, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to install the Net package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Net using nuget. Below are the steps for nuget :

```nuget

Install-Package Aspose.Cells-Cloud

```

You can install Aspose.Cells Cloud SDK for Net using dotnet, too. Below are the steps for dotnet :

```powershell

dotnet add package Aspose.Cells-Cloud

```

## How to use Net package to convert Xlsx to PDF

- Import Aspose.Cells Cloud Library
  Begin by importing the necessary package from the Aspose.Cells Cloud DotNet SDK into your project.
- Configure API Client with Credentials
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

### **Sample Code**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}
