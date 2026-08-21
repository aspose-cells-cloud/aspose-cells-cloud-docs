---
title: "ย้ายตารางพิวต์ในไฟล์ Excel"
second_title: "เอกสาร"
linktitle: ย้าย
type: docs
url: /th/pivot-tables/move/
aliases: [  /th/move-pivot-table/ ]
keywords: "Aspose.Cells Cloud, ย้ายตารางพิวต์, Excel, REST API, SDK, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "เรียนรู้วิธีใช้ Aspose.Cells Cloud REST API ในการย้ายตารางพิวต์ภายในสมุดงาน Excel SDK มีให้ใช้งานสำหรับ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
weight: 120
---

REST API นี้ใช้ย้ายตารางพิวต์ภายในสมุดงาน Excel

**ข้อกำหนดเบื้องต้น:** ก่อนเรียกใช้การดำเนินการนี้ คุณต้องมีโทเค็น JWT ที่ถูกต้อง และสมุดงานต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud ระบุพารามิเตอร์ `folder` และ `storageName` ตามความจำเป็น

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Move
```

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                 |
| ---------------- | ------- | -------- | --------------------------------------------------------- |
| name             | string  | path     | ชื่อไฟล์ Excel                                            |
| sheetName        | string  | path     | ชื่อแผ่นงานที่มีตารางพิวต์                               |
| pivotTableIndex  | integer | path     | ดัชนีของตารางพิวต์ที่ต้องการย้าย (เริ่มต้นที่ 0)         |
| fieldIndex       | integer | query    | ดัชนีของฟิลด์ตารางพิวต์ที่ต้องการย้าย                   |
| from             | string  | query    | พื้นที่ต้นทางของฟิลด์ (เช่น `Row` หรือ `Column`)         |
| to               | string  | query    | พื้นที่ปลายทางของฟิลด์ (เช่น `Row` หรือ `Column`)        |
| folder           | string  | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่                   |
| storageName      | string  | query    | ชื่อของบริการพื้นที่จัดเก็บ                              |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldMoveTo) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Move?fieldIndex=0&from=C1&to=C10" \
  -X POST \
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

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ใช้ HTTPS endpoints ในระบบจริง
public void Run_PivotTable_Move()
{
    url = @"https://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null}, ... ],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/Move?row=10&column=10&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Move?fieldIndex=1&from=Row&to=Column&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "60360c7d035abd1b2c9e36c68c9f00fb" >}}

{{< /tab >}}

{{< /tabs >}}