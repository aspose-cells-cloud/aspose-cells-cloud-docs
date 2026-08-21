---
---
title: "ส่งออกตาราง – API 云 Aspose.Cells | แปลง Excel เป็น PDF, PNG, CSV"
second_title: "เอกสาร"
ArticleTitle: "วิธีส่งออกตารางสเปรดชีตแบบรีโมทไปยังรูปแบบอื่น: คู่มือแบบทีละขั้นตอน"
linktype: "ส่งออกตารางไปยังรูปแบบที่ระบุ"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells, ส่งออกตาราง, Excel เป็น PDF, API 云, REST"
description: "ส่งออกตาราง Excel แบบเก็บบนคลาวด์ไปยังไฟล์รูปแบบต่างๆ เช่น PDF, PNG, CSV, JSON หรือรูปแบบอื่นๆ โดยใช้ Aspose.Cells Cloud API ด้วยปลายทาง HTTPS ที่มีความปลอดภัย การยืนยันตัวตนด้วย JWT และตัวอย่าง SDK"
weight: 100
---

ส่งออกตารางของไฟล์สเปรดชีต (Excel) ที่เก็บไว้บนคลาวด์ไปยังไฟล์รูปแบบอื่น

## **API ส่งออกตารางเป็นรูปแบบ**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTPBody | คำอธิบาย                                                                                                                                       |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| name           | String | Path                       | **จำเป็น** ชื่อของไฟล์สมุดงานที่ต้องการดึงข้อมูล                                                                                      |
| worksheet      | String | Path                       | ชื่อของแผ่นงาน                                                                                                                            |
| tableName      | String | Path                       | ชื่อของตาราง                                                                                                                                |
| format         | String | Query                      | **จำเป็น** รูปแบบผลลัพธ์ที่ต้องการ (เช่น "png", "pdf", "svg")                                                                              |
| folder         | String | Query                      | ทางเลือก เส้นทางของโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ `null`                                                                        |
| storageName    | String | Query                      | ทางเลือก ชื่อของพื้นที่จัดเก็บในคลาวด์แบบกำหนดเอง ใช้พื้นที่จัดเก็บเริ่มต้นหากไม่ระบุ                                                  |
| outPath        | String | Query                      | ทางเลือก เส้นทางของโฟลเดอร์สำหรับพื้นที่จัดเก็บผลลัพธ์ ค่าเริ่มต้นคือ `null`                                                                                  |
| outStorageName | String | Query                      | ทางเลือก ชื่อของพื้นที่จัดเก็บไฟล์ผลลัพธ์                                                                                                        |
| fontsLocation  | String | Query                      | ทางเลือก ตำแหน่งของฟอนต์แบบกำหนดเอง                                                                                                              |
| region         | String | Query                      | ทางเลือก การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อการจัดรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมที่ขึ้นกับภาษาท้องถิ่น |
| password       | String | Query                      | ทางเลือก รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต                                                                                              |

### **คำตอบ**

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

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)                    | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของปฏิบัติการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | ข้อมูลหนักเกินไป (Payload Too Large)     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                 |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                          |

## **ควรใช้ API ส่งออกตารางเป็นรูปแบบอื่นในกรณีใด?**

- **การย้ายระบบเก่า**: แปลงไฟล์ XLS เก่าหลายพันไฟล์เป็น XLSX เพื่อใช้กับระบบสมัยใหม่
- **การมาตรฐานการจัดเก็บข้อมูล**: ทำให้รูปแบบสเปรดชีตต่างๆ (XLS, XLSM, ODS, CSV) เป็นรูปแบบเดียวกันสำหรับการเก็บถาวร
- **การเชื่อมต่อกับชุดโปรแกรมสำนักงานอื่นๆ**: แปลงไฟล์ Excel เป็นรูปแบบที่ใช้ได้กับ LibreOffice, Google Sheets หรือ Apple Numbers
- **การมาตรฐานแหล่งข้อมูล**: แปลงรูปแบบสเปรดชีตต่างๆ เป็น CSV หรือ JSON เพื่อนำเข้าสู่ฐานข้อมูล
- **การเผยแพร่บนเว็บ**: แปลงโมเดลทางการเงินเป็น HTML เพื่อแสดงผลบนเว็บไซต์

## **เหตุใดจึงควรใช้ API ส่งออกตารางเป็นรูปแบบอื่น?**

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK รองรับหลายภาษา ช่วยให้พัฒนาได้อย่างรวดเร็ว และมีเอกสารประกอบที่ครบถ้วน เมื่อเทียบกับการสร้างโซลูชันการเรนเดอร์กราฟิกแบบกำหนดเอง วิธีนี้ช่วยลดภาระงานในการพัฒนาอย่างมาก
- **ลดค่าใช้จ่ายด้านแรงงาน**: ลดความจำเป็นในการจ้างบุคลากรเฉพาะด้านสำหรับการรวมเอกสาร
- **จ่ายตามการใช้งาน**: ไม่ต้องลงทุนล่วงหน้า จ่ายเฉพาะเมื่อใช้งาน API จริง
- **ไม่มีค่าใช้จ่ายในการดูแลรักษา**: ไม่ต้องดูแลเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่ต้องจัดการปัญหาความเข้ากันได้
- **API จะส่งกลับเฉพาะข้อมูลตารางดิบโดยไม่มีการจัดรูปแบบสมุดงานใดๆ**

## **วิธีใช้ API ส่งออกตารางสเปรดชีตเป็นรูปแบบด้วย SDK?**

### **สเปค API ส่งออกตารางเป็นรูปแบบ**

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">สเปค API ส่งออกตารางเป็นรูปแบบ</a> กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณใช้งาน REST ได้โดยตรงจากเบราว์เซอร์เว็บ

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

### **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เพราะช่วยซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถส่งออกตารางสเปรดชีตเป็นไฟล์รูปแบบต่างๆ ด้วยโค้ดที่สั้นกระชับ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}