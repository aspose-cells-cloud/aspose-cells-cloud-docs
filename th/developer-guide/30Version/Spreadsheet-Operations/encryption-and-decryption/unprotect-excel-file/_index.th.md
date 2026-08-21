---
title: "ยกเลิกการป้องกันสมุดงาน Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ยกเลิกการป้องกันไฟล์ Excel"
type: docs
url: /th/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, API ยกเลิกการป้องกัน Excel, นำการป้องกันสมุดงานออก, REST API, สเปรดชีตบนคลาวด์"
description: "เรียนรู้วิธีการนำการป้องกันออกจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API รวมถึงไวยากรณ์คำขอ พารามิเตอร์ ตัวอย่าง cURL และโค้ด SDK ในหลายภาษา"
weight: 60
ArticleTitle: "ยกเลิกการป้องกันสมุดงาน Excel – Aspose.Cells Cloud API"
---

ใช้ REST API นี้เพื่อยกเลิกการป้องกันสมุดงาน Excel

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์เส้นทาง (Path Parameters)

| พารามิเตอร์ | ประเภท   | คำอธิบาย                                             | จำเป็น |
| ----------- | -------- | ----------------------------------------------------- | ------ |
| **name**    | string   | ชื่อไฟล์สมุดงาน (รวมส่วนขยายไฟล์ด้วย)               | ใช่    |

### พารามิเตอร์คิวรี (Query Parameters)

| ชื่อพารามิเตอร์ | ประเภท   | คำอธิบาย                                               |
| ---------------- | -------- | ------------------------------------------------------ |
| folder           | string   | เส้นทางไปยังโฟลเดอร์ที่เก็บสมุดงานต้นฉบับไว้         |
| storageName      | string   | ชื่อของบริการจัดเก็บข้อมูลที่สมุดงานนั้นอยู่           |

### พารามิเตอร์เนื้อหาคำขอ (Request Body Parameters)

| ชื่อพารามิเตอร์ | ประเภท                      | คำอธิบาย                                               |
| ---------------- | --------------------------- | ------------------------------------------------------ |
| protection       | WorkbookProtectionRequest   | ออบเจกต์ที่ระบุการตั้งค่าการป้องกันที่ต้องการยกเลิก    |

#### WorkbookProtectionRequest

| ชื่อพารามิเตอร์ | ประเภท   | คำอธิบาย                                                                                         |
| ---------------- | -------- | ------------------------------------------------------------------------------------------------ |
| ProtectionType   | string   | ประเภทการป้องกันที่ต้องการยกเลิก (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`) |
| Password         | string   | รหัสผ่านที่จำเป็นสำหรับการยกเลิกการป้องกัน (ไม่บังคับ)                                             |

#### ตัวอย่าง cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### คำตอบ (ความสำเร็จ)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### คำตอบข้อผิดพลาดจาก HTTPS Status

| HTTP Status | Code                | คำอธิบาย                                                   |
| ----------- | ------------------- | ---------------------------------------------------------- |
| 400         | BadRequest          | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง                           |
| 401         | Unauthorized        | โทเคนการเข้าถึงไม่ถูกต้องหรือขาดหาย                       |
| 404         | NotFound            | ไม่พบสมุดงานที่ระบุในโฟลเดอร์/พื้นที่จัดเก็บที่ระบุ        |
| 500         | InternalServerError | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                        |

## วิธีใช้ DeleteUnProtectWorkbook API ด้วย SDK

### ข้อมูลจำเพาะ DeleteUnProtectWorkbook API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL แบบ command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK จะทำให้การผสานรวมง่ายขึ้นและลดโค้ดที่ซ้ำซ้อน โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---