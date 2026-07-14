---
title: "Aspose.Cells Cloud SDK for Perl – Convert, Merge, Split, Protect & More"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for Perl – Convert, Merge, Split, Protect & More"
linktitle: "Aspose.Cells Cloud SDK for Perl"
type: docs
url: /available-sdks/aspose-cells-cloud-perl/
description: "Explore the Aspose.Cells Cloud Perl SDK – a cross‑platform library to create, convert, merge, split, protect, search and replace Excel files without Office installed."
weight: 30
keywords: "Perl, Aspose.Cells Cloud, Excel SDK, conversion, PDF, API"
---

The SDK is open-source and licensed under the MIT License. You can access the Perl library source code for Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **How to use Perl library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Perl is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Perl programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Perl to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for Go, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to install the Perl package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Perl by the command below:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## How to use Perl package to convert Xlsx to other formats

- Import Aspose.Cells Cloud Library
  Begin by importing the necessary package from the Aspose.Cells Cloud Perl SDK into your project.
- Configure API Client with Credentials
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}
