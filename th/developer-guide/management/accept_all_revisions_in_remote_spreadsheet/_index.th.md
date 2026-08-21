---
---
title: "รับการแก้ไขทั้งหมดในสเปรดชีตระยะไกล"
ArticleTitle: "รับการแก้ไขทั้งหมดในสเปรดชีตระยะไกล – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "รับการแก้ไขทั้งหมดในสเปรดชีตระยะไกล"
type: docs
url: /cells/accept-all-revisions
aliases: ["/cells/accept-all-revisions"]
keywords: "Aspose.Cells, AcceptAllRevisions, สเปรดชีตระยะไกล"
description: "รับการแก้ไขทั้งหมดในสเปรดชีตระยะไกล และส่งคืนไฟล์สมุดงานที่อัปเดตแล้ว"
weight: 1000
---

## การรับการแก้ไขทั้งหมดในสเปรดชีตระยะไกลของเว็บเซอร์วิส Aspose.Cells Cloud

รับการแก้ไขที่ติดตามไว้ (revisions) ทั้งหมดในสมุดงานที่ระบุซึ่งถูกจัดเก็บไว้ในพื้นที่จัดเก็บระยะไกล การดำเนินการนี้สามารถบันทึกสมุดงานที่ได้รับการอัปเดตไปยังตำแหน่งหรือพื้นที่จัดเก็บอื่นได้ตามต้องการ และส่งคืนไฟล์ที่อัปเดตแล้วในรูปแบบสตรีมไบนารี

### จุดจบของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|----------------|------|-----------------------------|-------------|
| name | string | Path | ชื่อของไฟล์สมุดงานที่จัดเก็บไว้ในพื้นที่จัดเก็บระยะไกล |
| folder | string | Query | (ไม่บังคับ) โฟลเดอร์ที่อยู่ภายในพื้นที่จัดเก็บที่สมุดงานนั้นตั้งอยู่ |
| storageName | string | Query | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บหากใช้พื้นที่จัดเก็บแบบคลาวด์ที่กำหนดเอง หากไม่ระบุจะใช้พื้นที่จัดเก็บเริ่มต้น |
| outPath | string | Query | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จะบันทึกสมุดงานที่อัปเดตแล้ว ค่าเริ่มต้นคือ null |
| outStorageName | string | Query | (ไม่บังคับ) ชื่อของพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| fontsLocation | string | Query | (ไม่บังคับ) เส้นทางไปยังตำแหน่งฟอนต์ที่กำหนดเอง |
| region | string | Query | (ไม่บังคับ) การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) ซึ่งมีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password | string | Query | (ไม่บังคับ) รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์เนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
| -------------- | ---- | ----------- |
| *ไม่มี* | *ไม่มี* | การดำเนินการนี้ไม่จำเป็นต้องมีเนื้อหาคำขอ |

### **การตอบกลับ**

```json
{
  "File": "สตรีมไบนารีของสมุดงานที่อัปเดตแล้ว (เช่น .xlsx) ซึ่งส่งคืนเป็นเนื้อหาของ response body"
}
```

**โค้ดสถานะของการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | OK | สมุดงานที่รับการแก้ไขทั้งหมดแล้วจะถูกส่งคืนในรูปแบบสตรีมไฟล์ไบนารี |
| 400 | Bad Request | พารามิเตอร์ที่จำเป็นหายไปหรือรูปแบบคำขอไม่ถูกต้อง |
| 401 | Unauthorized | JWT token ไม่ถูกต้องหรือไม่ได้ระบุ |
| 413 | Payload Too Large | คำขอเกินขีดจำกัดขนาดที่อนุญาต |
| 500 | Internal Server Error | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้การรับการแก้ไขทั้งหมดในสเปรดชีตระยะไกลด้วย SDK

### ข้อมูลจำเพาะการรับการแก้ไขทั้งหมดในสเปรดชีตระยะไกล

[ข้อมูลจำเพาะของ API การรับการแก้ไขทั้งหมดในสเปรดชีตระยะไกล](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่อยู่ในรูปแบบคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "สตรีมไบนารีของสมุดงานที่อัปเดตแล้ว (เช่น .xlsx)"
}
```

{{< /tab >}}

{{< /tabs >}}

### การใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer"> kho ของ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิสของ Aspose Cells Cloud ผ่าน SDK ต่างๆ:
 `[TBD]`
---