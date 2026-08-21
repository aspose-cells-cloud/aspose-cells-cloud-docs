---
title: "เรียงข้อมูล ListObject ในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "เรียงลำดับ"
type: docs
url: /th/list-objects/sort-data/
aliases: [/th/get-a-list-object-or-table-inside-the-worksheet/, /th/tables/sort-data/]
keywords: "Aspose.Cells Cloud, Excel, ListObject, เรียงข้อมูล, REST API, แผ่นงาน"
description: "เรียนรู้วิธีเรียงข้อมูล ListObject (ตาราง) ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ซึ่งประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่างคำสั่ง cURL และตัวอย่าง SDK"
weight: 40
ArticleTitle: "เรียงข้อมูล ListObject ในแผ่นงาน Excel – API Aspose.Cells Cloud"
---

**ข้อกำหนดเบื้องต้น**  
เพื่อเรียกใช้ API นี้ คุณต้องมีโทเคน JWT สำหรับการเข้าถึง Aspose Cloud ที่ถูกต้อง และไฟล์สมุดงานต้องถูกอัปโหลดไปยังที่จัดเก็บของ Aspose Cloud แล้ว ให้ใส่ header `Authorization: Bearer <jwt token>` ในทุกคำขอ

API REST นี้จะเรียงข้อมูลของตารางในแผ่นงาน Excel  
เพื่อใช้งานฟังก์ชันนี้ คุณต้องระบุชื่อไฟล์สมุดงาน ชื่อแผ่นงาน และดัชนีของ ListObject ที่ต้องการเรียง รวมทั้งส่ง JSON body ที่ชื่อ `dataSorter` ซึ่งกำหนดเงื่อนไขการเรียงลำดับ

## API PostWorksheetListObjectSortTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วยโทเคน JWT</a>

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง (Path/Query String/HTTPBody) | คำอธิบาย |
|------------------|-------------|----------------------------------------|-----------|
| name             | string      | path                                   | ชื่อไฟล์ Excel ที่จัดเก็บไว้ในที่จัดเก็บของ Aspose Cloud |
| sheetName        | string      | path                                   | ชื่อของแผ่นงานที่มี ListObject อยู่ |
| listObjectIndex  | integer     | path                                   | ดัชนีแบบเริ่มต้นที่ 0 ของ ListObject (ตาราง) ภายในแผ่นงาน |
| dataSorter       | object      | body                                   | วัตถุ JSON ที่ระบุตัวเลือกการเรียงลำดับ (เช่น `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`) |
| folder           | string      | query                                  | เส้นทางโฟลเดอร์ในที่จัดเก็บที่ไฟล์ Excel อยู่ |
| storageName      | string      | query                                  | ชื่อของที่จัดเก็บ Aspose Cloud |

**หมายเหตุ**  
เนื้อหาของคำขอนั้นต้องเป็นวัตถุ JSON ที่ถูกต้องและสอดคล้องกับโครงสร้างของ `dataSorter` โปรดตรวจสอบให้แน่ใจว่าไฟล์สมุดงาน แผ่นงาน และ ListObject มีอยู่จริงก่อนที่จะเรียกใช้ฟังก์ชันการเรียงลำดับ

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**โค้ดสถานะ HTTP**

| โค้ดสถานะ | คำอธิบาย |
|-----------|----------|
| 200       | สำเร็จ – การเรียงลำดับเสร็จสมบูรณ์ |
| 400       | คำขอไม่ถูกต้อง – พารามิเตอร์ผิดพลาด |
| 401       | ไม่ได้รับอนุญาต – การพิสูจน์ตัวตนล้มเหลว |
| 404       | ไม่พบ – ไม่พบไฟล์สมุดงาน แผ่นงาน หรือ ListObject |
| 500       | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – ปัญหาฝั่งเซิร์ฟเวอร์ |

**พารามิเตอร์ของการตอบกลับ**

| พารามิเตอร์ | ประเภทข้อมูล | คำอธิบาย |
|-------------|-------------|----------|
| Code        | integer     | โค้ดสถานะ HTTP ที่ส่งคืนโดย API |
| Status      | string      | คำอธิบายเชิงข้อความของผลลัพธ์ (เช่น "OK") |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และอนุญาตให้คุณมุ่งเน้นไปที่งานของโครงการ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[กลับไปยังภาพรวม ListObjects](/th/list-objects/)