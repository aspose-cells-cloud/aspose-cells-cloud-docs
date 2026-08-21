---
title: "ค้นหาเนื้อหาในสเปรดชีต – Aspose.Cells Cloud API (ค้นหาข้อความใน Excel)"
second_title: "เอกสาร"
ArticleTitle: "ค้นหาข้อความในสเปรดชีต Excel บนเครื่อง – ค้นหาข้อมูลที่เฉพาะเจาะจง"
linktype: "docs"
url: /search-spreadsheet-content/
keywords: "Aspose.Cells, API ค้นหา Excel, การค้นหาเนื้อหาในสเปรดชีต, API สเปรดชีตบนคลาวด์, การค้นหาข้อความ"
description: "ใช้ Aspose.Cells Cloud API เพื่อค้นหาข้อความ ตัวเลข หรือสูตรในไฟล์ Excel บนเครื่องของคุณ รองรับการค้นหาแบบไม่คำนึงถึงตัวพิมพ์เล็ก-ใหญ่ การจำกัดขอบเขตตามแผ่นงาน และการยืนยันตัวตนแบบปลอดภัย"
weight: 100
---

## **API สำหรับค้นหาเนื้อหาในสเปรดชีต**

ค้นหาข้อความเฉพาะใดๆ ภายในสเปรดชีต Excel ใดๆ โดยใช้ Aspose.Cells Cloud API อย่างเป็นโปรแกรม ซึ่ง API นี้สามารถค้นหาข้อความ ตัวเลข หรือสูตรในไฟล์ที่จัดเก็บไว้บนคลาวด์ ช่วยให้สามารถค้นหาข้อมูลโดยอัตโนมัติ วิเคราะห์เนื้อหา และดำเนินกระบวนการตรวจสอบสเปรดชีตได้

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

หากคุณต้องการใช้ HTTP แบบดิบ ตัวอย่าง cURL ต่อไปนี้แสดงคำขอเดียวกัน:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### **พารามิเตอร์ของคำขอ**

| พารามิเตอร์      | ชนิดข้อมูล | ตำแหน่ง     | คำอธิบาย                                                                                     |
| ---------------- | ---------- | ------------ | -------------------------------------------------------------------------------------------- |
| spreadsheet      | ไฟล์       | FormData     | ไฟล์ Excel ที่ต้องการค้นหา                                                                   |
| searchText       | สตริง       | Query        | ข้อความ (หรือค่าตัวเลข) ที่ต้องการค้นหาในสมุดงาน                                              |
| ignoringCase     | บูลีน       | Query        | ตั้งค่าเป็น `true` เพื่อดำเนินการค้นหาแบบไม่คำนึงถึงตัวพิมพ์เล็ก-ใหญ่                           |
| worksheet        | สตริง       | Query        | ชื่อของแผ่นงานที่จำกัดขอบเขตการค้นหา หากไม่ระบุ จะสแกนแผ่นงานทั้งหมด                        |
| cellArea         | สตริง       | Query        | ช่วงแบบ A-1 (เช่น `A1:C10`) ที่จำกัดพื้นที่การค้นหา                                            |
| region           | สตริง       | Query        | ภูมิภาคทางภูมิศาสตร์ของบริการ (เช่น `us-east-1`)                                              |
| password         | สตริง       | Query        | รหัสผ่านที่จำเป็นสำหรับการเปิดสมุดงานที่ได้รับการป้องกัน                                        |

### **การตอบกลับ**

API จะส่งกลับวัตถุ `SearchResult` ซึ่งประกอบด้วยอาเรย์ของเซลล์ที่ตรงกัน โดยแต่ละองค์ประกอบจะให้ชื่อแผ่นงาน ที่อยู่เซลล์ และข้อความที่ตรงกัน

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### รหัสข้อผิดพลาด

- **400 Bad Request** – URI หรือพารามิเตอร์ของคำขอนั้นไม่ถูกต้อง
- **401 Unauthorized** – ไม่มีหรือโทเค็นการเข้าถึงไม่ถูกต้อง หรือข้อมูลประจำตัวของไคลเอนต์ไม่ถูกต้อง
- **404 Not Found** – ไม่สามารถเข้าถึงสเปรดชีตที่ระบุได้
- **500 Internal Server Error** – เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิดขณะประมวลผลสมุดงาน

## ควรใช้ API ค้นหาเนื้อหาในสเปรดชีตในกรณีใด?

- **การตรวจสอบความสอดคล้องของสมุดงานโดยรอบ** – สแกนสมุดงานทั้งหมดเพื่อค้นหาคำที่ละเอียดอ่อน (เช่น “ข้อกำหนดความลับ”, “ข้อมูลภายใน”) เพื่อใช้ในการตรวจสอบความปลอดภัยของข้อมูลและการปฏิบัติตามข้อกำหนด
- **การค้นหาความสัมพันธ์ของข้อมูลข้ามแผ่นงาน** – ค้นหาหมายเลขโครงการหรือชื่อลูกค้าที่ปรากฏในหลายแผ่นงาน เพื่อให้สามารถบูรณาการข้อมูลข้ามแผ่นงานได้อย่างรวดเร็ว
- **การตรวจสอบเนื้อหาเทมเพลตแบบแบทช์** – หลังจากสร้างรายงานแล้ว ตรวจสอบว่าตัวยึดตำแหน่งทั้งหมด เช่น `{{Date}}` ถูกแทนที่อย่างถูกต้องในไฟล์ Excel หลายไฟล์
- **การเก็บรักษาและขุดข้อมูลประวัติศาสตร์** – ค้นหาโค้ดเหตุการณ์เฉพาะหรือคำศัพท์ทางธุรกิจในไฟล์ Excel รุ่นเก่า เพื่อเร่งกระบวนการวิเคราะห์และค้นหาข้อมูลย้อนหลัง

## เหตุใดจึงควรใช้ API ค้นหาเนื้อหาในสเปรดชีต?

- **เป็นมิตรกับนักพัฒนา** – มี SDK ให้ใช้งานในหลายภาษา ลดความพยายามในการพัฒนาเทียบกับการสร้างโซลูชันแบบกำหนดเอง
- **ลดค่าใช้จ่ายแรงงาน** – ทำให้ภารกิจที่ต้องตรวจสอบสเปรดชีตด้วยตนเองโดยอัตโนมัติ
- **จ่ายตามการใช้งานจริง** – คุณจะจ่ายเฉพาะสำหรับคำขอ API ที่คุณดำเนินการจริงเท่านั้น
- **ไม่มีการบำรุงรักษา** – ไม่ต้องจัดการเซิร์ฟเวอร์ ไม่ต้องอัปเดตซอฟต์แวร์ และไม่มีปัญหาเรื่องความเข้ากันได้
- **รักษาการจัดรูปแบบที่ซับซ้อน** – ผลลัพธ์สามารถส่งออกเป็น PDF ได้โดยรักษารูปแบบ Excel เดิมไว้

## วิธีใช้การค้นหาลิงก์ที่เสียภายใน Spreadsheet API ด้วย SDKs

### **ข้อกำหนด OpenAPI**

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้โดยสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันการค้นหา SDK ทำหน้าที่ซ่อนชั้น HTTP ช่วยให้คุณสามารถเรียกใช้ API ด้วยโค้ดเพียงเล็กน้อย ดูรายชื่อ SDK ทั้งหมดได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้การดำเนินการค้นหาเนื้อหาในสเปรดชีตโดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}