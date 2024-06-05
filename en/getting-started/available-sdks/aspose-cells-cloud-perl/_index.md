---
title: "Aspose.Cells Cloud SDK for Perl"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /available-sdks/aspose-cells-cloud-perl/
description: "Aspose.Cells Cloud supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Perl
---

The SDK is open-source and has an MIT license. You can get the Node library source code about Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).


# **How to use Perl library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Perl is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Perl programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Perl to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using Aspose.Cells Cloud SDK for Perl, you'll need to set up your development environment and install the necessary dependencies. You can refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to get your client ID and client secret.

## How to install the Perl package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Perl by the command below:

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## How to use Perl package to convert Xlsx to PDF

- Import Aspose.Cells Cloud Library
  Begin by importing the necessary package from the Aspose.Cells Cloud Perl SDK into your project.
- Configure API Client with Credentials
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

```Perl
use lib 'lib';
use strict;
use warnings;
use File::Slurp;
use MIME::Base64;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'CellsCloudClientId'}, client_secret => $ENV{'CellsCloudClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $remoteFolder = 'TestData/In';
  
my $localName = 'Book1.xlsx';
my $remoteName = 'Book1.xlsx';

my $upload_file_request = AsposeCellsCloud::Request::UploadFileRequest->new( 'UploadFiles'=>{ $localName => $localName  }  ,'path'=>$remoteFolder . '/' . $remoteName );
 
my $format = 'csv';

my $mapFiles = {};           

 $mapFiles->{$localName}= "TestData/".$localName ;

my $request = AsposeCellsCloud::Request::PutConvertWorkbookRequest->new();
$request->{file} =  $mapFiles;
$request->{format} =  $format;
$instance->put_convert_workbook(request=> $request);
```
