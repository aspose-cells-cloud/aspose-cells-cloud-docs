---
title: "การลบค่าซ้ำกัน"
ArticleTitle: "การลบค่าซ้ำกัน – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "การลบค่าซ้ำกัน"
type: docs
url: /th/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, ลบค่าซ้ำกัน, API"
description: "ลบค่าที่ซ้ำกันในแผ่นงาน ช่วงข้อมูล หรือตาราง"
weight: 1000
---

## การลบค่าซ้ำกันด้วยบริการเว็บ Aspose.Cells Cloud

ลบค่าที่ซ้ำกันในแผ่นงาน ช่วงข้อมูล หรือตาราง วิธีนี้จะสแกนขอบเขตเป้าหมายเพื่อหาแถวที่มีค่าตรงกันในคอลัมน์ที่ระบุเพื่อตรวจสอบ จากนั้นจะลบค่าที่ซ้ำกันทั้งหมดยกเว้นค่าที่ปรากฏครั้งแรก การเปรียบเทียบจะเป็นแบบแยกแยะตัวพิมพ์เล็ก/พิมพ์ใหญ่ และตรงกับค่าในเซลล์แบบแม่นยำ

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | ไฟล์   | FormData                    | อัปโหลดไฟล์สมุดบันทึก |
| worksheet      | ข้อความ | Query                       | ชื่อแผ่นงาน (ไม่บังคับ) |
| range          | ข้อความ | Query                       | ชื่อช่วงข้อมูลที่ต้องการลบค่าซ้ำกัน (ไม่บังคับ) |
| table          | ข้อความ | Query                       | ชื่อตารางที่ต้องการลบค่าซ้ำกัน (ไม่บังคับ) |
| outPath        | ข้อความ | Query                       | (ไม่บังคับ) ที่อยู่โฟลเดอร์ที่เก็บสมุดบันทึก ค่าเริ่มต้นคือ null |
| outStorageName | ข้อความ | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| region         | ข้อความ | Query                       | การตั้งค่าภูมิภาค/ภาษาของสมุดบันทึก (เช่น `en-US`, `fr-FR`) ซึ่งมีผลต่อการจัดรูปแบบตัวเลข การประมวลผลวันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password       | ข้อความ | Query                       | รหัสผ่านสำหรับเปิดไฟล์สมุดบันทึก |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **การตอบกลับ**

```json
{
  "File": "สตรีมไบนารีของสมุดบันทึกผลลัพธ์ (เช่น .xlsx)"
}
```

**โค้ดสถานะของการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | ส่งคืนสมุดบันทึกผลลัพธ์ที่ลบค่าซ้ำกันแล้วในรูปแบบสตรีมไฟล์ |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์ของคำขอไม่ถูกต้อง หรือ URL มีรูปแบบผิด |
| 401 | ไม่ได้รับอนุญาต | การยืนยันตัวตนล้มเหลว หรือไม่ได้ระบุข้อมูลยืนยันตัวตน |
| 413 | เนื้อหาคำขอใหญ่เกินไป | ขนาดไฟล์ที่อัปโหลดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | สมุดบันทึกมีข้อผิดพลาดในการดึงข้อมูล หรือเกิดข้อผิดพลาดฝั่งเซิร์ฟเวอร์อื่นๆ |

## วิธีใช้การลบค่าซ้ำกันด้วย SDK

### ข้อมูลเฉพาะของ API การลบค่าซ้ำกัน

[ข้อมูลเฉพาะของ API การลบค่าซ้ำกัน](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถใช้งาน REST API ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}
{< tab tabNum="1" >}
```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "สตรีมไบนารีของสมุดบันทึกผลลัพธ์ (เช่น .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### ใช้ SDK ของ Aspose Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose Cells Cloud ด้วย SDK ต่างๆ:

```csharp
// ตัวอย่างโค้ด SDK สำหรับ C#
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// ตัวอย่างโค้ด SDK สำหรับ Java
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# ตัวอย่างโค้ด SDK สำหรับ Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception when calling TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---