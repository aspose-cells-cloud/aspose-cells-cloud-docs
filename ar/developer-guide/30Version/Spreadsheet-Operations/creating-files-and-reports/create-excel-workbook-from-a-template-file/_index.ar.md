---
title: "كيفية إنشاء ملف مصنف Excel باستخدام ملف قالب"
second_title: "مستند"
linktitle: "ملف القالب"
type: docs
url: /ar/create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, قالب, API, Aspose.Cells, مصنف, REST, سحابة"
description: "تعرّف على كيفية إنشاء مصنفات Excel باستخدام ملفات القوالب عبر واجهة Aspose.Cells Cloud REST API. يشمل المتطلبات الأساسية، خطوات المصادقة، أمثلة cURL، تفاصيل معالجة الأخطاء، وأكواد مقتطفات SDK."
weight: 30
---

# كيفية إنشاء ملف مصنف Excel باستخدام ملف قالب

قم بإنشاء مصنف Excel جديد باستخدام ملف قالب موجود، مع إمكانية استخدام ملف بيانات يوفّر قيم علامات التحديد الذكية (Smart‑Markers) اختياريًا. تُنفَّذ هذه العملية من خلال نقطة نهاية **PUT** `/cells/{name}` في خدمة Aspose.Cells Cloud.

---

## المتطلبات الأساسية

| المتطلب | الوصف |
|----------|---------|
| **حساب Aspose.Cells Cloud** | سجّل الدخول في https://dashboard.aspose.cloud/ واحصل على **مُعرّف العميل** / **سرّ العميل**. |
| **رمز وصول JWT** | أنشئ رمز JWT وفقًا لما هو موضح في [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **ملف القالب** | ارفع ملف Excel القالبي (مثل `Calendar.xlsx`) إلى مساحة التخزين التي تختارها باستخدام واجهة برمجة تطبيقات **رفع ملف** أو الواجهة الرسومية. |
| **ملف البيانات (اختياري)** | ملف JSON أو XML يحتوي على قيم علامات التحديد الذكية (مثل `Sample_Data.xml`). |
| **مساحة التخزين المدعومة** | مساحة التخزين الافتراضية (`Default`) أو مساحة تخزين مخصّصة تم تكوينها في حساب Aspose الخاص بك. |

---

## المصادقة

تتطلّب جميع طلبات Aspose.Cells Cloud رمز **Bearer JWT** يُمرَّر في رأس `Authorization`:

```http
Authorization: Bearer {access_token}
```

يجب الحصول على الرمز مسبقًا، وهو ساري المفعول لمدة ساعة افتراضيًا.

---

## الطلب

### طلب HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| العنصر | القيمة |
|--------|--------|
| **الطريقة** | `PUT` |
| **المسار** | `/cells/{name}` – `name` هو الاسم المطلوب للمصنف الجديد الذي سيتم إنشاؤه (مع امتداد الملف، مثل `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (عند إرسال ملف بيانات في جسم الطلب). |
| **Accept** | `application/json` |

### معامل المسار

| الاسم | النوع | مطلوب | الوصف |
|-------|-------|--------|--------|
| `name` | سلسلة نصية | **نعم** | اسم المصنف المراد إنشاؤه (مثل `newworkbook.xlsx`). |

### معاملات الاستعلام

| المعامل | النوع | مطلوب | القيمة الافتراضية | الوصف |
|---------|-------|--------|------------------|--------|
| `templateFile` | سلسلة نصية | لا | — | اسم ملف القالب المخزّن في السحابة. |
| `dataFile` | سلسلة نصية | لا | — | اسم ملف البيانات (XML أو JSON) المخزّن في السحابة. |
| `isWriteOver` | منطقي | لا | `false` | استبدال الملف الهدف إذا كان موجودًا مسبقًا. مرّر `true` أو `false` **بدون** علامات اقتباس. |
| `folder` | سلسلة نصية | لا | — | مسار المجلد الذي يحتوي على القالب (وملف البيانات الاختياري). |
| `storageName` | سلسلة نصية | لا | — | اسم خدمة التخزين التي تحتوي على الملفات. |
| `checkExcelRestriction` | منطقي | لا | `true` | التحقق من صحة المصنف وفق قيود Excel قبل إنشائه. |

### جسم الطلب (اختياري)

عند إرسال بيانات علامات التحديد الذكية مباشرةً في الطلب، تضمّنها كجزء ملف من نوع **`data`** في محتوى متعدد الأجزاء (multipart).

| اسم الجزء | النوع | الوصف |
|-----------|-------|--------|
| `data` | ملف | ملف XML أو JSON يحتوي على قيم علامات التحديد الذكية. |

#### مثال باستخدام cURL مع جسم الطلب

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*إذا استخدمت معامل الاستعلام `dataFile` بدلًا من جسم متعدد الأجزاء، فتجاهل علامة `-F`.*

---

## الاستجابة

يُعيد الطلب الناجح رمز الحالة **`200 OK`** (أو **`201 Created`** عند إنشاء ملف جديد) مع حُمل JSON يصف المصنف المُنشأ.

```json
{
    "Code": 200,
    "Status": "OK",
    "File": {
        "Name": "newworkbook.xlsx",
        "Size": 18234,
        "Path": "output/newworkbook.xlsx",
        "Url": "https://api.aspose.cloud/v3.0/storage/file/output/newworkbook.xlsx"
    }
}
```

### أنواع بيانات الاستجابة

| الخاصية | النوع | الوصف |
|----------|-------|--------|
| `Code` | عدد صحيح | رمز الحالة مثل HTTP يعيده الـ API. |
| `Status` | سلسلة نصية | وصف نصي لحالة الاستجابة. |
| `File` | كائن | تفاصيل المصنف المُنشأ. |
| `File.Name` | سلسلة نصية | اسم ملف المصنف الجديد. |
| `File.Size` | عدد صحيح | الحجم بالبايت. |
| `File.Path` | سلسلة نصية | المسار النسبي داخل مساحة التخزين. |
| `File.Url` | سلسلة نصية | رابط تحميل مباشر (يتطلب نفس رمز JWT). |

---

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | OK | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُصادَق عليه | رمز JWT غير صالح أو مفقود. |
| 413 | حمل الطلب كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح (50 ميجابايت افتراضيًا). |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

---

## أمثلة باستخدام SDKs

تُظهر المقتطفات التالية كيفية استدعاء **PutWorkbookCreate** باستخدام SDKs الرسمية لـ Aspose.Cells Cloud.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | اسم المستند الجديد.
var templateFile = "Calendar.xlsx"; // string | اسم ملف القالب.
var dataFile = "Sample_Data.xml"; // string | اسم ملف البيانات (اختياري).
var isWriteOver = true; // bool? | الاستبدال في حال وجود الملف.
var folder = "templates"; // string | المجلد الذي توجد فيه الملفات.
var storageName = "MyStorage"; // string | اسم مساحة التخزين.

using (var dataStream = File.OpenRead("Sample_Data.xml"))
{
    var response = apiInstance.PutWorkbookCreate(
        name,
        templateFile: templateFile,
        dataFile: dataFile,
        isWriteOver: isWriteOver,
        folder: folder,
        storageName: storageName,
        data: dataStream);
    Console.WriteLine(response);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cloud.cells.api.WorkbookApi;
import com.aspose.cloud.cells.model.*;

import java.io.File;
import java.io.FileInputStream;

WorkbookApi api = new WorkbookApi();
String name = "newworkbook.xlsx";
String templateFile = "Calendar.xlsx";
String dataFile = "Sample_Data.xml";
Boolean isWriteOver = true;
String folder = "templates";
String storageName = "MyStorage";

FileInputStream dataStream = new FileInputStream(new File("Sample_Data.xml"));
CellsCloudResponse response = api.putWorkbookCreate(
        name,
        templateFile,
        dataFile,
        isWriteOver,
        folder,
        storageName,
        dataStream);
System.out.println(response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorkbookApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new WorkbookApi(null, $config);
$name = "newworkbook.xlsx";
$templateFile = "Calendar.xlsx";
$dataFile = "Sample_Data.xml";
$isWriteOver = true;
$folder = "templates";
$storageName = "MyStorage";

$data = fopen("Sample_Data.xml", "r");
$result = $apiInstance->putWorkbookCreate($name, $templateFile, $dataFile, $isWriteOver, $folder, $storageName, $data);
print_r($result);
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::WorkbookApi.new
api.config.access_token = '{access_token}'

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = true
folder = 'templates'
storage_name = 'MyStorage'

File.open('Sample_Data.xml', 'rb') do |data|
  response = api.put_workbook_create(name,
                                     template_file: template_file,
                                     data_file: data_file,
                                     is_write_over: is_write_over,
                                     folder: folder,
                                     storage_name: storage_name,
                                     data: data)
  puts response
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorkbookApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

let config = new Configuration();
config.accessToken = '{access_token}';
config.basePath = 'https://api.aspose.cloud';

let apiInstance = new WorkbookApi(config);

let name = 'newworkbook.xlsx';
let templateFile = 'Calendar.xlsx';
let dataFile = 'Sample_Data.xml';
let isWriteOver = true;
let folder = 'templates';
let storageName = 'MyStorage';

let data = fs.createReadStream('Sample_Data.xml');

apiInstance.putWorkbookCreate(name, templateFile, dataFile, isWriteOver, folder, storageName, data)
    .then(response => console.log(response))
    .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.apis import WorkbookApi
from asposecellscloud.models import CellsCloudResponse

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api_instance = WorkbookApi(asposecellscloud.ApiClient(config))

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = True
folder = 'templates'
storage_name = 'MyStorage'

with open('Sample_Data.xml', 'rb') as data:
    response = api_instance.put_workbook_create(
        name,
        template_file=template_file,
        data_file=data_file,
        is_write_over=is_write_over,
        folder=folder,
        storage_name=storage_name,
        data=data)
    print(response)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorkbookApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::Api::WorkbookApi->new($config);

my $name = 'newworkbook.xlsx';
my $template_file = 'Calendar.xlsx';
my $data_file = 'Sample_Data.xml';
my $is_write_over = 1;
my $folder = 'templates';
my $storage_name = 'MyStorage';

open my $fh, '<:raw', 'Sample_Data.xml' or die $!;
my $response = $api_instance->put_workbook_create(
    name => $name,
    template_file => $template_file,
    data_file => $data_file,
    is_write_over => $is_write_over,
    folder => $folder,
    storage_name => $storage_name,
    data => $fh);
print $response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "os"

    asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorkbookApi(cfg)

    name := "newworkbook.xlsx"
    templateFile := "Calendar.xlsx"
    dataFile := "Sample_Data.xml"
    isWriteOver := true
    folder := "templates"
    storageName := "MyStorage"

    data, _ := os.Open("Sample_Data.xml")
    defer data.Close()

    result, _, err := apiInstance.PutWorkbookCreate(name, &templateFile, &dataFile, &isWriteOver, &folder, &storageName, data)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Printf("Response: %+v\n", result)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## معالجة الأخطاء

| رمز الحالة | الحالة | الإجراء الموصى به |
|------------|---------|-------------------|
| **400** | معاملات مطلوبة مفقودة أو نوع ملف غير صالح. | تحقق من معاملات الاستعلام، وتأكد من وجود ملفات القالب والبيانات ودعمها (`.xlsx`, `.xml`, `.json`). |
| **401** | رمز JWT مفقود أو منتهٍ أو غير صحيح. | أنشئ رمز وصول جديد باستخدام مُعرّف العميل وسرّ العميل. |
| **413** | تجاوز حجم الملف المرفوع الحد المسموح (50 ميجابايت افتراضيًا). | قلل من حجم الملف أو اقسم المصنف إلى أجزاء أصغر. |
| **500** | خطأ غير متوقع في الخادم. | أعد المحاولة بعد تأخير قصير؛ وإذا استمرت المشكلة، تواصل مع دعم Aspose مع تضمين قيمة رأس `Request‑Id`. |

---

## راجع أيضًا

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – حفظ مصنف موجود بتنسيق محدّد.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – استرجاع معلومات المصنف أو تنزيل الملف.  
- **[واجهة برمجة تطبيقات رفع ملف](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – رفع ملفات القالب أو البيانات إلى مساحة التخزين السحابية.  

---