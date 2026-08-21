---
---
title: "Aspose.Cells Cloud Web API – การรวมและนับค่าตามสีใน Excel"
second_title: "เอกสาร"
ArticleTitle: "รวม นับ ค่าเฉลี่ย ค่าสูงสุด ค่าต่ำสุด ตามสีในสเปรดชีต/Excel"
LinkTitle: "รวมเซลล์ตามสี"
type: docs
url: /aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregate, color, sum, count, average, min, max"
description: "รวมเซลล์ Excel ตามสีพื้นหลังหรือสีตัวอักษร (รวม นับ ค่าเฉลี่ย ค่าต่ำสุด ค่าสูงสุด) โดยใช้ Aspose.Cells Cloud API เรียนรู้เกี่ยวกับ endpoint พารามิเตอร์ การตรวจสอบสิทธิ์ และตัวอย่าง SDK"
weight: 100
---

## ภาพรวม

API สามารถดำเนินการคำนวณข้อมูลตาม **สี** ของเซลล์ ซึ่งสามารถรวม นับ คำนวณค่าเฉลี่ย และหาค่าสูงสุดและต่ำสุดในสเปรดชีต Excel ตามสีเติมหรือสีตัวอักษรของเซลล์

| ปฏิบัติการคำนวณ | คำอธิบาย                                                     |
| :---------------- | :----------------------------------------------------------- |
| นับ (Count)       | ระบุจำนวนเซลล์ที่มีสีเดียวกัน                              |
| รวม (Sum)         | คำนวณค่ารวมของเซลล์ที่มีสีเดียวกัน                         |
| ค่าสูงสุด (Max Value) | ระบุค่าสูงสุดระหว่างเซลล์ที่มีสีเดียวกัน                   |
| ค่าต่ำสุด (Min Value) | ค้นหาค่าต่ำสุดระหว่างเซลล์ที่มีสีเดียวกัน                  |
| ค่าเฉลี่ย (Average Value) | คำนวณค่าเฉลี่ยของเซลล์ที่มีสีเดียวกัน                      |

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบ JWT token</a>

### พารามิเตอร์สำหรับคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                       |
| :------------- | :----- | :------- | :--------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | FormData | สมุดงาน Excel ที่ต้องประมวลผล                                  |
| Worksheet      | สตริง | Query    | ชื่อแผ่นงานที่มีช่วงข้อมูล                                      |
| Range          | สตริง | Query    | ช่วงในรูปแบบ A‑1 (เช่น `A1:B10`)                               |
| Operation      | สตริง | Query    | วิธีการคำนวณ – `Sum`, `Count`, `Average`, `Min`, หรือ `Max`   |
| ColorPosition  | สตริง | Query    | ระบุสีที่ต้องการประเมิน – `Background`, `Font`                 |
| Region         | สตริง | Query    | การตั้งค่าภูมิภาคของสเปรดชีต (เช่น `us-east-1`)                |
| Password       | สตริง | Query    | รหัสผ่านสำหรับเปิดสมุดงานที่ได้รับการป้องกัน (ไม่บังคับ)         |

#### ค่าที่กำหนดไว้ล่วงหน้า (Enumerations)

- **ColorPosition**

  | ค่า         | ความหมาย                      |
  | :--------- | :-------------------------- |
  | Background | ใช้สีเติมของเซลล์            |
  | Font       | ใช้สีตัวอักษรของเซลล์        |

**ตัวอย่างคำขอ multipart/form‑data**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### การตอบกลับ

โครงสร้างด้านล่างอธิบายวัตถุการตอบกลับ มีตัวอย่างที่เป็นจริงตามด้วยโครงสร้างนี้

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**ตัวอย่างการตอบกลับ (ค่าจริง)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย               | คำอธิบาย                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)                    | ใช้ตัวกรองสำเร็จ การตอบกลับมีรายละเอียดการดำเนินการ         |
| 400  | คำขอไม่ถูกต้อง (Bad Request)           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)      |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)          | JWT token ไม่ถูกต้องหรือขาดหาย                                  |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large)     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                             |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                       |

## ควรใช้ Aggregate by Color API ที่ไหน?

ในสเปรดชีต ข้อมูลจากหมวดหมู่ต่างๆ มักจะถูกเขียนโค้ดด้วยสี เพื่อให้สามารถแยกแยะได้ง่าย API นี้ช่วยให้คุณรวม นับ คำนวณค่าเฉลี่ย หรือหาค่าต่ำสุดและสูงสุดสำหรับแต่ละกลุ่มสี ทำให้การวิเคราะห์ข้อมูลตามสีง่ายขึ้น

## เหตุใดจึงควรใช้ Aggregate by Color API?

API นี้ให้วิธีที่รวดเร็วและเชื่อถือได้ในการดำเนินการคำนวณตามสีโดยไม่จำเป็นต้องเขียนตรรกะการแยกวิเคราะห์แบบกำหนดเอง ผสานรวมเข้ากับ Aspose.Cells Cloud SDKs ได้อย่างลงตัว ทำให้นักพัฒนาสามารถใช้การรวมข้อมูลตามสีได้เพียงไม่กี่บรรทัดของโค้ด

## วิธีใช้ Aggregate by Color API ร่วมกับ SDKs

### ข้อกำหนด Aggregate by Color API

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">ข้อกำหนด Aggregate by Color API</a> กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถรวมการคำนวณตามสีของเซลล์ได้ด้วยโค้ดเพียงไม่กี่บรรทัด  
โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**หมายเหตุ:**

- เมื่อทำงานกับสมุดงานที่ได้รับการป้องกัน ให้รวมพารามิเตอร์ `Password` แบบไม่บังคับใน query parameter มิฉะนั้นคำขอจะล้มเหลวด้วยรหัสข้อผิดพลาด 401
- ขนาดสูงสุดของคำขอสำหรับไฟล์ `Spreadsheet` คือ 100 MB หากคุณต้องการประมวลผลไฟล์ที่มีขนาดใหญ่กว่านี้ ให้พิจารณาอัปโหลดสมุดงานไปยังพื้นที่จัดเก็บของ Aspose Cloud ก่อน และอ้างอิงโดยใช้พารามิเตอร์ `Path` (ซึ่งไม่ได้แสดงไว้ที่นี่)