---
title: "Aspose.Cells Cloud Web API – ลบแถวว่าง/แถวที่ไม่มีข้อมูลโดยอัตโนมัติ"
second_title: "เอกสาร"
ArticleTitle: "วิธีลบแถวว่างทั้งหมดใน Excel – คู่มือการจัดการข้อมูลอย่างสมบูรณ์"
linktype: "ลบแถวว่าง"
type: docs
url: /th/delete-spreadsheet-blank-rows/
keywords: "Aspose.Cells, Excel, แถวว่าง, ลบแถว, การทำความสะอาดสเปรดชีต, API"
description: "ลบแถวที่ว่างทั้งหมดจากไฟล์ Excel ผ่าน Aspose.Cells Cloud API รวดเร็ว พร้อมสำหรับการประมวลผลเป็นชุด และสามารถเขียนโปรแกรมได้อย่างเต็มรูปแบบ – ดูตัวอย่างโค้ดใน C#, Java, Python และอื่นๆ"
weight: 100
---

ลบแถวว่างทั้งหมดจากสเปรดชีต Excel โดยใช้ Aspose.Cells Cloud API ระบบ API อัจฉริยะของเราจะตรวจจับและลบแถวที่ไม่มีข้อมูล สูตร ความคิดเห็น หรือวัตถุใดๆ ทั้งสิ้น ทั้งยังคงรักษาเนื้อหาอื่นๆ ไว้อย่างสมบูรณ์ รองรับการประมวลผลเป็นชุด การทำอัตโนมัติบนคลาวด์ และการผสานรวมอย่างราบรื่นสำหรับเวิร์กโฟลว์การทำความสะอาดข้อมูลในองค์กร

## API DeleteSpreadsheetBlankRows

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```


### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                                                                                    |
| ---------------- | -------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ไฟล์   | FormData | ไฟล์ Excel (`.xlsx`, `.xls`, `.ods` เป็นต้น) ที่จะประมวลผล                                                                                     |
| outPath          | สตริง | Query    | (ไม่บังคับ) ไดเรกทอรีเป้าหมายในที่จัดเก็บบนคลาวด์สำหรับสมุดงานที่ผ่านการทำความสะอาดแล้ว หากไม่ระบุ ไฟล์จะถูกบันทึกไว้ใกล้กับไฟล์ต้นฉบับ        |
| outStorageName   | สตริง | Query    | ชื่อของที่จัดเก็บบนคลาวด์ที่กำหนดค่าไว้ (เช่น `MyDropbox`, `CorporateOneDrive`) จำเป็นเมื่อต้องการบันทึกผลลัพธ์ลงในที่จัดเก็บเฉพาะเจาะจง         |
| region           | สตริง | Query    | การตั้งค่าภาษาและภูมิภาค (เช่น `en-US`, `fr-FR`) ที่ใช้ระหว่างการประมวลผล                                                           |
| password         | สตริง | Query    | รหัสผ่านสำหรับเปิดสเปรดชีตที่เข้ารหัส ละเว้นหากไฟล์ไม่ได้รับการป้องกันด้วยรหัสผ่าน                                               |

**การยืนยันตัวตน**  
คำขอทั้งหมดต้องระบุส่วนหัว `Authorization: Bearer <access_token>` รับ access token ได้จากขั้นตอน OAuth2 ของ Aspose Cloud ซึ่งระบุไว้ในคู่มือการยืนยันตัวตน

**ข้อกำหนดเบื้องต้นและหมายเหตุ**  
- ตรวจสอบให้แน่ใจว่าที่จัดเก็บบนคลาวด์ของคุณได้รับการกำหนดค่าไว้แล้ว และสมุดงานต้นฉบับได้รับการอัปโหลดไว้ก่อนเรียกใช้ API  
- รูปแบบไฟล์ที่รองรับ ได้แก่ `.xlsx`, `.xls`, `.ods` และรูปแบบสเปรดชีตทั่วไปอื่นๆ  
- ขนาดไฟล์สูงสุดคือ 150 MB ต่อคำขอเดียว; ไฟล์ที่มีขนาดใหญ่กว่านั้นควรประมวลผลแบบแบ่งเป็นชุด  

### คำตอบ

API จะส่งกลับอาร์เรย์ JSON ที่มีข้อมูลอ้างอิงถึงไฟล์ที่ประมวลผลแล้ว

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

### รหัสข้อผิดพลาด

- **400 Bad Request** – URI ของ Aspose.Cells Cloud API ไม่ถูกต้อง
- **401 Unauthorized** – access token หรือข้อมูลประจำตัวของไคลเอนต์ไม่ถูกต้อง
- **404 Not Found** – ไม่สามารถเข้าถึงไฟล์สเปรดชีตได้
- **500 Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดขณะประมวลผลไฟล์

## ควรใช้ API ลบแถวว่างจากสเปรดชีตในกรณีใด?

- **เวิร์กโฟลว์การนำเข้าและทำความสะอาดข้อมูล** – ลบแถวว่างที่อยู่ท้ายหรือโครงสร้างที่ไม่จำเป็นทันทีหลังจากนำเข้าข้อมูลจาก CSV ฐานข้อมูล หรือ API บนเว็บ
- **การสร้างรายงานและแดชบอร์ด** – สร้างเค้าโครงที่ดูเป็นมืออาชีพโดยการลบแถวว่างที่ไม่จำเป็นออกก่อนการสรุปรายงานด้านการเงิน การขาย หรือปฏิบัติการ
- **การเตรียมข้อมูลสำหรับการวิเคราะห์ (ETL)** – ประมวลผลข้อมูล Excel ในพายpline ETL ก่อนโหลดลงในคลังข้อมูล (Snowflake, BigQuery) หรือเครื่องมือ BI (Tableau, Power BI)
- **การผสานรวมระบบและฟีด API** – ปรับมาตรฐานไฟล์ Excel ที่ได้รับจากระบบพันธมิตร CRM หรือ ERP โดยการตัดแถวที่ไม่ได้ใช้ออก
- **การสร้างเอกสารอัตโนมัติและการประมวลผลแบบชุด** – ลบแถวตัวอย่างที่ถูกสร้างขึ้นโดยระบบ template engine ก่อนการจัดส่ง
- **การประมวลผลเนื้อหาที่ผู้ใช้สร้างขึ้น** – มาตรฐานไฟล์ Excel ที่อัปโหลดจากพอร์ทัลหรือแอปพลิเคชันเว็บ ก่อนการประมวลผลหรือจัดเก็บเพิ่มเติม
- **การย้ายข้อมูลเก่า** – ทำให้คลังสเปรดชีตเก่ามีความเรียบร้อยขึ้นโดยการลบแถวว่างหรือแถวตัวอย่างที่มีมาแต่เดิมออก

## เหตุใดควรใช้ API ลบแถวว่างจากสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา** – มี SDK ให้ใช้งานในหลายภาษา ลดความพยายามในการพัฒนาเทียบกับการสร้างโซลูชันแบบกำหนดเอง
- **ลดต้นทุนแรงงาน** – ไม่จำเป็นต้องทำความสะอาดสเปรดชีตด้วยตนเองหรือจ้างบุคลากรเฉพาะด้าน
- **จ่ายตามการใช้งานจริง** – จ่ายเฉพาะค่า API ที่เรียกใช้งานจริงเท่านั้น
- **ไม่มีต้นทุนการดูแลรักษา** – ไม่ต้องจัดการเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่มีปัญหาเรื่องความเข้ากันได้

## วิธีใช้ API ลบแถวว่างจากสเปรดชีตผ่าน SDK

### สเปคของ API ลบแถวว่างจากสเปรดชีต

[สเปคของ API ลบแถวว่างจากสเปรดชีต](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณใช้งาน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้งาน Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถลบแถวว่างจากสเปรดชีตได้ด้วยโค้ดเพียงไม่กี่บรรทัด  
โปรดดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}  
{{</tab>}}  
{{< /tabs >}}