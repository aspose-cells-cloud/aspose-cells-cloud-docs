---  
title: "Aspose.Cells Cloud PHP SDK – Convert, Merge, Split, Protect Excel Files"  
second_title: "Document"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Convert, Merge, Split, Protect Excel Files"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /available-sdks/aspose-cells-cloud-php/  
description: "Download the Aspose.Cells Cloud PHP SDK (v24.3). Learn how to install via Composer, authenticate, convert XLSX to PDF/CSV, merge workbooks, protect sheets, and more – all without installing Office."  
keywords: "Aspose.Cells, Cloud, PHP, SDK, Excel, Convert, Merge, Split, Protect"  
weight: 30  
---  

The SDK is open-source and licensed under the MIT License. You can access the PHP library source code for Aspose.Cells Cloud <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">here</a>.

# **How to use Aspose.Cells Cloud SDK for PHP**

Aspose.Cells Cloud SDK for PHP is a powerful library that allows developers to manipulate and process Microsoft Excel files using the **PHP programming language**. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for PHP to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for **PHP**, you need to set up your development environment and install the necessary dependencies. Refer to <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">the article</a> on the Aspose website to obtain your client ID and client secret.

**Prerequisites**

- PHP 7.4 or later  
- Composer installed on your development machine  
- Valid Aspose Cloud client ID and client secret  
- Access to an Aspose Cloud storage location (default or custom)  

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

## How to use PHP package to convert Xlsx to other formats

- Import Aspose.Cells Cloud Library  
  Begin by importing the necessary package from the Aspose.Cells Cloud PHP SDK into your project.

- Configure API Client with Credentials  
  Authenticate your API client with your unique client ID and client secret.

- Prepare Conversion Parameters  
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.

- Execute Workbook Conversion  
  Invoke the conversion process using the `PostConvertWorkbook` method and handle the response.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### API Reference for `PostConvertWorkbook`

| Parameter      | Description                                   | Type   | Required |
|----------------|-----------------------------------------------|--------|----------|
| `file`         | Name of the source Excel file (e.g., `sample.xlsx`). | string | Yes |
| `format`       | Desired output format (`pdf`, `csv`, `png`, etc.). | string | Yes |
| `storage`      | Storage name or folder path where the source file resides. | string | No |
| `outPath`      | Optional path to save the converted file directly in storage. | string | No |

**HTTP Method:** POST  
**Endpoint:** `/cells/convert/{format}`  

**Response Example (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**Status Codes**

- `200` – Conversion successful.  
- `400` – Bad request (missing or invalid parameters).  
- `401` – Authentication failed.  
- `500` – Server error.  