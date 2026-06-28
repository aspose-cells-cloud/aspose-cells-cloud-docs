---
title: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more"
linktitle: "Aspose.Cells Cloud SDK for Node.js"
type: docs
url: /available-sdks/aspose-cells-cloud-node/
description: "The Aspose.Cells Cloud SDK for Node.js provides a cross‑platform, fluent API for creating, converting, merging, splitting, protecting, searching, and replacing Excel files in the cloud without requiring Microsoft Office."
weight: 30
keywords: "Aspose.Cells Cloud, Node.js SDK, Excel SDK, spreadsheet conversion, merge Excel, split workbook, protect Excel, search replace Excel, REST API"
---

The SDK is open-source and licensed under the MIT License. You can access [the Node library source code for Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

## **How to use Node library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Node is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Node programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Node to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for Node, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to install the Node package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Node using npm. Below are the steps for npm:

```Powershell
npm install asposecellscloud
```

## How to add dependencies in package configuration for Aspose.Cells Cloud

Node configuration file: package.json

```Node
{
  "name": "asposecellscloud",
  "version": "26.5.0",
  "description": "Aspose.Cells Cloud is a REST API for creating and editing Excel files. Most popular features: Excel to PDF, Convert to Image, Merge workbooks, Split worksheets, Data processing with formulas and pivot tables. It can also be used to convert spreadsheets between various formats (XLSX, CSV, JSON, ODS, HTML) without any local office software.",
  "keywords": [
    "excel",
    "spreadsheet",
    "convert",
    "xlsx",
    "Aspose",
    "Cloud",
    "Cells",
    "PowerPoint",
    "PPTX",
    "PPT",
    "Conversion",
    "Merge",
    "PDF",
    "Export",
    "Html",
    "Css",
    "Rest",
    "Api",
    "Image"
  ],
  "author": "Aspose Nanjing Team",
  "license": "MIT",
  "engines": {
    "node": ">=4.8"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/aspose-cells-cloud/aspose-cells-cloud-node.git"
  },
  "main": "dist/api.js",
  "types": "dist/api.d.ts",
  "scripts": {
    "test": "cross-env JUNIT_REPORT_PATH=integration_tests_result.xml mocha -r ts-node/register test/**/*.ts --timeout 250000 --reporter mocha-jenkins-reporter",
    "test-jenkins": "cross-env JUNIT_REPORT_PATH=reports/integration_tests_result.xml mocha -r ts-node/register test/**/*.ts --timeout 250000 --reporter mocha-jenkins-reporter",
    "lint": "tslint src/{,**/}*.ts test/{,**/}*.ts -t verbose --project ./tsconfig.json",
    "cucumber": "cucumber-js ./bdd/features -r ./dist/bdd/steps",
    "gulp": "gulp"
  },
  "dependencies": {
    "@types/jest": "^26.0.24",
    "@types/request": "^2.48.7",
    "request": "^2.88.2",
    "request-debug": "^0.2.0"
  },
  "devDependencies": {
    "@types/chai": "^4.2.22",
    "@types/mocha": "^2.2.44",
    "@types/node": "^8.10.66",
    "chai": "^4.3.7",
    "cross-env": "^5.1.4",
    "cucumber": "^3.0.0",
    "del": "^3.0.0",
    "gulp": "^3.9.1",
    "gulp-cucumber": "0.0.23",
    "gulp-typescript": "^2.12.2",
    "gulp-util": "^1.0.0",
    "mocha": "^10.8.2",
    "mocha-cases": "^0.2.1",
    "mocha-jenkins-reporter": "^0.4.7",
    "mocha-sinon": "^2.0.0",
    "sinon": "^7.0.0",
    "ts-node": "^4.1.0",
    "tslint": "^5.8.0",
    "typescript": "^2.9.2"
  },
  "bugs": {
    "url": "https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/issues"
  },
  "homepage": "https://github.com/aspose-cells-cloud/aspose-cells-cloud-node#readme",
  "directories": {
    "doc": "docs",
    "test": "test"
  }
}

```

## How to use Node package to convert Xlsx to other formats

- Import Aspose.Cells Cloud Library  
  Begin by importing the necessary package from the Aspose.Cells Cloud NodeJS SDK into your project.
- Configure API Client with Credentials  
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters  
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion  
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
