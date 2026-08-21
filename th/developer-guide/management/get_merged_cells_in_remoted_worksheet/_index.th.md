---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "รับเซลล์ที่ถูกรวมในวอร์กชีตระยะไกล – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "รับเซลล์ที่ถูกรวมในวอร์กชีตระยะไกล"
type: docs
url: /cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, รับเซลล์ที่ถูกรวม, วอร์กชีตระยะไกล, API"
description: "ดึงพื้นที่เซลล์ที่ถูกรวมทั้งหมดจากวอร์กชีตในไฟล์สเปรดชีตที่อยู่บนคลาวด์"
weight: 10
---

## GetMergedCellsInRemotedWorksheet ของ Aspose.Cells Cloud Web Services

รับพื้นที่เซลล์ที่ถูกรวมทั้งหมดจากวอร์กชีตในไฟล์สเปรดชีตบนคลาวด์

### จุดสิ้นสุดของ Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|--------|-----------------------------|-------------|
| name | string | Path | ชื่อไฟล์สเปรดชีต |
| worksheet | string | Path | ชื่อวอร์กชีต |
| folder | string | Query | เส้นทางของคลาวด์สตอเรจที่เก็บไฟล์สเปรดชีต |
| storageName | string | Query | (ไม่บังคับ) ชื่อของคลาวด์สตอเรจที่ใช้เฉพาะ หากไม่ระบุ จะใช้คลาวด์สตอเรจเริ่มต้น |
| region | string | Query | การตั้งค่าภูมิภาค/ภาษาของไฟล์สเปรดชีต (เช่น `en-US`, `fr-FR`) ซึ่งมีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของแต่ละภูมิภาค |
| password | string | Query | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| — | — | *ไม่มี* |

### **การตอบกลับ**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**โค้ดสถานะของการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | คำขอประสบความสำเร็จ และส่งรายการของพื้นที่เซลล์ที่ถูกรวมกลับมา |
| 400 | คำขอไม่ถูกต้อง | URL ไม่ถูกต้องหรือพารามิเตอร์ของคำขอไม่ถูกต้องตามรูปแบบ |
| 401 | ไม่ได้รับอนุญาต | การยืนยันตัวตนล้มเหลว หรือไม่ได้ระบุข้อมูลรับรองใดๆ |
| 413 | เนื้อหาคำขอใหญ่เกินไป | เนื้อหาของคำขอเกินขนาดที่อนุญาต |
| 500 | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ | ไฟล์สเปรดชีตมีข้อผิดพลาดขณะดึงข้อมูล |

## วิธีการใช้งาน GetMergedCellsInRemotedWorksheet ด้วย SDKs

### ข้อมูลเฉพาะของ GetMergedCellsInRemotedWorksheet

[ข้อมูลเฉพาะของ API GetMergedCellsInRemotedWorksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST interactions ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### ใช้งาน Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> สำหรับรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose Cells Cloud web services ด้วย SDK ต่างๆ:
`[TBD]`
---