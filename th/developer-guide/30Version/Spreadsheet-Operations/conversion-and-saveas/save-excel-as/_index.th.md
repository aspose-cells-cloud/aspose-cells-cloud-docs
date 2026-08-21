---
title: "บันทึกสมุดงาน Excel – API ของ Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "บันทึกเป็น"
type: docs
url: /save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, บันทึกเป็น, PDF, CSV, JSON, Markdown, REST API"
description: "บันทึกสมุดงาน Excel ไปยังรูปแบบต่างๆ เช่น PDF, CSV, JSON, Markdown และอื่นๆ โดยใช้ REST API ของ Aspose.Cells Cloud"
weight: 30
---

API นี้ช่วยให้คุณสามารถ **บันทึก** ไฟล์ Excel ไปยังรูปแบบต่างๆ ได้  
ก่อนที่จะเรียกใช้ปลายทางนี้ คุณต้องมีโทเค็นการเข้าถึง OAuth 2.0 ที่ถูกต้อง และสมุดงานต้นฉบับต้องถูกเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud ของคุณแล้ว

**ข้อกำหนดเบื้องต้น**  
1. รับโทเค็น JWT และใส่ในส่วนหัว `Authorization: Bearer <token>` ของคำขอทุกคำขอ  
2. อัปโหลดสมุดงานต้นฉบับไปยังพื้นที่จัดเก็บของ Aspose Cloud (หรือยืนยันว่ามีอยู่แล้ว)  
3. ทราบชื่อพื้นที่จัดเก็บและเส้นทางโฟลเดอร์ที่สมุดงานนั้นอยู่

## API PostWorkbookSaveAs

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์เส้นทาง**

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                     |
| ---------------- | ------ | ----------------------------- |
| name             | string | ชื่อของไฟล์ Excel             |

### **พารามิเตอร์แบบคิวรี**

| ชื่อพารามิเตอร์        | ประเภท | คำอธิบาย                                                                                             |
| ----------------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| newfilename             | string | ชื่อไฟล์ใหม่สำหรับเอกสารที่บันทึกไว้                                                                  |
| isAutoFitRows           | string | หากเป็น `true` จะปรับความสูงของแถวทั้งหมดในสมุดงานโดยอัตโนมัติ ค่าเริ่มต้นคือ `false`                 |
| isAutoFitColumns        | string | หากเป็น `true` จะปรับความกว้างของคอลัมน์ในสมุดงานโดยอัตโนมัติ ค่าเริ่มต้นคือ `false`                  |
| folder                  | string | โฟลเดอร์ที่มีสมุดงานต้นฉบับ                                                                          |
| storageName             | string | ชื่อของพื้นที่จัดเก็บที่มีไฟล์ต้นฉบับ                                                                |
| outStorageName          | string | ชื่อของพื้นที่จัดเก็บที่จะบันทึกไฟล์ผลลัพธ์                                                          |
| checkExcelRestriction   | bool   | ระบุว่าจะบังคับข้อจำกัดของ Excel เมื่อแก้ไขเซลล์หรือวัตถุที่เกี่ยวข้องหรือไม่                       |
| region                  | string | การตั้งค่าภูมิภาคที่ใช้กับสมุดงาน                                                                     |
| pageWideFitOnPerSheet   | bool   | ปรับความกว้างของหน้าให้พอดีกับแต่ละแผ่นงานเมื่อแปลง                                                   |
| pageTallFitOnPerSheet   | bool   | ปรับความสูงของหน้าให้พอดีกับแต่ละแผ่นงานเมื่อแปลง                                                   |
| sheetName               | string | ชื่อของแผ่นงานที่จะแปลง                                                                              |
| pageIndex               | string | ดัชนีของหน้าที่จะแปลงภายในแผ่นงานที่ระบุ (ต้องระบุ `sheetName`)                                     |
| onePagePerSheet         | bool   | เมื่อแปลงเป็น PDF จะสร้างหนึ่งหน้าต่อหนึ่งแผ่นงาน                                                    |

### **พารามิเตอร์เนื้อหาคำขอ**

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย                                                           |
| ---------------- | ------ | ------------------------------------------------------------------- |
| SaveOptions      | Object | ตัวเลือกการบันทึกที่ส่งมาในส่วนที่สองของคำขอแบบมัลติพาร์ท (multipart) |

**ตัวอย่างเนื้อหาคำขอ (ส่วน JSON ของคำขอแบบมัลติพาร์ท)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### ผลลัพธ์

API จะส่งกลับวัตถุ `SaveResponse`

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                                                 |
|------|-----------------------------|---------------------------------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองสำเร็จ; ผลลัพธ์ประกอบด้วยรายละเอียดของการดำเนินการ          |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)             |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือหายไป                                           |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                        |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                |

## วิธีใช้ API PostWorkbookSaveAs ด้วย SDK

### ข้อมูลจำเพาะ API PostWorkbookSaveAs

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้ **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="ผลลัพธ์" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">คลังข้อมูลบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

สำหรับกรณีการแปลงอื่นๆ โปรดดูคู่มือ [แปลง Excel เป็น PDF](/convert-excel-to-pdf/) และ [ส่งออก Excel เป็น CSV](/export-excel-to-csv/)