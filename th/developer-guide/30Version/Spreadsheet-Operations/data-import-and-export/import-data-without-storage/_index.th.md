---
---
title: "นำเข้าข้อมูลโดยไม่ต้องใช้การจัดเก็บ – Aspose.Cells Cloud API"
second title: "เอกสาร"
link title: "นำเข้าข้อมูลโดยไม่ต้องใช้การจัดเก็บ"
type: docs
url: /import/without-using-storage/
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: "Aspose.Cells, Cloud API, นำเข้าข้อมูลโดยไม่ต้องใช้การจัดเก็บ, Excel import API, REST import"
description: "เรียนรู้วิธีการนำเข้าข้อมูลลงในสมุดงาน Excel โดยไม่ต้องใช้การจัดเก็บผ่าน Aspose.Cells Cloud API รวมถึงรูปแบบคำขอ พารามิเตอร์ ตัวอย่าง cURL โค้ด SDK และการจัดการข้อผิดพลาด"
weight: 10
ArticleTitle: "นำเข้าข้อมูลโดยไม่ต้องใช้การจัดเก็บ – Aspose.Cells Cloud API"
---

การนำเข้าข้อมูล Excel อาจซับซ้อนเนื่องจากมีหลายปัจจัยที่มีผลต่อผลลัพธ์ ปัจจัยทั้งหมดเหล่านี้ควรพิจารณาในระหว่างกระบวนการ **นำเข้า** Aspose.Cells Cloud ช่วยให้คุณนำเข้าข้อมูลและรูปแบบต่างๆ ลงในไฟล์ Excel ได้อย่างง่ายดายด้วยคุณภาพระดับมืออาชีพ

API นี้สำหรับ REST ใช้สำหรับการนำเข้า **ข้อมูล** ลงในไฟล์ Excel

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ประเภท           | ตำแหน่ง       | คำอธิบาย                                                                                                                                     |
| ---------------- | ---------------- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| file             | ไฟล์             | formData       | ไฟล์ Excel ที่จะอัปโหลด                                                                                                                       |
| ImportOption     | ImportOption     | JSON body      | ออบเจกต์ JSON ที่กำหนดข้อมูลที่จะนำเข้า ประเภทของข้อมูล (เช่น `IntArray`, `DoubleArray`, `StringArray`) และตำแหน่งที่จะวางลงในแผ่นงาน |

พารามิเตอร์ **ImportOption** มีคำอธิบายเพิ่มเติมในเอกสารอ้างอิง **ตัวเลือก ImportData** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter)

**ข้อกำหนดเบื้องต้น:**  
ต้องสร้างโทเคน JWT ที่ถูกต้องก่อนล่วงหน้า และขนาดไฟล์ต้องไม่เกินขีดจำกัดของบริการ (โดยทั่วไปคือ 100 MB) รูปแบบไฟล์ที่รองรับได้แก่ XLS, XLSX, CSV และ ODS หากต้องการใช้การเข้าถึงผ่านโปรแกรม ให้ตรวจสอบให้แน่ใจว่าได้ติดตั้ง SDK ที่เหมาะสมแล้ว

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-------------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                  | กรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

**หมายเหตุ:**  
เมื่อส่งคำขอ หัวข้อ `Content-Type: multipart/form-data` จะถูกตั้งค่าโดยอัตโนมัติผ่านตัวเลือก `-F` สำหรับข้อมูลขนาดใหญ่ ควรพิจารณาบีบอัดข้อมูลก่อนนำเข้า และจัดการการลองใหม่ (retry logic) สำหรับข้อผิดพลาดชั่วคราว

## วิธีใช้ API PostImportData ด้วย SDKs

### ข้อกำหนด API PostImportData

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*ตัวเลือก `-F` จะตั้งค่า `Content-Type: multipart/form-data` โดยอัตโนมัติ*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### ใช้ SDKs ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและอนุญาตให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}
---