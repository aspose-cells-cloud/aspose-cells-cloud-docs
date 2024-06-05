---
title: "Aspose.Cells Cloud SDK for PHP"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /available-sdks/aspose-cells-cloud-php/
description: "Aspose.Cells Cloud supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, PHP
---

The SDK is open-source and has an MIT license. You can get the Node library source code about Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **How to use Aspose.Cells Cloud SDK for PHP**

Aspose.Cells Cloud SDK for PHP is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Go programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for PHP to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using Aspose.Cells Cloud SDK for Perl, you'll need to set up your development environment and install the necessary dependencies. You can refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to get your client ID and client secret.

## How to install the PHP package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for PHP. Below are the steps:

- Add Aspose.Cells Cloud as a dependency to your `composer.json` file:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Run Composer update to install the SDK:

   ```bash

   composer install

   ```

- Include Composer's autoloader in your PHP code:

   ```php

   require 'vendor/autoload.php';

   ```

## How to use PHP package to convert Xlsx to PDF

- Import Aspose.Cells Cloud Library
  Begin by importing the necessary package from the Aspose.Cells Cloud PHP SDK into your project.
- Configure API Client with Credentials
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```
