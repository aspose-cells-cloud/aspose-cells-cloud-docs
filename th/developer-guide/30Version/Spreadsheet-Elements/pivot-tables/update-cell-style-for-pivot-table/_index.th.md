---
title: "อัปเดตสไตล์ของเซลล์ในตารางสรุปข้อมูล"
second_title: "เอกสาร"
linktype: รูปแบบ
type: docs
url: /pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, สไตล์ตารางสรุปข้อมูล, API อัปเดตสไตล์เซลล์, REST API, Excel API, การจัดรูปแบบสเปรดชีต, cloud SDK, สไตล์เซลล์, ตารางสรุปข้อมูล"
description: "เรียนรู้วิธีอัปเดตสไตล์ของเซลล์ที่กำหนดในตารางสรุปข้อมูลของ Aspose.Cells Cloud ผ่าน REST API ซึ่งประกอบด้วย endpoint, พารามิเตอร์, การยืนยันตัวตน, ตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับ Go พร้อมคำแนะนำที่ปรับให้เหมาะสมกับ SEO"
weight: 90
ArticleTitle: "อัปเดตสไตล์ของเซลล์ในตารางสรุปข้อมูล - เอกสารประกอบ API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้อัปเดต **สไตล์** ของเซลล์ในตารางสรุปข้อมูล

**ข้อกำหนดเบื้องต้น / การยืนยันตัวตน**  
ในการเรียก endpoint นี้ คุณต้องมี JWT access token ที่ถูกต้องจาก Aspose Cloud รับ token ผ่านขั้นตอน OAuth 2.0 ตามที่อธิบายไว้ใน [คู่มือการยืนยันตัวตน](/authentication/) และแนบ token ใน header ของคำขอ:

```http
Authorization: Bearer <jwt token>
```

JWT token จำเป็นสำหรับการเรียกใช้ API ทั้งหมดของ Aspose.Cells Cloud

## API PostPivotTableCellStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                             |
| ---------------- | --------- | -------- | ----------------------------------------------------------------------------------------------------- |
| name             | string    | path     | ชื่อเอกสาร (จำเป็น)                                                                                    |
| sheetName        | string    | path     | ชื่อแผ่นงาน (จำเป็น)                                                                                  |
| pivotTableIndex  | integer   | path     | ดัชนีของตารางสรุปข้อมูล (จำเป็น)                                                                      |
| column           | integer   | query    | ดัชนีคอลัมน์แบบเริ่มต้นที่ 0 ของเซลล์ที่ต้องการจัดรูปแบบ (จำเป็น)                                      |
| row              | integer   | query    | ดัชนีแถวแบบเริ่มต้นที่ 0 ของเซลล์ที่ต้องการจัดรูปแบบ (จำเป็น)                                          |
| style            | object    | body     | Style DTO (data-transfer object) ที่กำหนดสไตล์เซลล์ใหม่                                               |
| needReCalculate  | boolean   | query    | ระบุว่าควรคำนวณตารางสรุปข้อมูลใหม่หลังจากจัดรูปแบบหรือไม่ ค่าเริ่มต้นคือ **false**                   |
| folder           | string    | query    | โฟลเดอร์ที่เก็บเอกสาร (ไม่บังคับ)                                                                      |
| storageName      | string    | query    | ชื่อของพื้นที่จัดเก็บ (ไม่บังคับ)                                                                      |
| Method           | string    | N/A      | HTTP method ที่ใช้สำหรับคำขอ (**POST**)                                                                |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">สเปค OpenAPI</a> กำหนด API แบบโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
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

{{< /tab >}}

{{< /tabs >}}

**การตอบกลับ**  
เมื่อสำเร็จ บริการจะส่งกลับ HTTP 200 พร้อมเนื้อหาว่างเปล่า ซึ่งบ่งชี้ว่าสไตล์ถูกใช้แล้ว ในกรณีที่เกิดข้อผิดพลาด จะส่งกลับ JSON payload ที่มีรหัสข้อผิดพลาดและข้อความ

| HTTP Status | คำอธิบาย                                                                 |
|-------------|--------------------------------------------------------------------------|
| 200         | อัปเดตสไตล์สำเร็จ                                                       |
| 400         | คำขอผิดพลาด – เช่น ดัชนีคอลัมน์/แถวไม่ถูกต้อง                           |
| 401         | ไม่ได้รับอนุญาต – ไม่มีหรือ JWT token ไม่ถูกต้อง                       |
| 404         | ไม่พบ – เอกสาร แผ่นงาน หรือตารางสรุปข้อมูลที่ระบุไม่มีอยู่              |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิด                        |

เนื้อหาของ response body จะว่างเปล่าเมื่อสำเร็จ

สำหรับข้อมูลเพิ่มเติม ดูที่เอกสารประกอบของ API **Get Pivot Table**

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> สำหรับรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ **Go SDK**:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "อัปเดตสไตล์ของเซลล์ในตารางสรุปข้อมูล",
  "description": "คู่มืออัปเดตสไตล์ของเซลล์ที่กำหนดในตารางสรุปข้อมูลของ Aspose.Cells Cloud โดยใช้ REST API",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, ตารางสรุปข้อมูล, สไตล์เซลล์, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>