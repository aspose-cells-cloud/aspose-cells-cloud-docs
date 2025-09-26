---
title: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more."
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js: Convert, merge, split, protect, search, replace, and more."
linktitle: "Aspose.Cells Cloud SDK for Node.js"
type: docs
url: /available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK for Node.js offers true cross-platform power: one import provides Windows, Linux, and macOS developers with the same fluent API to create, convert, merge, split, protect, and manipulate every Excel object—no Office installation is required, and no platform-specific tweaks are needed."
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK for Node.js, Cloud SDK for Node.js, REST, Chart, Pivot Table, Table/List Object, Convert Spreadsheet, PDF, CSV, Json, Markdown, Merge, Split, Protect, Search, Replace
---

The SDK is open-source and licensed under the MIT License. You can access [the Node library source code for Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **How to use Node library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Node is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Node programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Node to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for Go, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to install the Node package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Node using npm. Below are the steps for npm:

```Powershell

npm install asposecellscloud

```

## How to add dependencies in package configuration for Aspose.Cells Cloud

node configuration file : package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
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
