---
title: "ตรวจสอบว่ามีพื้นที่จัดเก็บข้อมูลหรือไม่ – Aspose.Cells Cloud API (v4.0)"
second_title: "เอกสาร"
ArticleTitle: "การจัดการไฟล์ Excel ผ่านระบบคลาวด์ – ตรวจสอบความมีอยู่ของพื้นที่จัดเก็บข้อมูล"
linktitle: "มีพื้นที่จัดเก็บข้อมูลหรือไม่"
type: docs
url: /th/storage-exists/
keywords: "Aspose.Cells, storage exists, cloud storage API, REST, Excel"
description: "ยืนยันความมีอยู่ของคอนเทนเนอร์พื้นที่จัดเก็บข้อมูลใน Aspose.Cells Cloud เรียนรู้เกี่ยวกับ endpoint GET /v4.0/cells/storage/{storageName}/exist พารามิเตอร์ที่จำเป็น รูปแบบการตอบกลับ และตัวอย่าง SDK ในภาษา C#, Java, Python และอื่นๆ"
weight: 100
---

API `storageExists` ใช้ตรวจสอบว่ามีพื้นที่จัดเก็บข้อมูลที่ระบุอยู่ในบริการคลาวด์ของ Aspose.Cells หรือไม่ ฟังก์ชันนี้มีความสำคัญมากในการรับประกันว่าการดำเนินการที่พึ่งพาพื้นที่จัดเก็บข้อมูลจะสามารถดำเนินการได้โดยไม่เกิดข้อผิดพลาด  
**สรุป** – endpoint `storageExists` ช่วยให้คุณยืนยันได้ว่าคอนเทนเนอร์พื้นที่จัดเก็บข้อมูลที่ระบุมีอยู่จริงใน Aspose.Cells Cloud ควรใช้ก่อนดำเนินการเกี่ยวกับไฟล์ เพื่อหลีกเลี่ยงข้อผิดพลาดขณะรันโปรแกรม

## ตรวจสอบความมีอยู่ของพื้นที่จัดเก็บข้อมูล (storageExists)

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์สำหรับคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                     |
| ---------------- | --------- | -------- | --------------------------------------------- |
| storageName      | String    | Path     | ชื่อของพื้นที่จัดเก็บข้อมูลที่ต้องการตรวจสอบความมีอยู่ |

### **การตอบกลับ**

```json
{
  "Name": "StorageExist",
  "Description": ["ระบุว่าพื้นที่จัดเก็บข้อมูลที่ระบุมีอยู่หรือไม่"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "ระบุว่าพื้นที่จัดเก็บข้อมูลมีอยู่หรือไม่",
        "คุณสมบัตินี้จะคืนค่าเป็น true หากพื้นที่จัดเก็บข้อมูลมีอยู่ มิฉะนั้นจะคืนค่าเป็น false"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย            | คำอธิบาย                                                    |
| ---- | -------------------- | ------------------------------------------------------------ |
| 200  | OK                   | ใช้ตัวกรองเรียบร้อยแล้ว การตอบกลับมีรายละเอียดของโอเปอเรชัน |
| 400  | Bad Request          | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)    |
| 401  | Unauthorized         | JWT token ไม่ถูกต้องหรือขาดหาย                               |
| 413  | Payload Too Large    | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                           |
| 500  | Internal Server Error | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด                 |

## วิธีใช้ API ตรวจสอบความมีอยู่ของพื้นที่จัดเก็บข้อมูลด้วย SDK?

### ข้อกำหนด OpenAPI

<a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">ข้อกำหนด OpenAPI</a> กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ ซึ่งช่วยให้นักพัฒนาสามารถโต้ตอบกับ REST API ได้อย่างราบรื่นจากเบราว์เซอร์เว็บ

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในคอมมานด์ไลน์เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดการดำเนินการระดับต่ำ ทำให้นักพัฒนาสามารถมุ่งเน้นไปที่งานในโครงการของตนได้ สำหรับรายชื่อ SDK ของ Aspose.Cells Cloud ที่มีให้ใช้งาน กรุณาเข้าชม <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">ที่เก็บบน GitHub</a>

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียก API กับบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}