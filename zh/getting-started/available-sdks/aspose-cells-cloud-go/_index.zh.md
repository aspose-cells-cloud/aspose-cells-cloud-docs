---
title: Aspose.Cells G 版云 SDK
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/available-sdks/aspose-cells-cloud-go/
description: Aspose.Cells Cloud SDK for Go 为 Go 开发者提供强大的跨平台支持，可轻松集成和使用 Windows、Linux 或 macOS。支持 Excel 创建、转换、合并、拆分、受保护、内部对象操作等
weight: 30
kwords: Go、Excel、Office 云、REST API、图表、数据透视表、表格、电子表格、PDF、CSV、Json、Markdown
---
 SDK 是开源的，并根据 MIT 许可证获得许可。您可以访问 Aspose.Cells Cloud 的 Go 库源代码[这里](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **如何使用Aspose.Cells云的Go库**

Aspose.Cells Cloud SDK for Go 是一个功能强大的库，允许开发人员使用 Go 编程语言操作和处理 Microsoft Excel 文件。借助此 SDK，您可以在云中创建、编辑和转换 Excel 文档，而无需在本地计算机上安装其他软件或依赖项。

在本文中，我们将探讨如何使用 Aspose.Cells Cloud SDK for Go 执行一些常见任务，例如创建一个新的 Excel 工作簿、将数据插入单元格以及将修改后的工作簿保存到云端。

## **入门**

在开始使用 Aspose.Cells Cloud SDK for Go 之前，您需要设置开发环境并安装必要的依赖项。请参阅[文章](https://docs.aspose.cloud/cells/quickstart/)在Aspose网站上获取您的客户端ID和客户端密钥。

## 如何安装 Aspose.Cells Cloud 的 Go 包

您可以使用 `go get` 命令安装 Aspose.Cells Cloud SDK for Go。打开终端或命令提示符并运行以下命令：

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

这会下载并安装最新版本的 SDK 到您的 Go 工作区。


## 如何将 Go 库导入到你的项目中


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## 如何使用 Go 包将 Xlsx 转换为 PDF

- 导入Aspose.Cells云图书馆
首先将 Aspose.Cells Cloud Go SDK 中的必要包导入到您的项目中。
- 使用凭证配置 API 客户端
使用您唯一的客户端 ID 和客户端密钥对您的 API 客户端进行身份验证。
- 准备转换参数
定义转换任务的参数，包括源文件名、所需输出格式和存储文件夹路径。
- 执行工作簿转换
使用 PostConvertWorkbook 方法调用转换过程并处理响应。

### **示例代码**

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
