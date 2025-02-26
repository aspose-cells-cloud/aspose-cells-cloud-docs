---
title: "Aspose.Cells Cloud SDK for Ruby"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /available-sdks/aspose-cells-cloud-ruby/
description: "Aspose.Cells Cloud supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Ruby
---

The SDK is open-source and licensed under the MIT License. You can access the Ruby library source code for Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby).

# **How to use Aspose.Cells Cloud SDK for Ruby**

Aspose.Cells Cloud SDK for Ruby is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Ruby programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Ruby to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for Go, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to install the Ruby package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Ruby by the command below:

```bash

    gem install aspose_cells_cloud
  
 ```

## How to use Ruby package to convert Xlsx to PDF

- Import Aspose.Cells Cloud Library
  Begin by importing the necessary package from the Aspose.Cells Cloud Python SDK into your project.
- Configure API Client with Credentials
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

```Ruby
require 'openssl'
require 'bundler'
require 'aspose_cells_cloud'

@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'],'v3.0',ENV['CellsCloudApiBaseUrl'])

local_name = 'Book1.xlsx'
remote_name = 'Book1.xlsx'
format = "pdf"
    
mapFiles = { }   
mapFiles[local_name]= ::File.open(File.expand_path("TestData/"+local_name),"r")
request =   AsposeCellsCloud::PutConvertWorkbookRequest.new(:File=>mapFiles,:format=>format);
@instance.put_convert_workbook(request);

```
