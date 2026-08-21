---
title: "แยกสมุดงาน Excel ออกเป็นหลายไฟล์"
ArticleTitle: "วิธีการแยกสมุดงาน Excel ออกเป็นหลายไฟล์โดยใช้ Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "แยกไฟล์ Excel"
type: docs
url: /split-multi-excel-files/
aliases: [/split/multi-files/]
keywords: "Excel, Aspose.Cells Cloud, REST API, แยกสมุดงาน, หลายไฟล์, JPEG, PNG, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API ช่วยให้สามารถแยกสมุดงาน Excel ออกเป็นหลายไฟล์ในรูปแบบต่างๆ ได้ เอกสารนี้ให้รายละเอียดพารามิเตอร์คำขอ ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับภาษาต่างๆ เช่น C#, Java, PHP, Ruby, Node.js, Python, Perl และ Go"
weight: 130
---

REST API นี้แยก **สมุดงาน** Excel ออกเป็นหลายไฟล์ในรูปแบบต่างๆ

> **ข้อกำหนดเบื้องต้น** – เพื่อใช้งาน API นี้คุณต้องมีโทเค็น JWT ที่ถูกต้อง ตรวจสอบให้แน่ใจว่าคุณใช้เวอร์ชัน SDK ที่รองรับ และยืนยันว่าสมุดงานของคุณถูกจัดเก็บไว้ในตำแหน่งที่จัดเก็บข้อมูลที่รองรับ API นี้ยังบังคับใช้ข้อจำกัดเกี่ยวกับขนาดไฟล์ตามที่ระบุไว้ในแนวทางของแพลตฟอร์ม

## API PostWorkbookSplit

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์     | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                     | จำเป็น |
| -------------------- | ------- | -------- | ----------------------------------------------------------------------------------------------- | -------- |
| files[]              | ไฟล์    | formData | สมุดงาน Excel หนึ่งสมุดงานขึ้นไปที่จะ **ถูกแยก** โดยใช้ `file1`, `file2`, … ในคำขอ          | ใช่      |
| format               | สตริง  | Query    | รูปแบบผลลัพธ์ที่ต้องการสำหรับไฟล์ที่แยกออก                                                                 | ไม่จำเป็น       |
| from                 | จำนวนเต็ม | Query    | ดัชนีของชีตเริ่มต้น                                                                        | ไม่จำเป็น       |
| to                   | จำนวนเต็ม | Query    | ดัชนีของชีตสุดท้าย                                                                         | ไม่จำเป็น       |
| horizontalResolution | จำนวนเต็ม | Query    | ความละเอียดแนวนอนของภาพ                                                                    | ไม่จำเป็น       |
| verticalResolution   | จำนวนเต็ม | Query    | ความละเอียดแนวตั้งของภาพ                                                                      | ไม่จำเป็น       |
| outFolder            | สตริง  | Query    | โฟลเดอร์ปลายทางสำหรับไฟล์ที่แยกออก                                                              | ไม่จำเป็น       |
| splitNameRule        | สตริง  | Query    | กฎการตั้งชื่อที่ใช้กับไฟล์ที่แยกออก                                                             | ไม่จำเป็น       |
| folder               | สตริง  | Query    | โฟลเดอร์ที่เก็บสมุดงานต้นฉบับ                                                        | ไม่จำเป็น       |
| storageName          | สตริง  | Query    | ชื่อของพื้นที่จัดเก็บข้อมูลที่จะใช้                                                                     | ไม่จำเป็น       |

### **การตอบกลับ**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[ชื่อไฟล์1]",
        "Filesize" : [ขนาดไฟล์],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[ชื่อไฟล์2]",
        "Filesize" : [ขนาดไฟล์],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[ชื่อไฟล์3]",
        "Filesize" : [ขนาดไฟล์],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์อย่างไม่คาดคิด |

## วิธีการใช้ API PostWorkbookSplit ร่วมกับ SDK

### ข้อกำหนดการ API PostWorkbookSplit

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}