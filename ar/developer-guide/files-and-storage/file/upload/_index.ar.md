---
title: تحميل الفيل
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/file/upload/
keywords: Learn how to upload file with Aspose Cells Cloud REST API
description: تعرف على كيفية تحميل الملف باستخدام Aspose Cells Cloud REST API SDK يدعم أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 100
---
يشير REST API إلى `upload file`.

## رسيت API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| المسار الذي سيتم التحميل فيه بما في ذلك اسم الملف والامتداد، على سبيل المثال /file.ext أو /Folder 1/file.ext إذا كان المحتوى متعدد الأجزاء ولا يحتوي المسار على اسم الملف، فإنه يحاول الحصول عليه من معلمة اسم الملف من رأس ترتيب المحتوى.|
| ملف| ملف| بيانات النموذج| ملف للتحميل|
| اسم التخزين| خيط| استفسار| اسم التخزين|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
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
 
## عائلة Cloud SDK
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى الاطلاع على[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:
 
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
 

