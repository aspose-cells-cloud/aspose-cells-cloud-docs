---
title: "อัปเดตแกนหมวดหมู่ของแผนภูมิ"
type: docs
url: /charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, แผนภูมิ, แกนหมวดหมู่, REST API, Excel, Cloud SDK"
description: "อัปเดตแกนหมวดหมู่ของแผนภูมิในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API"
ArticleTitle: "อัปเดตแกนหมวดหมู่ของแผนภูมิ – Aspose.Cells Cloud API"
---

API นี้อัปเดตแกนหมวดหมู่ของแผนภูมิ

## API PostChartCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **ความปลอดภัยและการพิสูจน์ตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การพิสูจน์ตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | ----------- |
| name           | string  | path     | ชื่อไฟล์ Excel |
| sheetName      | string  | path     | ชื่อแผ่นงานที่มีแผนภูมิ |
| chartIndex     | integer | path     | ดัชนีแบบเริ่มต้นด้วย 0 ของแผนภูมิที่ต้องการอัปเดต |
| axis           | object  | body     | ออบเจกต์ JSON ที่กำหนดคุณสมบัติของแกนหมวดหมู่ |
| folder         | string  | query    | โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่ไฟล์ตั้งอยู่ (ไม่บังคับ) |
| storageName    | string  | query    | ชื่อของพื้นที่จัดเก็บ (ไม่บังคับ) |

**สchemаของเนื้อหาคำขอ – ออบเจกต์ `axis`**

| คุณสมบัติ | ชนิดข้อมูล | คำอธิบาย |
|----------|--------|-------------|
| IsAutomaticMajorUnit | boolean | ระบุว่าหน่วยหลักจะคำนวณอัตโนมัติหรือไม่ |
| MajorUnit | number | ค่าของหน่วยหลักเมื่อ `IsAutomaticMajorUnit` เป็น `false` |
| IsAutomaticMinorUnit | boolean | ระบุว่าหน่วยย่อยจะคำนวณอัตโนมัติหรือไม่ |
| MinorUnit | number | ค่าของหน่วยย่อยเมื่อ `IsAutomaticMinorUnit` เป็น `false` |
| Title | object | การตั้งค่าชื่อเรื่องสำหรับแกน (เช่น `Text`, `Font`, `Visible`) |
| TickLabelPosition | string | ตำแหน่งของฉลากบั้ง (เช่น `Low`, `High`, `NextToAxis`) |
| ... | ... | คุณสมบัติของแกนเพิ่มเติมตามที่กำหนดไว้ในสเปคของ API |

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | เนื้อหาคำขอใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

**ข้อกำหนดเบื้องต้น / การพิสูจน์ตัวตน**

เพื่อเรียกใช้เอนด์พอยต์นี้ คุณต้องได้รับโทเคนการเข้าถึง JWT จากบริการพิสูจน์ตัวตนของ Aspose.Cells Cloud (`/connect/token`) แล้วแนบโทเคนนี้ในส่วนหัว `Authorization` ดังตัวอย่างต่อไปนี้

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Category Axis",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**ตัวอย่างการตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### หมายเหตุ

* เอนด์พอยต์นี้ต้องใช้ HTTPS; การใช้ HTTP อาจทำให้เกิดคำเตือนเกี่ยวกับเนื้อหาแบบผสมในเว็บเบราว์เซอร์
* ต้องแทนค่าตัวแปรแบบ Platzholder (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) ด้วยตัวระบุจริงทั้งหมด
* ประเภทแผนภูมิที่รองรับสำหรับการอัปเดตแกนหมวดหมู่มีรายละเอียดอยู่ในเอกสารอ้างอิงของ API

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา โดย SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}