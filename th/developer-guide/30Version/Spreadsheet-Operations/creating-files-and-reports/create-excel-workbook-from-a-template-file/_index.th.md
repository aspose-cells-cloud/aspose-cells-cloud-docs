---
title: "วิธีการสร้างสมุดงาน Excel ด้วยไฟล์เทมเพลต"
second_title: "เอกสาร"
linktitle: "ไฟล์เทมเพลต"
type: docs
url: /th/create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, template, API, Aspose.Cells, workbook, REST, Cloud"
description: "เรียนรู้วิธีการสร้างสมุดงาน Excel จากไฟล์เทมเพลตโดยใช้ Aspose.Cells Cloud REST API รวมถึงข้อกำหนดเบื้องต้น ขั้นตอนการยืนยันตัวตน ตัวอย่าง cURL รายละเอียดการจัดการข้อผิดพลาด และโค้ดตัวอย่าง SDK"
weight: 30
---

# วิธีการสร้างสมุดงาน Excel ด้วยไฟล์เทมเพลต

สร้างสมุดงาน Excel ใหม่โดยใช้ไฟล์เทมเพลตที่มีอยู่แล้ว และ/หรือไฟล์ข้อมูลที่จัดเตรียมค่าสำหรับ Smart-Marker การดำเนินการนี้ทำผ่านจุดสิ้นสุด **PUT** `/cells/{name}` ของ Aspose.Cells Cloud

---

## ข้อกำหนดเบื้องต้น

| ข้อกำหนด | คำอธิบาย |
|----------|-----------|
| **บัญชี Aspose.Cells Cloud** | ลงทะเบียนที่ https://dashboard.aspose.cloud/ และรับ **Client Id** / **Client Secret** |
| **โทเค็น JWT** | สร้างโทเค็น JWT ตามที่อธิบายไว้ใน[คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) |
| **ไฟล์เทมเพลต** | อัปโหลดไฟล์ Excel เทมเพลต (เช่น `Calendar.xlsx`) ไปยังพื้นที่เก็บข้อมูลที่คุณเลือกโดยใช้ API **Upload File** หรืออินเทอร์เฟซผู้ใช้ |
| **ไฟล์ข้อมูล (ไม่บังคับ)** | ไฟล์ JSON หรือ XML ที่มีค่า Smart-Marker (เช่น `Sample_Data.xml`) |
| **พื้นที่เก็บข้อมูลที่รองรับ** | พื้นที่เก็บข้อมูลค่าเริ่มต้น (`Default`) หรือพื้นที่เก็บข้อมูลแบบกำหนดเองที่กำหนดค่าไว้ในบัญชี Aspose ของคุณ |

---

## การยืนยันตัวตน

คำขอทั้งหมดไปยัง Aspose.Cells Cloud ต้องส่ง **โทเค็น JWT แบบ Bearer** ในส่วนหัว `Authorization`:

```http
Authorization: Bearer {access_token}
```

โทเค็นต้องได้รับมาก่อน และจะมีผลใช้งานเป็นเวลา 1 ชั่วโมงตามค่าเริ่มต้น

---

## คำขอ

### คำขอ HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| ส่วนประกอบ | ค่า |
|-----------|-----|
| **เมธอด** | `PUT` |
| **พาธ** | `/cells/{name}` – `name` คือชื่อที่ต้องการสำหรับสมุดงานที่จะสร้างขึ้นใหม่ (รวมนามสกุลไฟล์ เช่น `newworkbook.xlsx`) |
| **Content-Type** | `multipart/form-data` (เมื่อส่งไฟล์ข้อมูลในเนื้อหาคำขอ) |
| **Accept** | `application/json` |

### พารามิเตอร์พาธ

| ชื่อ | ประเภท | จำเป็น | คำอธิบาย |
|------|--------|--------|----------|
| `name` | ข้อความ | **จำเป็น** | ชื่อสมุดงานที่จะสร้าง (เช่น `newworkbook.xlsx`) |

### พารามิเตอร์คิวรี

| พารามิเตอร์ | ประเภท | จำเป็น | ค่าเริ่มต้น | คำอธิบาย |
|-------------|--------|--------|------------|----------|
| `templateFile` | ข้อความ | ไม่บังคับ | — | ชื่อไฟล์เทมเพลตที่จัดเก็บไว้ในคลาวด์ |
| `dataFile` | ข้อความ | ไม่บังคับ | — | ชื่อไฟล์ข้อมูล (XML หรือ JSON) ที่จัดเก็บไว้ในคลาวด์ |
| `isWriteOver` | ค่าตรรกะ | ไม่บังคับ | `false` | เขียนทับไฟล์เป้าหมายหากมีอยู่แล้ว ส่ง `true` หรือ `false` **โดยไม่ต้อง**ใส่เครื่องหมายคำพูด |
| `folder` | ข้อความ | ไม่บังคับ | — | เส้นทางโฟลเดอร์ที่ไฟล์เทมเพลต (และไฟล์ข้อมูลที่อาจมี) อยู่ |
| `storageName` | ข้อความ | ไม่บังคับ | — | ชื่อของบริการพื้นที่เก็บข้อมูลที่มีไฟล์ |
| `checkExcelRestriction` | ค่าตรรกะ | ไม่บังคับ | `true` | ตรวจสอบสมุดงานกับข้อจำกัดของ Excel ก่อนการสร้าง |

### เนื้อหาคำขอ (ไม่บังคับ)

เมื่อส่งข้อมูลสำหรับตัวยึดตำแหน่ง Smart-Marker โดยตรงในคำขอ ให้รวมไว้เป็นส่วนของไฟล์แบบ multipart ชื่อ **`data`**

| ชื่อส่วน | ประเภท | คำอธิบาย |
|----------|--------|----------|
| `data` | ไฟล์ | ไฟล์ XML หรือ JSON ที่มีค่า Smart-Marker |

#### ตัวอย่าง cURL พร้อมเนื้อหาคำขอ

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*หากใช้พารามิเตอร์คิวรี `dataFile` แทนเนื้อหาคำขอแบบ multipart ให้ละเว้นฟลาเก `-F`*

---

## การตอบกลับ

การเรียกที่ประสบความสำเร็จจะส่งกลับ **`200 OK`** (หรือ **`201 Created`** เมื่อมีการสร้างไฟล์ใหม่) พร้อมข้อมูล JSON ที่อธิบายสมุดงานที่สร้างขึ้น

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

### ประเภทข้อมูลของการตอบกลับ

| คุณสมบัติ | ประเภท | คำอธิบาย |
|-----------|--------|----------|
| `Code` | จำนวนเต็ม | รหัสสถานะแบบ HTTP ที่ส่งกลับโดย API |
| `Status` | ข้อความ | คำอธิบายสถานะในรูปแบบข้อความ |
| `File` | ออบเจกต์ | รายละเอียดของสมุดงานที่สร้างขึ้น |
| `File.Name` | ข้อความ | ชื่อไฟล์ของสมุดงานที่สร้างขึ้น |
| `File.Size` | จำนวนเต็ม | ขนาดเป็นไบต์ |
| `File.Path` | ข้อความ | เส้นทางสัมพัทธ์ภายในพื้นที่เก็บข้อมูล |
| `File.Url` | ข้อความ | URL ดาวน์โหลดโดยตรง (ต้องใช้โทเค็น JWT เดียวกัน) |

---

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|-----------|----------|
| 200  | สำเร็จ | ตัวกรองถูกใช้งานเรียบร้อยแล้ว การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต | โทเค็น JWT ไม่ถูกต้อง หมดอาย หรือรูปแบบผิด |
| 413  | เนื้อหาหนักเกินไป | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด (ค่าเริ่มต้น 50 เมกะไบต์) |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

---

## ตัวอย่าง SDK

โค้ดตัวอย่างต่อไปนี้แสดงวิธีการเรียก **PutWorkbookCreate** ด้วย SDK อย่างเป็นทางการของ Aspose.Cells Cloud

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | ชื่อเอกสารใหม่
var templateFile = "Calendar.xlsx"; // string | ชื่อไฟล์เทมเพลต
var dataFile = "Sample_Data.xml"; // string | ชื่อไฟล์ข้อมูล (ไม่บังคับ)
var isWriteOver = true; // bool? | เขียนทับหากมีอยู่แล้ว
var folder = "templates"; // string | โฟลเดอร์ที่ไฟล์ตั้งอยู่
var storageName = "MyStorage"; // string | ชื่อพื้นที่เก็บข้อมูล

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

## การจัดการข้อผิดพลาด

| รหัสสถานะ | สถานการณ์ | การดำเนินการที่แนะนำ |
|-----------|------------|----------------------|
| **400** | พารามิเตอร์ที่จำเป็นขาดหาย หรือประเภทไฟล์ไม่ถูกต้อง | ตรวจสอบพารามิเตอร์คิวรี ยืนยันว่าไฟล์เทมเพลตและไฟล์ข้อมูลมีอยู่และรองรับ (`.xlsx`, `.xml`, `.json`) |
| **401** | โทเค็น JWT ขาดหาย หมดอาย หรือรูปแบบไม่ถูกต้อง | สร้างโทเค็นการเข้าถึงใหม่โดยใช้ Client Id/Secret ของคุณ |
| **413** | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาดของบริการ (ค่าเริ่มต้น 50 เมกะไบต์) | ลดขนาดไฟล์ หรือแบ่งสมุดงานออกเป็นส่วนย่อยที่เล็กกว่า |
| **500** | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ | ลองใหม่อีกครั้งหลังจากหน่วงเวลาสั้นๆ หากยังคงเกิดปัญหา โปรดติดต่อฝ่ายสนับสนุนของ Aspose พร้อมค่าของส่วนหัว `Request-Id` |

---

## ดูเพิ่มเติม

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – บันทึกสมุดงานที่มีอยู่เป็นรูปแบบที่ระบุ  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – ดึงข้อมูลสมุดงานหรือดาวน์โหลดไฟล์  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – อัปโหลดไฟล์เทมเพลตหรือไฟล์ข้อมูลไปยังพื้นที่เก็บข้อมูลบนคลาวด์  

---