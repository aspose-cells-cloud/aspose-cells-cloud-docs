---
title: "ส่งออกกราฟใน Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
description: "แปลงกราฟจากสมุดงาน Excel ที่จัดเก็บไว้ในคลาวด์เป็นรูปแบบไฟล์อื่น เช่น PDF, PNG, SVG หรืออื่นๆ ด้วยการเรียก REST เพียงครั้งเดียว"
ArticleTitle: "วิธีการแปลงแผ่นงานในสเปรดชีตที่อยู่ในเครื่องให้เป็นไฟล์ PDF: คู่มือแบบทีละขั้นตอน"
linktype: "แปลงแผ่นงานเป็น PDF"
type: docs
url: /th/export-chart-as-format/
keywords: "Aspose.Cells Cloud, ส่งออกกราฟ, API, PDF, PNG, SVG, Excel, REST, การแปลงผ่านคลาวด์"
weight: 100
---

แปลงกราฟที่อยู่ในสมุดงานที่จัดเก็บไว้ใน Aspose Cloud Storage ให้อยู่ในรูปแบบไฟล์อื่น (เช่น PDF, PNG, SVG, …) โดยไม่ต้องดาวน์โหลดไฟล์ต้นฉบับ

## API ExportChartAsFormat

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ JWT token ซึ่งอธิบายเพิ่มเติมได้ที่ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนคำร้องขอ API</a>

### 📦 พารามิเตอร์สำหรับคำร้องขอ

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย                                                 |
| ------------------ | --------- | -------- | ------ | --------------------------------------------------------- |
| **name**           | string    | Path     | ใช่    | ชื่อไฟล์สมุดงาน                                          |
| **worksheet**      | string    | Path     | ใช่    | ชื่อแผ่นงานที่มีกราฟ                                     |
| **chartIndex**     | integer   | Path     | ใช่    | ดัชนีของกราฟที่ต้องการส่งออก (เริ่มต้นที่ 0)             |
| **format**         | string    | Query    | ใช่    | รูปแบบไฟล์ที่ต้องการ (เช่น `png`, `pdf`, `svg`)           |
| **folder**         | string    | Query    | ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ที่จัดเก็บสมุดงาน (ค่าเริ่มต้น: root) |
| **storageName**    | string    | Query    | ไม่จำเป็น | ชื่อที่จัดเก็บแบบกำหนดเอง; ละเว้นเพื่อใช้ที่จัดเก็บเริ่มต้น |
| **outPath**        | string    | Query    | ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ที่จะบันทึกไฟล์ที่แปลงแล้ว          |
| **outStorageName** | string    | Query    | ไม่จำเป็น | ชื่อที่จัดเก็บสำหรับไฟล์ผลลัพธ์                           |
| **fontsLocation**  | string    | Query    | ไม่จำเป็น | เส้นทางไปยังโฟลเดอร์ที่มีฟอนต์แบบกำหนดเอง               |
| **region**         | string    | Query    | ไม่จำเป็น | การตั้งค่าภาษา和地区 (เช่น `en-US`, `fr-FR`)              |
| **password**       | string    | Query    | ไม่จำเป็น | รหัสผ่านสำหรับเปิดสมุดงานที่มีการป้องกัน                 |

### **คำตอบที่ได้**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                | คำอธิบาย                                                     |
| ---- | ----------------------- | ------------------------------------------------------------ |
| 200  | สำเร็จ (OK)            | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของปฏิบัติการ |
| 400  | คำร้องขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)        |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                               |
| 413  | ข้อมูลที่ส่งมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                   |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                    |

## วิธีใช้ API ส่งออกกราฟเป็นรูปแบบต่างๆ ร่วมกับ SDK?

### ข้อมูลอ้างอิง API ส่งออกกราฟเป็นรูปแบบต่างๆ

[ข้อมูลอ้างอิง API ส่งออกกราฟเป็นรูปแบบต่างๆ](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) มีอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำร้องขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถแปลงข้อมูลตารางในสเปรดชีตเป็นไฟล์ PDF ได้ด้วยโค้ดเพียงไม่กี่บรรทัด โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ: