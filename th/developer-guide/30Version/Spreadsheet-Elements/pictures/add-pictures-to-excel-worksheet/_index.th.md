---
title: "เพิ่มรูปภาพลงในไฟล์ Excel"
second_title: "เอกสาร"
linktitle: "เพิ่ม"
type: docs
url: /th/pictures/add/
aliases: [  /th/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, add picture, REST API"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อเพิ่มรูปภาพลงในแผ่นงาน Excel SDK สำหรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift ช่วยให้การผสานรวมข้ามแพลตฟอร์มทำได้ง่ายขึ้น"
weight: 20
ArticleTitle: "เพิ่มรูปภาพลงในแผ่นงาน Excel – Aspose.Cells Cloud API"
---

REST API นี้จะเพิ่มรูปภาพใหม่ลงในแผ่นงาน Excel  
**ข้อกำหนดเบื้องต้น:** คุณต้องมีโทเคนยืนยันตัวตนของ Aspose Cloud ที่ถูกต้อง มีสมุดงานที่มีอยู่แล้วซึ่งจัดเก็บไว้ในพื้นที่เก็บข้อมูลที่รองรับ และมีสิทธิ์ที่เหมาะสมในการแก้ไขแผ่นงาน

## API PutWorksheetAddPicture

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| ---------------- | ------- | -------- | -------------------------------------------------------------------------------------------- |
| name             | string  | path     | ชื่อสมุดงาน |
| sheetName        | string  | path     | ชื่อแผ่นงาน |
| picture          | object  | body     | ออบเจกต์รูปภาพ (ข้อมูลไบนารี) |
| upperLeftRow     | integer | query    | ดัชนีที่เริ่มต้นที่ 0 ของแถวบนซ้ายที่จะวางรูปภาพ |
| upperLeftColumn  | integer | query    | ดัชนีที่เริ่มต้นที่ 0 ของคอลัมน์บนซ้ายที่จะวางรูปภาพ |
| lowerRightRow    | integer | query    | ดัชนีที่เริ่มต้นที่ 0 ของแถวล่างขวาของพื้นที่รูปภาพ |
| lowerRightColumn | integer | query    | ดัชนีที่เริ่มต้นที่ 0 ของคอลัมน์ล่างขวาของพื้นที่รูปภาพ |
| picturePath      | string  | query    | ตำแหน่งไฟล์รูปภาพ; หากไม่ระบุ ข้อมูลรูปภาพจะต้องส่งในเนื้อหาคำขอ |
| folder           | string  | query    | โฟลเดอร์ที่เก็บสมุดงานไว้ |
| storageName      | string  | query    | ชื่อของบริการพื้นที่เก็บข้อมูล |

**หมายเหตุเกี่ยวกับเนื้อหาคำขอ:** เมื่อไม่ระบุ `picturePath` ให้ส่งข้อมูลรูปภาพแบบไบนารีในเนื้อหาคำขอโดยใช้ `multipart/form-data`

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK) | กรองถูกใช้งานเรียบร้อยแล้ว คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลที่ส่งมามีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |

**ตัวอย่างโครงสร้างคำตอบสำหรับสถานะ 200**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**หมายเหตุ:** ขนาดรูปภาพสูงสุดคือ 10 เมกะไบต์ ไฟล์ที่มีขนาดใหญ่กว่านี้จะถูกปฏิเสธด้วยคำตอบ `400 Bad Request`

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ผ่านเบราว์เซอร์เว็บได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
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

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณได้ ดังนั้นคุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**หมายเหตุ:** รูปแบบภาพที่รองรับ ได้แก่ PNG, JPEG, BMP และ GIF ขนาดรูปภาพสูงสุดคือ 10 เมกะไบต์ ไฟล์ที่มีขนาดใหญ่กว่านี้จะถูกปฏิเสธด้วยคำตอบ `400 Bad Request`