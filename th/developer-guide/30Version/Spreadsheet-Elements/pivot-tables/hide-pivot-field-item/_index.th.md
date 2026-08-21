---
title: "ซ่อนรายการฟิลด์พิวต์ในตารางพิวต์"
second_title: "Document"
linktype: Hide
type: docs
url: /pivot-tables/hide-pivot-field-item/
aliases: [/hide-pivot-field-item/]
keywords: "Aspose.Cells, ซ่อนรายการฟิลด์พิวต์, PivotTable API, REST API, cloud SDK"
description: "เรียนรู้วิธีซ่อนรายการฟิลด์พิวต์ในตารางพิวต์โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยรายละเอียดคำขอ ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับหลายภาษา"
weight: 110
ArticleTitle: "ซ่อนรายการฟิลด์พิวต์ในตารางพิวต์ – คู่มือ API ของ Aspose.Cells Cloud"
---

ก่อนเรียกใช้ API คุณจำเป็นต้องมี:

* **โทเคน JWT ที่ใช้งานได้** (ขอรับได้ผ่านกระบวนการยืนยันตัวตนของ Aspose Cloud)  
* สมุดงานเป้าหมายที่อัปโหลดลงในพื้นที่จัดเก็บบน Aspose Cloud ของคุณแล้ว  
* ชีตงานและตารางพิวต์ถูกสร้างไว้แล้ว

ข้อกำหนดเบื้องต้นเหล่านี้ช่วยป้องกันข้อผิดพลาดในการยืนยันตัวตนและข้อผิดพลาด "ไม่พบทรัพยากร" ขั้นตอนต่อไปนี้อธิบายการตั้งค่าที่จำเป็นก่อนเรียกใช้ API

API นี้ของ REST API ใช้สำหรับซ่อนรายการฟิลด์พิวต์ในตารางพิวต์

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและจำเป็นต้องมีการยืนยันตัวตนแบบใช้โทเคน <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                      |
| --------------- | -------- | ------- | ---------------------------------------------------------------------------------------------- |
| name            | string   | path    | ชื่อไฟล์ Excel                                                                                 |
| sheetName       | string   | path    | ชีตงานที่มีตารางพิวต์                                                                          |
| pivotTableIndex | integer  | path    | ดัชนีของตารางพิวต์ภายในชีตงาน                                                                 |
| pivotFieldType  | string   | query   | ประเภทของฟิลด์พิวต์ (Row, Column, Page, Data เป็นต้น)                                         |
| fieldIndex      | integer  | query   | ดัชนีแบบเริ่มต้นที่ 0 ของฟิลด์พิวต์ที่ต้องการแก้ไข                                            |
| itemIndex       | integer  | query   | ดัชนีของรายการเฉพาะภายในฟิลด์ที่ต้องการซ่อน                                                  |
| isHide          | boolean  | query   | ตั้งค่าเป็น **true** เพื่อซ่อนรายการ หรือ **false** เพื่อแสดงรายการ                           |
| needReCalculate | boolean  | query   | ระบุว่าควรคำนวณตารางพิวต์ใหม่หลังการเปลี่ยนแปลงหรือไม่ ค่าเริ่มต้นคือ **false**              |
| folder          | string   | query   | เส้นทางโฟลเดอร์ที่เก็บสมุดงาน                                                                  |
| storageName     | string   | query   | ชื่อของบริการจัดเก็บข้อมูล                                                                      |

**สรุปพารามิเตอร์ที่จำเป็นสำหรับ query**

- **pivotFieldType** – ประเภทของฟิลด์ (เช่น `Row`)  
- **fieldIndex** – ดัชนีแบบเริ่มต้นที่ 0 ของฟิลด์ที่ต้องการแก้ไข  
- **itemIndex** – ดัชนีแบบเริ่มต้นที่ 0 ของรายการที่ต้องการซ่อน/แสดง  
- **isHide** – `true` เพื่อซ่อน, `false` เพื่อแสดง  
- **needReCalculate** – ไม่บังคับ ค่าเริ่มต้นคือ `false`

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะและอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีการเรียกใช้ API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
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

**รายละเอียดของคำตอบ**

| สถานะโค้ด | คำอธิบาย                                                           |
| --------- | ------------------------------------------------------------------ |
| 200       | ซ่อนรายการเรียบร้อยแล้ว                                          |
| 400       | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง               |
| 401       | ไม่ได้รับอนุญาต – โทเคน JWT ไม่ถูกต้องหรือขาดหาย               |
| 500       | ข้อผิดพลาดของเซิร์ฟเวอร์ – การดำเนินการไม่สามารถเสร็จสิ้นได้    |

**หมายเหตุ:** หาก `fieldIndex` หรือ `itemIndex` ที่ระบุเกินขอบเขตที่กำหนด API จะส่งคำตอบ **400 Bad Request**

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาบน API SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจของคุณได้ ดู [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการซ่อนรายการฟิลด์พิวต์โดยใช้ SDK ต่างๆ

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // เตรียมสมุดงานและชีตงาน
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // อัปโหลดสมุดงาน
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // สร้างชีตงานที่จะมีตารางพิวต์
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // สร้างชีตงานที่สองพร้อมข้อมูลตัวอย่าง
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // นำเข้าข้อมูลตัวอย่างลงใน Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // ตัดทอนเพื่ออ่านง่าย
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // เพิ่มตารางพิวต์ลงใน PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // ซ่อนรายการฟิลด์แถวที่ระบุ
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**หมายเหตุ:** ตัวอย่าง SDK เหล่านี้สมมติว่าคุณได้ตั้งค่าการยืนยันตัวตน (โทเคน JWT) เรียบร้อยแล้ว และสมุดงานอยู่ในโฟลเดอร์ที่ระบุของพื้นที่จัดเก็บ ปรับค่าพารามิเตอร์ `folder` และ `storageName` ตามสภาพแวดล้อมของคุณ
---