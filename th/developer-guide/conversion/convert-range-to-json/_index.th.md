---
---
title: "Aspose.Cells Cloud Web API - แปลงข้อมูลช่วงในไฟล์ Excel ท้องถิ่นเป็นไฟล์ JSON - เครื่องมือออนไลน์ฟรี"
second title: "เอกสาร"
ArticleTitle: "วิธีการแปลงข้อมูลช่วงในไฟล์สเปรดชีตท้องถิ่นเป็นไฟล์ JSON: คู่มือแบบทีละขั้นตอน"
linktype: "แปลงช่วงเป็น JSON"
type: docs
url: /convert-range-to-json/
keywords: "แปลงช่วงเป็น JSON, Aspose.Cells Cloud, Excel เป็น JSON, การแปลงสเปรดชีต, API"
description: "แปลงช่วงที่ระบุจากไฟล์ Excel ท้องถิ่นเป็น JSON โดยใช้ Aspose.Cells Cloud API"
weight: 100
---

ส่งออกข้อมูลช่วงจากไฟล์ Excel ท้องถิ่นเป็นไฟล์ JSON โดยใช้ Cloud API

## **API สำหรับการแปลงช่วงเป็น JSON**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนแบบ JWT token</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย                                                                 |
| ---------------- | ------ | --------------------------- | ------------------------------------------------------------------------ |
| Spreadsheet      | ไฟล์  | FormData                    | อัปโหลดไฟล์สเปรดชีต                                                     |
| worksheet        | สตริง | Query                       | ชื่อของworksheet ในไฟล์สเปรดชีต                                          |
| range            | สตริง | Query                       | พื้นที่เซลล์ที่ต้องการแปลง เช่น A1:C10                                 |
| outPath          | สตริง | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน; ค่าเริ่มต้นคือ null         |
| outStorageName   | สตริง | Query                       | ชื่อของพื้นที่จัดเก็บไฟล์ผลลัพธ์                                         |
| fontsLocation    | สตริง | Query                       | ตำแหน่งที่จัดเก็บฟอนต์ที่กำหนดเองสำหรับการใช้งานส่วนตัว                |
| region           | สตริง | Query                       | การตั้งค่าภูมิภาคของสเปรดชีต                                            |
| password         | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต                                          |

### **คำตอบ (Response)**

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

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                | คำอธิบาย                                                       |
| ---- | ------------------------ | -------------------------------------------------------------- |
| 200  | คำขอสำเร็จ (OK)         | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)  |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                  |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                             |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                      |

## **คุณควรใช้ API สำหรับการแปลงช่วงเป็น JSON ที่ใด?**

- แดชบอร์ดแบบเรียลไทม์: แปลงข้อมูล Excel แบบสดเป็น JSON เพื่อนำไปใช้กับไลบรารีกราฟฟิกเช่น Chart.js หรือ D3.js
- Spreadsheet-as-a-Service: เปิดเผยช่วงของไฟล์ Excel เป็น JSON endpoints ให้กับบริการอื่นๆ
- ข้อมูลพื้นหลังสำหรับ Webhook: แปลงข้อมูลสเปรดชีตเป็น JSON เพื่อใช้ในการแจ้งเตือนผ่าน webhook
- การพัฒนาต้นแบบข้อมูลอย่างรวดเร็ว: แปลงข้อมูล Excel ที่ผ่านการปรับปรุงแล้วเป็น JSON เพื่อใช้ในการวิเคราะห์ด้วย Python หรือ R อย่างรวดเร็ว
- ระบบไปป์ไลน์การเรียนรู้ของเครื่อง (Machine-learning pipelines): ประมวลผลข้อมูลฝึกอบรมที่เก็บอยู่ในสเปรดชีตที่ผู้ใช้ธุรกิจเป็นผู้ดูแล
- การดำเนินงานด้านอีคอมเมิร์ซ: ซิงค์แคต ALOGสินค้าหรือแผ่นราคาเป็นเว็บไซต์ผ่าน JSON
- การทำรายงานอัตโนมัติ: สร้างข้อมูล JSON feeds จากแบบจำลองการเงินเพื่อใช้ในการทำรายงานอัตโนมัติ
- การตั้งค่าแอปพลิเคชัน: จัดการค่าตัวแปรคุณสมบัติ (feature flags), การตั้งค่า หรือพารามิเตอร์การทดสอบ A/B ที่เก็บไว้ใน Excel → JSON
- การรองรับหลายภาษา: แปลงสเปรดชีตที่ใช้สำหรับการแปลเป็น JSON เพื่อใช้กับไลบรารี i18n
- เมนู/การนำทางแบบไดนามิก: เก็บโครงสร้างการนำทางเว็บไซต์ไว้ใน Excel และปรับใช้ในรูปแบบ JSON

_สำหรับตัวเลือกการแปลงอื่นๆ โปรดดูคู่มือ [แปลงช่วงเป็น CSV](/convert-range-to-csv/)_

## เหตุใดคุณจึงควรใช้ API สำหรับการแปลงช่วงเป็น JSON?

- **การรองรับ SDK**: Aspose.Cells Cloud มีไลบรารีสำหรับภาษาต่างๆ หลายภาษา ลดปริมาณโค้ดที่ต้องเขียนเอง
- **ลดต้นทุนการจัดเก็บ**: สามารถแปลงช่วงข้อมูลได้โดยไม่จำเป็นต้องอัปโหลดสมุดงานทั้งหมดก่อน ช่วยประหยัดพื้นที่จัดเก็บ
- **เข้ากับแอปพลิเคชันเว็บและมือถือ**: JSON เป็นรูปแบบข้อมูลดั้งเดิมสำหรับเฟรมเวิร์ก JavaScript สมัยใหม่ เช่น React, Vue และ Angular
- **การรองรับภาษาอย่างกว้างขวาง**: แทบทุกภาษาการเขียนโปรแกรมและฐานข้อมูลสามารถใช้งาน JSON ได้
- **การรักษาโครงสร้างข้อมูล**
  - **การตรวจจับโครงสร้างอัจฉริยะ**: แปลงข้อมูลตารางให้เป็นอาเรย์หรือออบเจกต์ JSON ที่ถูกต้องโดยอัตโนมัติ
  - **การแมปคอลัมน์หัวเรื่อง**: ใช้แถวแรกเป็นคีย์ JSON เพื่อให้โครงสร้างออบเจกต์สะอาด
  - **การรักษาชนิดข้อมูล**: รักษาชนิดข้อมูลตัวเลข วันที่ และค่าบูลีนไว้ แทนที่จะแปลงเป็นข้อความธรรมดา

## วิธีใช้ API สำหรับการแปลงช่วงเป็น JSON ด้วย SDK?

### ข้อมูลจำเพาะ API สำหรับการแปลงช่วงเป็น JSON

[ข้อมูลจำเพาะ API สำหรับการแปลงช่วงเป็น JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API คลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจากซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถแปลงช่วงข้อมูลเป็นไฟล์ JSON ด้วยโค้ดที่กระชับได้  
โปรดดูที่ [คลังข้อมูล GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}