---
title: "สร้างสมุดงาน Excel ที่ว่างเปล่า"
second_title: "เอกสาร"
linktype: "สมุดงานที่ว่างเปล่า"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    "/create-an-empty-excel-workbook/",
    "/workbook/new/",
    "/workbook/create/empty-workbook/",
  ]
keywords: "Aspose.Cells, คลาวด์, Excel, สมุดงานที่ว่างเปล่า, REST API, SDK"
description: "เรียนรู้วิธีการสร้างสมุดงาน Excel ที่ว่างเปล่าโดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL และ SDK"
weight: 20
ArticleTitle: "สร้างสมุดงาน Excel ที่ว่างเปล่าโดยใช้ Aspose.Cells Cloud API"
---

REST API นี้จะสร้าง **สมุดงานที่ว่างเปล่า**

## API PutWorkbookCreate

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์ Query

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                                                 |
| ---------------- | ---------- | ------------------------------------------------------------------------ |
| templateFile     | string     | เส้นทางไปยังสมุดงานแม่แบบที่จะใช้เป็นฐาน (ไม่บังคับ)                     |
| dataFile         | string     | เส้นทางไปยังไฟล์ข้อมูลที่จะใช้เติมข้อมูลลงในสมุดงาน (ไม่บังคับ)          |
| isWriteOver      | boolean    | `true` หากต้องการเขียนทับไฟล์ที่มีอยู่; `false` กรณีอื่นๆ               |
| folder           | string     | โฟลเดอร์ปลายทางที่จะบันทึกสมุดงานที่สร้างขึ้น (ไม่บังคับ)                |
| storageName      | string     | ชื่อของบริการจัดเก็บข้อมูลที่จะใช้                                       |

### พารามิเตอร์ Request Body

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                     |
| ---------------- | ---------- | -------------------------------------------- |
| data             | file       | เนื้อหาไบนารีของไฟล์สมุดงานที่ต้องการสร้าง |

### **การตอบกลับ**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                       | สถานการณ์ที่ส่งคืน                           |
|-----|--------------------------------|---------------------------------------------|
| 200 OK | สร้างสมุดงานเรียบร้อยแล้ว      | กรณีการทำงานตามปกติ                         |
| 201 Created | สร้างสมุดงานเรียบร้อยแล้ว (การตอบกลับทางเลือก) | เมื่อ API ส่งคืนสถานะ created             |
| 400 Bad Request | พารามิเตอร์ไม่ถูกต้อง         | ข้อผิดพลาดฝั่งไคลเอนต์                      |
| 401 Unauthorized | ขาดโทเคนหรือโทเคนไม่ถูกต้อง | ข้อผิดพลาดด้านการยืนยันตัวตน               |
| 409 Conflict | มีไฟล์อยู่แล้วและ `isWriteOver=false` | ขัดแย้งกับไฟล์ที่มีอยู่                      |

## วิธีการใช้ PutWorkbookCreate API ร่วมกับ SDK

### ข้อกำหนด PutWorkbookCreate API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells โดยระบุ header `Authorization` พร้อมโทเคน OAuth2/JWT ที่ถูกต้อง สำหรับสมุดงานที่ว่างเปล่า ตัวเนื้อหาของ request body เป็นตัวเลือก; หากคุณต้องการอัปโหลดไฟล์ ให้เพิ่ม `--data-binary @empty.xlsx` ดังตัวอย่างด้านล่าง

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# สร้างสมุดงานที่ว่างเปล่าชื่อ newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # ข้ามบรรทัดนี้หากต้องการสมุดงานที่ว่างเปล่าอย่างสมบูรณ์
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ ตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---