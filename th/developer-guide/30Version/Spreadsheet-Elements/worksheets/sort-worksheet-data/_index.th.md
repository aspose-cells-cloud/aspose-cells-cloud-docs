---
title: "จัดเรียงข้อมูลในช่วงของสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "จัดเรียง"
type: docs
url: /worksheets/sort-data/
aliases: [/sort-worksheet-data/]
keywords: "Aspose.Cells Cloud, API สำหรับการเรียงลำดับ Excel, การเรียงลำดับช่วงของworksheet, REST API, dataSorter"
description: "จัดเรียงช่วงที่กำหนดในสมุดงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ซึ่งรวมถึง endpoint, พารามิเตอร์ที่จำเป็น, ขั้นตอนการยืนยันตัวตน, การจัดการข้อผิดพลาด และตัวอย่าง SDK"
weight: 20
---

API REST นี้จัดเรียงข้อมูลภายในช่วงที่ระบุในสมุดงาน Excel

## API REST

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | จำเป็น | คำอธิบาย                                                                   |
| ---------------- | -------- | ------- | ------ | -------------------------------------------------------------------------- |
| name             | string   | path    | ใช่    | ชื่อสมุดงาน                                                               |
| sheetName        | string   | path    | ใช่    | ชื่อworksheet                                                              |
| cellArea         | string   | query   | ใช่    | ช่วงของเซลล์ที่ต้องการจัดเรียง (เช่น `A5:A10`)                             |
| dataSorter       | object   | body    | ใช่    | วัตถุ JSON ที่กำหนดการตั้งค่าการจัดเรียง (ดูโครงสร้างด้านล่าง)            |
| folder           | string   | query   | ไม่บังคับ | โฟลเดอร์ที่เก็บสมุดงานไว้                                                 |
| storageName      | string   | query   | ไม่บังคับ | ชื่อพื้นที่จัดเก็บที่สมุดงานนั้นอยู่                                     |

**โครงสร้างวัตถุ `dataSorter`** – เนื้อหาของ body ต้องมีวัตถุ JSON ที่ประกอบด้วยคุณสมบัติต่อไปนี้:

- `CaseSensitive` _(boolean, จำเป็น)_ – ระบุว่าการจัดเรียงนั้นคำนึงถึงตัวพิมพ์เล็ก/ใหญ่หรือไม่
- `HasHeaders` _(boolean, จำเป็น)_ – ระบุว่าช่วงนี้มีแถวหัวข้อหรือไม่
- `KeyList` _(array, จำเป็น)_ – คอลเลกชันของคีย์การจัดเรียง โดยแต่ละคีย์จะประกอบด้วย:
  - `Key` _(integer)_ – ดัชนีของคอลัมน์แบบเริ่มต้นที่ 0
  - `SortOrder` _(string)_ – `"ascending"` หรือ `"descending"`
- `SortLeftToRight` _(boolean, จำเป็น)_ – หากเป็น `true` การจัดเรียงจะทำจากซ้ายไปขวา มิฉะนั้นจะจัดเรียงจากบนลงล่าง
- อาจมีคุณสมบัติเพิ่มเติมเช่น `CaseOrder`, `SortLeftToRight` ตามที่ระบุไว้ใน OpenAPI Specification

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) กำหนดอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้สาธารณะ และอนุญาตให้คุณดำเนินการ REST interaction โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
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

**การจัดการข้อผิดพลาด** – API อาจส่งกลับรหัสข้อผิดพลาด HTTP มาตรฐาน ซึ่งการตอบกลับทั่วไปมีดังนี้:

| HTTP Status | รหัส | ข้อความ                                                                         |
| ----------- | ---- | ------------------------------------------------------------------------------ |
| 400         | 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง                              |
| 401         | 401  | ไม่ได้รับอนุญาต – JWT token ไม่ถูกต้องหรือไม่มี                               |
| 404         | 404  | ไม่พบ – สมุดงานหรือworksheet ไม่มีอยู่                                         |
| 500         | 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์                                                     |

สำหรับกรณีข้อผิดพลาด เนื้อหาการตอบกลับจะอยู่ในรูปแบบ `{ "Code": <status>, "Message": "<คำอธิบาย>", "Status": "Error" }`

## กลุ่ม SDK สำหรับ Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้ ทำให้คุณสามารถมุ่งเน้นไปที่งานหลักของโปรเจกต์ได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}