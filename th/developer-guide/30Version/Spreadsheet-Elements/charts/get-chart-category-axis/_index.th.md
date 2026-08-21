---
title: "รับแกนหมวดหมู่ของแผนภูมิ"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, แกนหมวดหมู่ของแผนภูมิ, Excel, REST API, Cloud Storage, OAuth2, เอกสาร API"
description: "ดึงข้อมูลแกนหมวดหมู่ของแผนภูมิในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API"
ArticleTitle: "รับแกนหมวดหมู่ของแผนภูมิ – เอกสาร API Aspose.Cells Cloud"
---

REST API นี้จะดึงข้อมูล **แกนหมวดหมู่ (Category Axis)** ของแผนภูมิ  
ในการเรียก endpoint นี้ คุณต้องมีโทเคนการเข้าถึง OAuth 2.0 ที่ถูกต้อง และไฟล์สมุดงานต้องถูกเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud

**ข้อกำหนดเบื้องต้น**  
ก่อนใช้งาน endpoint นี้ ให้ตรวจสอบให้แน่ใจว่า:  

- ได้รับโทเคน OAuth 2.0 และโทเคนนั้นยังคงใช้งานได้กับบริการของ Aspose Cloud  
- ไฟล์สมุดงานถูกอัปโหลดไว้ในพื้นที่จัดเก็บของ Aspose Cloud (ค่าเริ่มต้นหรือโฟลเดอร์ที่ระบุ)  
- ใช้เวอร์ชัน API **v3.0** ดังที่แสดงใน URL คำขอ  
- แอปพลิเคชันที่เรียกใช้งานมีสิทธิ์ในการอ่านสมุดงานและเข้าถึงแผ่นงานต่างๆ ของสมุดงานนั้น

## API GetChartCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**บริบท** – การลบแผนภูมิทั้งหมดออกจากแผ่นงานมีประโยชน์เมื่อคุณต้องการรีเซ็ตเค้าโครงเชิงภาพของแผ่นงาน แทนที่การนำเสนอข้อมูลที่ล้าสมัย หรือเตรียมสมุดงานให้พร้อมใช้งานอีกครั้งโดยไม่ต้องเก็บข้อมูลแผนภูมิเดิมไว้

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | ------------------------------------------------------ |
| name           | string  | path     | ชื่อไฟล์สมุดงาน |
| sheetName      | string  | path     | ชื่อแผ่นงานที่มีแผนภูมิ |
| chartIndex     | integer | path     | ดัชนีของแผนภูมิที่ต้องการแกน (เริ่มต้นที่ 0) |
| folder         | string  | query    | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานอยู่ |
| storageName    | string  | query    | ชื่อของบริการจัดเก็บข้อมูล (ถ้าไม่ใช่ค่าเริ่มต้น) |

### **การตอบกลับ**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของOPERATION |
| 400  | Bad Request                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ชนิดไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized                | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

## วิธีใช้ API GetChartCategoryAxis ร่วมกับ SDK

### ข้อมูลจำเพาะ API GetChartCategoryAxis

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">ข้อมูลจำเพาะ OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่มีทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
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