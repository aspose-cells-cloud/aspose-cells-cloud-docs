---
title: "อัปเดตแกนหมวดหมู่ที่สองของแผนภูมิ"
type: docs
url: /th/charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart, Second Category Axis, REST API, Update Chart, Excel, Cloud API"
description: "เรียนรู้วิธีอัปเดตแกนหมวดหมู่ที่สองของแผนภูมิในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API"
ArticleTitle: "อัปเดตแกนหมวดหมู่ที่สองของแผนภูมิ – Aspose.Cells Cloud API"
---

API นี้อัปเดตแกนหมวดหมู่ที่สองของแผนภูมิ

## API PostChartSecondCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| พารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | คำอธิบาย |
|-------------|-------------|----------|----------|
| name | string | path | ชื่อไฟล์ Excel |
| sheetName | string | path | ชื่อแผ่นงานที่มีแผนภูมิ |
| chartIndex | integer | path | ดัชนีแบบเริ่มต้นที่ 0 ของแผนภูมิที่ต้องการอัปเดต |
| axis | object | body | ออบเจกต์แกนหมวดหมู่ที่สองที่มีการตั้งค่าใหม่ |
| folder | string | query | เส้นทางโฟลเดอร์ที่จัดเก็บไฟล์ไว้ |
| storageName | string | query | ชื่อของบริการจัดเก็บข้อมูล |

**การยืนยันตัวตน** – API นี้ต้องมีโทเคนการเข้าถึง OAuth 2.0 ที่ถูกต้อง สร้าง JWT token โดยทำตาม[คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/cells/authentication/) แล้วใส่โทเคนนี้ใน header `Authorization` ดังตัวอย่าง cURL ด้านล่าง

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* การตั้งค่าแกน เช่น "Title": "New Axis Title", "IsVisible": true */
        }
      }'
```

*แทนที่ `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, และ `{storageName}` ด้วยค่าจริงของคุณ โดยเนื้อหาคำขอต้องมีออบเจกต์ `axis` ที่มีการตั้งค่าที่ต้องการ*

{{< /tab >}}

{{< tab tabNum="2" >}}

**การตอบกลับที่สำเร็จ (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "New Axis Title",
      "IsVisible": true,
      /* คุณสมบัติแกนเพิ่มเติม */
    }
  }
}
```

**การตอบกลับกรณีเกิดข้อผิดพลาด**  

| สถานะโค้ด | คำอธิบาย |
|-----------|----------|
| 400 | คำขอไม่ถูกต้อง – พารามิเตอร์หายไปหรือไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต – JWT token ไม่ถูกต้องหรือหายไป |
| 404 | ไม่พบ – ไฟล์ แผ่นงาน หรือแผนภูมิที่ระบุไม่มีอยู่จริง |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เกิดสิ่งผิดปกติบนเซิร์ฟเวอร์ |

```json
{
  "Code": 400,
  "Message": "Invalid request payload."
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

SDK ช่วยลดความซับซ้อนของการพัฒนา โดยจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ โปรดดู[ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}

**หมายเหตุและแนวทางปฏิบัติที่ดี**

* พารามิเตอร์ `chartIndex` ใช้ดัชนีแบบเริ่มต้นที่ 0 โดยแผนภูมิแรกในแผ่นงานจะมีดัชนีเป็น 0  
* API นี้รองรับทั้งรูปแบบสมุดงาน `.xlsx` และ `.xls`  
* ใส่เฉพาะคุณสมบัติที่คุณต้องการในออบเจกต์ `axis` เท่านั้น คุณสมบัติที่ไม่ได้ระบุจะยังคงใช้ค่าเดิมอยู่  
* ปฏิบัติตามข้อจำกัดอัตราการเรียกใช้งาน (โดยทั่วไปคือ 100 คำขอต่อนาทีต่อบัญชี) เพื่อหลีกเลี่ยงการถูกจำกัดการใช้งาน
---