---  
title: "Aspose.Cells Cloud SDK for Go: Convert, merge, split, protect, search, replace, and more"  
second_title: "Document"  
ArticleTitle: "Aspose.Cells Cloud SDK for Go: Convert, merge, split, protect, search, replace, and more"  
linktitle: "Aspose.Cells Cloud SDK for Go"  
type: docs  
url: /available-sdks/aspose-cells-cloud-go/  
description: "Learn how to install, import, and use Aspose.Cells Cloud SDK for Go. Step‑by‑step guide with code samples, authentication, and best practices."  
weight: 30  
keywords: "Aspose.Cells Cloud Go SDK, Go Excel API, Aspose Cells Go example"  
---  

The SDK is open‑source and licensed under the MIT License. You can access [the Go library source code for Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **How to use Go library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Go is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Go programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud without installing additional software or dependencies on your local machine.

In this article, we’ll explore how to use Aspose.Cells Cloud SDK for Go to perform common tasks such as creating a new workbook, inserting data into cells, and saving the modified workbook to the cloud.

## **Getting Started**

Before you can start using Aspose.Cells Cloud SDK for Go, set up your development environment and install the required dependencies. Refer to the [Aspose quick‑start guide](https://docs.aspose.cloud/cells/quickstart/) to obtain your client ID and client secret.

### Prerequisites (included here for quick reference)

* Go 1.20 or later  
* Internet connectivity to download the SDK module  
* Your Aspose Cloud **client‑id** and **client‑secret**  

## How to install the Go package for Aspose.Cells Cloud

Run the following command (note the version suffix **/v25**) to install the latest v25 module:

```bash
go install github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25@latest
```

## How to import the Go library into your project

```go
package main

import (
    . "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25"
)
```

## How to get started with Aspose.Cells Cloud for Go – follow these steps

1. **Create an Aspose Cloud account** and obtain your **client ID** and **client secret**.  
2. **Create a project directory** and add a `main.go` file.  
3. **Initialize the module** and fetch dependencies:

   ```bash
   go mod init myproject
   go mod tidy
   ```

4. **Add runnable code** (see the sample below).  
5. **Run the application**:

   ```bash
   go run main.go
   ```

### Sample Code (embedded)

```go
package main

import (
    "context"
    "log"

    asposecells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25"
)

func main() {
    // Configure authentication
    cfg := asposecells.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "YOUR_CLIENT_ID")
    cfg.AddDefaultHeader("client-secret", "YOUR_CLIENT_SECRET")

    // Create an API client
    apiClient := asposecells.NewAPIClient(cfg)

    // Example: create a new workbook named Sample.xlsx
    ctx := context.Background()
    _, err := apiClient.CellsApi.PutCreateWorkbook(ctx, "Sample.xlsx", nil)
    if err != nil {
        log.Fatalf("Error creating workbook: %v", err)
    }
    log.Println("Workbook created successfully.")
}
```

*The original gist can be viewed on GitHub [here](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

---  