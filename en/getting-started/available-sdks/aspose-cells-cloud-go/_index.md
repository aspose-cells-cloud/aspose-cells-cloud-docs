---
title: "Aspose.Cells Cloud SDK for Go"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /available-sdks/aspose-cells-cloud-go/
description: "Aspose.Cells Cloud SDK for Go provides strong cross-platform support for Go developers, making it easy to integrate and use for Windows, Linux, or macOS. It supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 30
kwords: Go, Excel, Office Cloud, REST API, Chart, Pivot Table, Table, Spreadsheet, PDF, CSV, Json, Markdown
---


The SDK is open-source and licensed under the MIT License. You can access the Go library source code for Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **How to use Go library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Go is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Go programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Go to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## **Getting Started**

Before you can start using the Aspose.Cells Cloud SDK for Go, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to install the Go package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Go using the `go get` command. Open your terminal or command prompt and run the following command:

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

This will download and install the latest version of the SDK to your Go workspace.


## How to import Go library into your project


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## How to use Go package to convert Xlsx to PDF

- Import Aspose.Cells Cloud Library
  Begin by importing the necessary package from the Aspose.Cells Cloud Go SDK into your project.
- Configure API Client with Credentials
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

### **Sample Code**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```
