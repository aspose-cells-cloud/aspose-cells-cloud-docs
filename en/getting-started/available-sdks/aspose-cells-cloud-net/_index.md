---
title: "Aspose.Cells Cloud SDK for C#: Convert, merge, split, protect, search, replace, and more."
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for C#: Convert, merge, split, protect, search, replace, and more."
linktitle: "Aspose.Cells Cloud SDK for .NET"
type: docs
url: /available-sdks/aspose-cells-cloud-net/
description: "Aspose.Cells Cloud .NET SDK provides a cross‑platform API for creating, converting, merging, splitting, protecting, searching and replacing Excel files—no Office installation required."
keywords: "Aspose.Cells, Cloud SDK, .NET, Excel, convert, merge, split, protect, search, replace, API"
weight: 30
---

The SDK is open-source and licensed under the MIT License. You can access the .NET library source code for Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).

# **How to use .NET library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for .NET is a powerful library that allows developers to manipulate and process Microsoft Excel files using the .NET programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for .NET to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for .NET, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

**Prerequisites**  
- .NET 6.0 or later installed.  
- An Aspose Cloud account with a client ID and client secret.  
- Access to a storage location (Aspose Cloud storage or a compatible service).

## How to install the .NET package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for .NET using NuGet. Below are the steps for NuGet :

```nuget
Install-Package Aspose.Cells-Cloud
```

You can install Aspose.Cells Cloud SDK for .NET using dotnet, too. Below are the steps for dotnet :

```powershell
dotnet add package Aspose.Cells-Cloud
```

## How to use .NET package to convert Xlsx to PDF

- Import Aspose.Cells Cloud Library  
  Begin by importing the necessary package from the Aspose.Cells Cloud .NET SDK into your project.  
- Configure API Client with Credentials  
  Authenticate your API client with your unique client ID and client secret.  
- Prepare Conversion Parameters  
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.  
- Execute Workbook Conversion  
  Invoke the conversion process using the `PostConvertWorkbook` method and handle the response.

### **Sample Code**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}