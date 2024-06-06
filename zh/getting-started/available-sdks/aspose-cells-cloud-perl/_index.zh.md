---
title: Aspose.Cells 适用于 Per 的 Cloud SDK
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/available-sdks/aspose-cells-cloud-perl/
description: Aspose.Cells云支持Excel创建、转换、合并、拆分、保护、内部对象操作等
weight: 30
kwords: Excel, Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、Perl
---
 SDK 是开源的，并根据 MIT 许可证获得许可。您可以访问 Aspose.Cells Cloud 的 Perl 库源代码[这里](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).


# **如何使用Aspose.Cells云的Perl库**

Aspose.Cells Cloud SDK for Perl 是一个功能强大的库，允许开发人员使用 Perl 编程语言操作和处理 Microsoft Excel 文件。使用此 SDK，您可以在云中创建、编辑和转换 Excel 文档，而无需在本地计算机上安装其他软件或依赖项。

在本文中，我们将探讨如何使用 Aspose.Cells Cloud SDK for Perl 执行一些常见任务，例如创建新的 Excel 工作簿、将数据插入单元格以及将修改后的工作簿保存到云端。

## 入门

在开始使用 Aspose.Cells Cloud SDK for Go 之前，您需要设置开发环境并安装必要的依赖项。请参阅[文章](https://docs.aspose.cloud/cells/quickstart/)在Aspose网站上获取您的客户端ID和客户端密钥。

## 如何安装 Aspose.Cells Cloud 的 Perl 包

您可以使用以下命令为 Perl 安装 Aspose.Cells Cloud SDK：

```Powershell

perl -MCPAN -e shell

install AsposeCellsCloud::CellsApi

```

## 如何使用 Perl 包将 Xlsx 转换为 PDF

- 导入Aspose.Cells云图书馆
首先将 Aspose.Cells Cloud Perl SDK 中的必要包导入到您的项目中。
- 使用凭证配置 API 客户端
使用您唯一的客户端 ID 和客户端密钥对您的 API 客户端进行身份验证。
- 准备转换参数
定义转换任务的参数，包括源文件名、所需输出格式和存储文件夹路径。
- 执行工作簿转换
使用 PostConvertWorkbook 方法调用转换过程并处理响应。

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
