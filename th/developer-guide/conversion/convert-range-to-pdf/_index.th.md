---
title: "แปลงช่วงข้อมูลใน Excel เป็น PDF ด้วย Aspose.Cells Cloud API"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงข้อมูลช่วงในสมุดงานในเครื่องเป็นไฟล์ PDF: คู่มือแบบทีละขั้นตอน"
linktype: "แปลงช่วงเป็น PDF"
type: docs
url: /th/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, แปลงช่วงข้อมูลใน Excel เป็น PDF, Excel เป็น PDF, การแปลงผ่านคลาวด์"
description: "แปลงช่วงข้อมูลเฉพาะจากสมุดงาน Excel ในเครื่องเป็น PDF โดยใช้ REST API ของ Aspose.Cells Cloud"
weight: 100
---

ส่งออกช่วงข้อมูลจากไฟล์ Excel ในเครื่องไปยังไฟล์ [PDF](https://docs.fileformat.com/pdf/) โดยใช้ Cloud API

**ข้อกำหนดเบื้องต้น**: ก่อนใช้งาน API นี้ คุณต้องมีบัญชี Aspose.Cells Cloud ที่ถูกต้อง โทเค็น JWT สำหรับการเข้าถึง และ (ทางเลือก) SDK ของ Aspose.Cells Cloud สำหรับภาษาการเขียนโปรแกรมที่คุณใช้ ตรวจสอบให้แน่ใจว่าได้กำหนดค่าพื้นที่จัดเก็บเป้าหมาย (ค่าเริ่มต้นหรือแบบกำหนดเอง) แล้ว หากคุณวางแผนจะใช้พารามิเตอร์ `outStorageName`

## **API แปลงช่วงเป็น PDF**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **ความปลอดภัยและการรับรองความถูกต้อง**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การรับรองความถูกต้องด้วยโทเค็น JWT</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                                                                 |
| ---------------- | ------------ | --------------------------- | ------------------------------------------------------------------------ |
| Spreadsheet      | ไฟล์         | FormData                    | อัปโหลดไฟล์สมุดงาน                                                      |
| worksheet        | สตริง         | Query                       | ชื่อแผ่นงานภายในสมุดงาน                                                |
| range            | สตริง         | Query                       | พื้นที่เซลล์ที่จะแปลง เช่น A1:C10                                      |
| outPath          | สตริง         | Query                       | (ทางเลือก) ตำแหน่งโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null           |
| outStorageName   | สตริง         | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์                                     |
| fontsLocation    | สตริง         | Query                       | ตำแหน่งที่เก็บแบบอักษรที่กำหนดเองสำหรับการใช้งานส่วนตัว               |
| region           | สตริง         | Query                       | การตั้งค่าภูมิภาคของสมุดงาน                                             |
| password         | สตริง         | Query                       | รหัสผ่านสำหรับเปิดไฟล์สมุดงาน                                           |

### **การตอบกลับ**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

*การตอบกลับทั่วไปคือสตรีมไบนารีของ PDF ที่ส่งกลับมาเป็นไฟล์ที่ให้ดาวน์โหลด*

**รหัสสถานะ HTTP**

| รหัส | ความหมาย             | คำอธิบาย                                                        |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | สำเร็จ (OK)          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของคำสั่ง |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)        |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                                  |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                              |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                        |

## **คุณควรใช้ API แปลงช่วงเป็น PDF ในการทำงานใดบ้าง?**

- **งบการเงิน**: แปลงงบดุล งบกำไรขาดทุน (ช่วงข้อมูลเฉพาะ) เป็น PDF เพื่อใช้เป็นเอกสารสำหรับการตรวจสอบ
- **รายงานการขาย**: แปลงแดชบอร์ดการขายหรือการคำนวณค่าคอมมิชชันเป็นไฟล์ PDF ที่สามารถจัดส่งได้
- **เมตริกการดำเนินงาน**: ส่งออกตาราง KPI และเมตริกประสิทธิภาพเป็นรายงาน PDF อย่างเป็นทางการ
- **ข้อมูลสัญญา**: ส่งออกตารางราคาและข้อตกลงระดับบริการจากสมุดงานเป็นไฟล์แนบ PDF
- **บันทึกการตรวจสอบ**: รักษาช่วงข้อมูลทางการเงินไว้ในรูปแบบ PDF ที่แก้ไขไม่ได้เพื่อใช้เป็นหลักฐาน
- **สรุปพอร์ตโฟลิโอ**: ส่งออกช่วงข้อมูลผลตอบแทนการลงทุนเป็นรายงาน PDF ที่พร้อมให้ลูกค้า
- **รายงานการควบคุมคุณภาพ**: ส่งออกช่วงข้อมูลการตรวจสอบเป็น PDF เพื่อใช้เป็นบันทึกการปฏิบัติตามข้อกำหนด
- **สรุปสินค้าคงคลัง**: แปลงตารางระดับสต๊อกเป็น PDF เพื่อใช้ในการทบทวนโดยผู้บริหาร

## **เหตุใดคุณจึงควรใช้ API แปลงช่วงเป็น PDF?**

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มีไลบรารี SDK ให้ใช้งานในหลายภาษา ช่วยให้พัฒนาแอปพลิเคชันได้อย่างรวดเร็ว และมีเอกสารอธิบายครบถ้วน เมื่อเทียบกับการสร้างโซลูชันสำหรับการเรนเดอร์กราฟิกแบบกำหนดเอง วิธีนี้ช่วยลดภาระงานพัฒนาอย่างมาก
- **คุ้มค่า**: คุณสามารถแปลงช่วงข้อมูลได้โดยไม่จำเป็นต้องอัปโหลดสมุดงานทั้งหมดก่อน ช่วยประหยัดพื้นที่จัดเก็บและลดค่าใช้จ่าย
- **คงรูปแบบ Excel ที่ซับซ้อนไว้ในรูปแบบ PDF ที่เข้าถึงได้ทั่วโลก**

## **วิธีการใช้ API แปลงช่วงเป็น PDF ด้วย SDK?**

### **ข้อมูลจำเพาะ API แปลงช่วงเป็น PDF**

[ข้อมูลจำเพาะ API แปลงช่วงเป็น PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และอนุญาตให้คุณโต้ตอบกับ REST API โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### **ใช้งาน SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ให้คุณสามารถแปลงช่วงข้อมูลเป็นไฟล์ PDF ได้ด้วยโค้ดที่กระชับ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}