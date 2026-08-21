---
title: "เพิ่มตารางสรุปในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: เพิ่ม
type: docs
url: /th/pivot-tables/add/
aliases: [  /th/add-a-pivot-table-in-a-worksheet/ ]
keywords: "เพิ่มตารางสรุป, แผ่นงาน Excel, Aspose.Cells Cloud, REST API, SDK, ตารางสรุป Excel"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อเพิ่มตารางสรุปในแผ่นงาน Excel โดยรองรับผ่าน SDK สำหรับ C#, Java, PHP, Python, Node.js, Android, Swift, Perl, Go"
weight: 30
ArticleTitle: "วิธีเพิ่มตารางสรุปในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud"
---

REST API นี้จะเพิ่มตารางสรุปลงในแผ่นงาน

**ข้อกำหนดเบื้องต้น:**
- บัญชี Aspose.Cells Cloud ที่มีโทเค็น JWT สำหรับการเข้าถึงที่ถูกต้อง
- สมุดงานเป้าหมายต้องถูกจัดเก็บไว้ในตำแหน่งที่จัดเก็บที่รองรับ (ค่าเริ่มต้นคือการจัดเก็บเริ่มต้นหรือการจัดเก็บที่ผู้ใช้ระบุ)
- แผ่นงานที่ระบุไว้ด้วย `sheetName` ต้องมีอยู่ในสมุดงาน

## API PutWorksheetPivotTable

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                                                                         |
| ---------------- | -------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| name             | string   | path     | ชื่อของเอกสาร Excel                                                                                                                |
| sheetName        | string   | path     | ชื่อของแผ่นงานที่จะสร้างตารางสรุป                                                                                                 |
| request          | object   | body     | DTO `CreatePivotTableRequest` ที่มีนิยามของตารางสรุป                                                                              |
| folder           | string   | query    | โฟลเดอร์ที่มีเอกสาร                                                                                                                 |
| storageName      | string   | query    | ชื่อของพื้นที่จัดเก็บที่มีเอกสาร                                                                                                    |
| sourceData       | string   | query    | ช่วงของข้อมูลต้นทางสำหรับแคชตารางสรุปใหม่ (เช่น `A5:E10`)                                                                         |
| destCellName     | string   | query    | ที่อยู่ของเซลล์บนซ้ายของช่วงปลายทางสำหรับรายงานตารางสรุป                                                                         |
| tableName        | string   | query    | ชื่อที่กำหนดให้กับตารางสรุปใหม่                                                                                                   |
| useSameSource    | boolean  | query    | เมื่อตั้งค่าเป็น `true` ตารางสรุปใหม่จะใช้แหล่งข้อมูลเดียวกับตารางที่มีอยู่ ซึ่งช่วยประหยัดหน่วยความจำหากมีตารางสรุปอื่นใช้แหล่งข้อมูลนี้แล้ว |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

**หมายเหตุด้านความปลอดภัย:** ควรใช้ `https://` เสมอเมื่อเรียกใช้ API และรักษาความลับของโทเค็น JWT ของคุณไว้ การส่งโทเค็นผ่าน HTTP แบบไม่เข้ารหัสอาจทำให้โทเค็นถูกดักจับได้

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองสำเร็จ; คำตอบมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จัดการรายละเอียดระดับต่ำ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

สำหรับการดำเนินการอื่นๆ เพิ่มเติม โปรดดูที่หน้า API ที่เกี่ยวข้อง: **[รับตารางสรุป](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[ลบตารางสรุป](https://docs.aspose.cloud/cells/pivot-tables/delete/)** และ **[อัปเดตตารางสรุป](https://docs.aspose.cloud/cells/pivot-tables/update/)**