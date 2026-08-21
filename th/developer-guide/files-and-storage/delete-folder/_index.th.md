---
---
title: "ลบโฟลเดอร์ – API คลาวด์ Aspose.Cells | การลบโฟลเดอร์ผ่าน REST"
description: "เรียนรู้วิธีการลบโฟลเดอร์ (โดยสามารถลบแบบเรียกซีฟได้) จากที่จัดเก็บข้อมูลบนคลาวด์ของ Aspose.Cells โดยใช้เอนด์พ้อยต์ DELETE /v4.0/cells/storage/folder/{path} ซึ่งรวมถึงไวยากรณ์คำขอ พารามิเตอร์ การยืนยันตัวตน ตัวอย่างโค้ด และการจัดการข้อผิดพลาด"
keywords: "Aspose.Cells, ลบโฟลเดอร์, ที่จัดเก็บข้อมูลบนคลาวด์, API, REST, Excel, การจัดการไฟล์"
slug: delete-folder
date: 2026-07-30
---

# ลบโฟลเดอร์ – API คลาวด์ Aspose.Cells

ลบโฟลเดอร์ (พร้อมเนื้อหาภายในทั้งหมดหรือไม่ก็ได้) ออกจากที่จัดเก็บข้อมูลบนคลาวด์ของ Aspose.Cells

---

## ภาพรวม

การดำเนินการ **ลบโฟลเดอร์** จะลบโฟลเดอร์ออกจากบัญชีการจัดเก็บข้อมูลที่ใช้โดยบริการคลาวด์ของ Aspose.Cells อย่างถาวร  
คุณสามารถลบโฟลเดอร์ที่ว่างเปล่า หรือโดยการตั้งค่าฟลาก `recursive` เป็น `true` เพื่อลบโฟลเดอร์พร้อมกับไฟล์และโฟลเดอร์ย่อยทั้งหมดที่อยู่ภายใน จุดสิ้นสุดของ API นี้มักถูกใช้ในสคริปต์ทำความสะอาด ระบบอัตโนมัติ หรือเมื่อไม่ต้องการไดเรกทอรีชั่วคราวอีกต่อไป

---

## คำขอ HTTP

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – พาธเต็มของโฟลเดอร์ที่ต้องการลบ (ต้องเข้ารหัส URL)

### หัวข้อ HTTP ที่จำเป็น

| หัวข้อ            | ค่า                                | คำอธิบาย                                      |
|-------------------|------------------------------------|-----------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | โทเคน JWT ที่ได้รับจากบริการยืนยันตัวตน      |
| `Accept`          | `application/json`                | รูปแบบการตอบกลับที่คาดหวัง                   |
| `Content-Type`    | `application/json` *(ไม่บังคับ)*   | ไม่จำเป็นสำหรับคำขอ DELETE แต่สามารถส่งได้    |

---

## การยืนยันตัวตน

Aspose.Cells Cloud ใช้ระบบการยืนยันตัวตนแบบ **โทเคน JWT**  
รับโทเคนการเข้าถึงผ่าน[จุดสิ้นสุดของการยืนยันตัวตน](/authentication/) แล้วใส่ลงในหัวข้อ `Authorization` ดังที่แสดงไว้ข้างต้น

```bash
-H "Authorization: Bearer {access_token}"
```

---

## พารามิเตอร์

| ชื่อ          | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย                                                                 |
|---------------|------------|----------|--------|--------------------------------------------------------------------------|
| `path`        | สตริง       | เส้นทาง   | ใช่    | เส้นทางของโฟลเดอร์ที่ต้องการลบ (ต้องเข้ารหัส URL)                         |
| `storageName` | สตริง       | คิวรี    | ไม่ใช่ | ชื่อของที่จัดเก็บข้อมูลที่มีโฟลเดอร์นี้ หากไม่ระบุ จะใช้ที่จัดเก็บข้อมูลเริ่มต้น |
| `recursive`   | บูลีน       | คิวรี    | ไม่ใช่ | `true` → ลบโฟลเดอร์ **และเนื้อหาทั้งหมด** ภายใน ค่าเริ่มต้นคือ `false`    |

**ตัวอย่างสตริงคิวรี**

```
?storageName=MyStorage&recursive=true
```

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## การตอบกลับ

คำขอที่สำเร็จจะส่งกลับ **HTTP 200 OK** พร้อมวัตถุ JSON ว่าง:

```json
{}
```

ไม่มีข้อมูลเพิ่มเติมส่งกลับมา เนื่องจากผลลัพธ์ของการดำเนินการนี้เป็นแบบไบนารี — โฟลเดอร์จะถูกลบหรือเกิดข้อผิดพลาดเท่านั้น

---

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                        |
|------|-----------------------------|-------------------------------------------------|
| 200  | สำเร็จ (OK)                 | ดำเนินการสำเร็จ; การตอบกลับมีรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                 |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด               |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์        |

เมื่อเกิดข้อผิดพลาด ข้อมูลในเนื้อหาจะเป็นวัตถุ JSON ที่มีฟิลด์ `code` และ `message` ซึ่งอธิบายปัญหาที่เกิดขึ้น

---

## ตัวอย่างโค้ด SDK

ตัวอย่างต่อไปนี้แสดงวิธีการเรียก **ลบโฟลเดอร์** ผ่าน SDK ที่ได้รับการสนับสนุนอย่างเป็นทางการ แทนค่า `{access_token}` และค่าพารามิเตอร์ด้วยของคุณเอง

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// กำหนดค่าไคลเอนต์ API
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// ลบโฟลเดอร์ (แบบเรียกซีฟ)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// เริ่มต้นไคลเอนต์ API
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// กำหนดค่า
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// ลบโฟลเดอร์แบบเรียกซีฟ
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Folder deleted.";
} catch (Exception $e) {
    echo 'Exception when calling FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Folder deleted.'
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Folder deleted'))
    .catch(err => console.error('Error:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Folder deleted")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Folder deleted.\n";
};
if ($@) {
    warn "Error deleting folder: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println("Folder deleted")
}
```
</details>

---

## ดูเพิ่มเติม

- **[สร้างโฟลเดอร์](/create-folder/)** – สร้างโฟลเดอร์ใหม่ในที่จัดเก็บข้อมูลบนคลาวด์  
- **[คัดลอกโฟลเดอร์](/copy-folder/)** – ทำซ้ำโฟลเดอร์และเนื้อหาภายในทั้งหมด  
- **[ย้ายโฟลเดอร์](/move-folder/)** – ย้ายโฟลเดอร์ไปยังเส้นทางอื่น  
- **[ข้อมูลเฉพาะ OpenAPI]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">การดำเนินการ DeleteFolder</a> (เครื่องมือสำรวจ API แบบโต้ตอบ)

---

## รายการตรวจสอบ SEO และการเข้าถึง (ภายใน)

- **ชื่อเรื่องและ H1** ใช้ขีดกลางแบบอังกฤษ (`–`) และมีคำหลัก *ลบโฟลเดอร์*  
- หัวข้อทั้งหมดจัดลำดับตามโครงสร้างที่เป็นเหตุผล (`H1 → H2 → H3`)  
- ไม่มีอาร์ติแฟกต์การเข้ารหัส UTF-8 ที่ค้างอยู่  
- คำค้น meta รวมอยู่ในรายการเดียวที่กระชับ (หรือละเว้นหากต้องการ)  
- ลิงก์ภายนอกมี `rel="noopener noreferrer"` เพื่อความปลอดภัย  
- ไอคอน UI และธงภาษา (หากแสดงบนหน้าเว็บ) ควรมีแอตทริบิวต์ `aria-label`/`alt` (เช่น `aria-label="ภาษาอังกฤษ (สหรัฐอเมริกา)"`)  
- แท็ก `<link rel="alternate" hreflang="xx" href="…">` ควรถูกรวมไว้ในส่วน head ของหน้าสำหรับแต่ละเวอร์ชันภาษา