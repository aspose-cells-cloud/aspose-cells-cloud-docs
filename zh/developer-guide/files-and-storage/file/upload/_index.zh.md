---
title: 上传文件
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/file/upload/
keywords: Learn how to upload file with Aspose Cells Cloud REST API
description: 了解如何使用 Aspose Cells Cloud REST API SDK 支持多种开发语言上传文件。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 100
---
这个REST API表示`upload file`。

## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|上传的路径，包括文件名和扩展名，例如 /file.ext 或 /Folder 1/file.ext 如果内容是多部分的并且路径不包含文件名，它将尝试从 Content-Disposition 标头的文件名参数中获取它们。|
|文件|文件|表单数据|要上传的文件|
|存储名称|细绳|询问|存储名称|
 
这[开放API规范](https://apireference.aspose.cloud/cells/#/File/UploadFile)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用cURL命令行工具轻松访问Aspose.Cells Web服务。以下示例展示如何使用 cURL 呼叫云端 API。
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## 云SDK系列
 
使用 SDK 是加快开发速度的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。
 
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
 {{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

```csharp

CellsApi cellsApi = new CellsApi(ClientId, ClientSecret);
cellsApi.UploadFile("DotNetSDK/OutResult/Upload_Book1.xlsx", File.OpenRead(filePath), null);

```

{{< /tab >}}

{{< tab tabNum="2" >}}
```java

    public static void main(String[] args) {
        try{
            CellsApi  cellsApi = new CellsApi(System.getenv("ProductClientId"),System.getenv("ProductClientSecret"));
            File file = new File("TestImportData.xlsx");
            cellsApi.uploadFile("JavaSDK/OutResult/Book1.xlsx", file, null);
        }
        catch( Exception e) 
        {
            System.out.print(e.getMessage());
        }
    }
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
$cells = new CellsApi( getenv("ProductClientId"),getenv("ProductClientSecret") );
$cells->uploadFile("PHPSDK/OutResult/UploadFile_Book1.xlsx","D:/projects/aspose/examples/testdata/source/Book1.xlsx",null );


```
{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}
```java

    public static void main(String[] args) {
        try{
            CellsApi  cellsApi = new CellsApi(System.getenv("ProductClientId"),System.getenv("ProductClientSecret"));
            File file = new File("TestImportData.xlsx");
            cellsApi.uploadFile("JavaSDK/OutResult/Book1.xlsx", file, null);
        }
        catch( Exception e) 
        {
            System.out.print(e.getMessage());
        }
    }
```

{{< /tab >}}

{{< tab tabNum="7" >}}
 ```perl
use strict;
use warnings;
use utf8; 
use File::Slurp;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'ProductClientId'}, client_secret => $ENV{'ProductClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $upload_file_data = read_file( 'C:/data/CellsTests/Book1.xlsx' , binmode => ':raw' );
$instance->upload_file(path=>'PerlSDK/OutResult/UplaodFile_Book1.xlsx' ,file => $upload_file_data);

 ```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go

package main

import (
	"os"
	"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22"
)

func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))

	file, err := os.Open("D:/projects/aspose/examples/testdata/source/Book1.xlsx")	
	if err != nil {
	   println( err)
	}


	uploadFileOpts := new(asposecellscloud.UploadFileOpts)
	uploadFileOpts.Path = "GoSDK/OutResult/UploadFile_Book1.xlsx"
	_, _, err1  := instance.UploadFile(file, uploadFileOpts)
	if err1 != nil {
	   println( err1)
	}

}

```

{{< /tab >}}
{{< tab tabNum="9" >}}
```python

import os
from asposecellscloud.apis.cells_api import CellsApi

cells_api = CellsApi(os.getenv('ProductClientId'),os.getenv('ProductClientSecret'))
cells_api.upload_file("PythonSDK/OutResult/UploadFile_Book1.xlsx", "D:/projects/aspose/examples/testdata/source/Book1.xlsx")

```
{{< /tab >}}
{{< /tabs >}}
 

