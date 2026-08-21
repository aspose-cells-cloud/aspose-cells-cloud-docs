---
title: "Aspose.Cells Cloud API – รับข้อมูลการใช้พื้นที่จัดเก็บ | ข้อมูลเชิงวัดผลการจัดเก็บแบบเรียลไทม์"
second_title: "เอกสาร"
ArticleTitle: "โซลูชันจัดการไฟล์ Excel บนคลาวด์ – อินเทอร์เฟซสำหรับดึงข้อมูลการใช้พื้นที่จัดเก็บบนคลาวด์อย่างรวดเร็ว"
linktype: "รับข้อมูลการใช้พื้นที่จัดเก็บ"
type: docs
url: /th/get-disk-usage/
keywords: "Aspose Cells, Cloud API, การใช้พื้นที่จัดเก็บ, ข้อมูลเชิงวัดผลการจัดเก็บ, Excel, REST"
description: "รับข้อมูลการใช้พื้นที่จัดเก็บแบบเรียลไทม์สำหรับ Aspose.Cells Cloud เรียนรู้เกี่ยวกับ endpoint GET /v4.0/cells/storage/disk การยืนยันตัวตนที่จำเป็น และตัวอย่างการตอบกลับ"
weight: 100
---

การดำเนินการ **รับข้อมูลการใช้พื้นที่จัดเก็บ** จะส่งคืนข้อมูลเชิงวัดผลการจัดเก็บแบบเรียลไทม์สำหรับบัญชี Aspose.Cells Cloud ของคุณ ใช้ endpoint นี้เพื่อตรวจสอบปริมาณพื้นที่จัดเก็บที่ใช้ไปและพื้นที่จัดเก็บทั้งหมด

- ดึงข้อมูลการใช้พื้นที่จัดเก็บปัจจุบันสำหรับ Excel API ในสภาพแวดล้อม Aspose Cloud
- ช่วยให้นักพัฒนาสามารถตรวจสอบปริมาณพื้นที่จัดเก็บที่แอปพลิเคชันของตนใช้ไป
- ทำให้สามารถจัดการขีดจำกัดการจัดเก็บและควบคุมต้นทุนได้อย่างมีประสิทธิภาพ

## Excel API: GetDiskUsage

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                         | จำเป็น |
| -------------- | ------ | -------- | ---------------------------------------------------- | -------- |
| storageName    | String | Query    | ชื่อของพื้นที่จัดเก็บที่ต้องการรับข้อมูลการใช้งาน | ไม่บังคับ |

### **การตอบกลับ**

```json
{
  "Name": "DiskUsage",
  "Description": ["คลาสสำหรับข้อมูลพื้นที่จัดเก็บ"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["ปริมาณพื้นที่จัดเก็บที่แอปพลิเคชันใช้ไป"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["ปริมาณพื้นที่จัดเก็บทั้งหมดที่มีอยู่"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                | คำอธิบาย                                                           |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)          |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                      |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                           |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                             |

## ข้อมูลจำเพาะ OpenAPI

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) กำหนดอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่รันผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}

---