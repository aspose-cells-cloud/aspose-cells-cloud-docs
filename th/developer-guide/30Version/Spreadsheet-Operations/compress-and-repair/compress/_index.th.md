---
title: "บีบอัดข้อมูลในไฟล์ Excel"
ArticleTitle: "บีบอัดข้อมูลในไฟล์ Excel – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "docs"
url: /compress-excel-files/
aliases: [/compress/]
keywords: "บีบอัดไฟล์ excel, aspose cells cloud, การบีบอัด excel, การบีบอัดสเปรดชีต, rest api, การบีบอัดไฟล์"
description: "บีบอัดไฟล์ Excel (XLS, XLSX, XLSM, XLSB, ODS) โดยใช้ REST API ของ Aspose.Cells Cloud ตั้งระดับการบีบอัด จัดการหลายไฟล์ และผสานรวมผ่าน SDK"
weight: 39
---

## API PostCompress ของเว็บเซอร์วิส Aspose.Cells Cloud

**ข้อกำหนดเบื้องต้น:**  
- ต้องมีโทเคน JWT ที่ถูกต้องสำหรับการตรวจสอบสิทธิ์  
- รูปแบบไฟล์ที่รองรับคือ XLS, XLSX, XLSM, XLSB และ ODS  
- ขนาดไฟล์สูงสุดที่อนุญาตคือ 500 MB ต่อคำขอ (ขึ้นอยู่กับข้อจำกัดของบริการ)

REST API นี้ใช้บีบอัดข้อมูลในไฟล์ Excel

- บีบอัดไฟล์ XLS, XLSX, XLSM, XLSB, ODS  
- บีบอัดไฟล์สเปรดชีต Excel หลายไฟล์ได้อย่างรวดเร็ว  
- เลือกระดับการบีบอัดได้ตามต้องการ  
- รองรับหลายไฟล์

### จุดสิ้นสุดเว็บ API

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย                                     |
|----------------|----------|-----------------------------|----------------------------------------------|
| file           | ไฟล์      | formData                    | ไฟล์ที่จะอัปโหลด                             |
| CompressLevel  | จำนวนเต็ม | query                       | ระดับการบีบอัด (0‑100); ค่าที่สูงขึ้นหมายถึงการบีบอัดที่เข้มงวดกว่า |

### พารามิเตอร์เนื้อความคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย                                      |
| -------------- | --------- | --------------------------------------------- |
| data           | ไฟล์      | เนื้อหาไบนารีของไฟล์เวิร์กบุ๊กที่ต้องการบีบอัด |

### **การตอบกลับ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[ชื่อไฟล์ที่รวมแล้ว]",
    "Filesize" : [ขนาดไฟล์],
    "FileContent" : "[Base64String]"
}
```

*หมายเหตุ:* `FileContent` ประกอบด้วยเวิร์กบุ๊กที่บีบอัดแล้วซึ่งเข้ารหัสเป็นสตริง Base64 ความยาวของสตริงนี้สอดคล้องกับขนาดของไฟล์ที่บีบอัด คุณสามารถถอดรหัสโดยใช้เครื่องมือ Base64 มาตรฐานเพื่อเรียกคืนไฟล์ Excel ในรูปแบบไบนารี

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                      |
|-----|-----------------------------|-----------------------------------------------|
| 200 | สำเร็จ (OK)                 | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                 |
| 413 | เนื้อหาคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ API PostCompress ด้วย SDK

### ข้อมูลจำเพาะ API PostCompress

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL แบบคำสั่งบรรทัดเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}