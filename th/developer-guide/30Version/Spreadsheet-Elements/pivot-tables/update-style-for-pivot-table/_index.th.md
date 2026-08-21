---
title: "อัปเดตสไตล์สำหรับตารางสรุป"
second_title: "เอกสาร"
linktitle: "จัดรูปแบบทั้งหมด"
type: docs
url: /th/pivot-tables/format-all/
aliases: [/th/update-style-for-pivot-table/]
keywords: "ตารางสรุป, อัปเดตสไตล์, Aspose.Cells Cloud, REST API, Excel, สเปรดชีต, API, สไตล์ตารางสรุป, จัดรูปแบบทั้งหมด"
description: "เรียนรู้วิธีการอัปเดตสไตล์ของตารางสรุปทั้งหมดโดยใช้ REST API ของ Aspose.Cells Cloud รวมถึงรายละเอียดคำขอ ตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับภาษาโปรแกรมต่างๆ"
weight: 100
ArticleTitle: "อัปเดตสไตล์สำหรับตารางสรุป - Aspose.Cells Cloud API"
---

REST API นี้ใช้อัปเดตสไตล์ของตารางสรุป

## API PostPivotTableStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**ข้อกำหนดเบื้องต้น / การยืนยันตัวตน**  
ต้องระบุโทเค็น JWT ที่ถูกต้องในส่วนหัว `Authorization` (เช่น `Bearer <jwt token>`) โดยต้องแน่ใจว่าโทเค็นนั้นมีสิทธิ์ในการเข้าถึงสมุดงานและชีตที่ระบุ

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบใช้โทเค็น JWT</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
|------------------|--------|----------|-----------|
| name             | string | path     | ชื่อไฟล์สมุดงาน |
| sheetName        | string | path     | ชีตที่มีตารางสรุป |
| pivotTableIndex  | integer | path    | ดัชนีของตารางสรุปที่ต้องการจัดรูปแบบ (เริ่มต้นที่ 0) |
| style            | object | body     | DTO ของสไตล์ที่กำหนดรูปแบบที่จะนำไปใช้ |
| needReCalculate  | boolean | query   | ตั้งค่าเป็น **true** เพื่อคำนวณตารางสรุปใหม่หลังจากจัดรูปแบบ ค่าเริ่มต้นคือ **false** |
| folder           | string | query    | โฟลเดอร์ที่จัดเก็บสมุดงานไว้ |
| storageName      | string | query    | ชื่อของบริการจัดเก็บข้อมูล |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle" rel="noopener noreferrer">ข้อกำหนด OpenAPI</a> นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย |
|------|-----------------------------|----------|
| 200  | สำเร็จ (OK)                | แอ็พพลายตัวกรองสำเร็จ; การตอบกลับประกอบด้วยรายละเอียดของOPERATION |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลในเนื้อหายาวเกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาโดยใช้ API SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ ดู <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียก API โดยใช้ Go SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}