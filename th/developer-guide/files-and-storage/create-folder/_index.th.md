---
title: "สร้างโฟลเดอร์ – Aspose.Cells Cloud API | การจัดการที่จัดเก็บไฟล์ Excel"
second_title: "เอกสาร"
ArticleTitle: "สร้างโฟลเดอร์ – Aspose.Cells Cloud API"
linktype: "สร้างโฟลเดอร์"
type: docs
url: /th/create-folder/
keywords: "Aspose.Cells, Cloud API, สร้างโฟลเดอร์, การจัดการที่จัดเก็บไฟล์, Excel"
description: "สร้างโฟลเดอร์ใหม่ในที่จัดเก็บไฟล์บนคลาวด์ของ Aspose.Cells ผ่านคำขอ PUT แบบง่าย ดูรูปแบบคำขอ พารามิเตอร์ การตอบกลับ และการจัดการข้อผิดพลาด"
weight: 100
---

การดำเนินการ **createFolder** สร้างโฟลเดอร์ใหม่ในตำแหน่งที่ระบุภายในที่จัดเก็บไฟล์บนคลาวด์ที่ Excel API ใช้งาน การดำเนินการนี้มีความจำเป็นสำหรับการจัดระเบียบไฟล์และรักษาโครงสร้างไดเรกทอรีที่มีระบบ

## **Excel API: สร้างโฟลเดอร์**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอของ API **createFolder** มีดังนี้

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | จำเป็น | ค่าเริ่มต้น | คำอธิบาย                                                                  |
|------------------|--------|----------|----------|-------------|-----------------------------------------------------------------------------|
| `path`           | String | Path     | ใช่      | –           | เส้นทางโฟลเดอร์ที่จะสร้าง (เช่น `myFolder/subFolder`)                       |
| `storageName`    | String | Query    | ไม่จำเป็น | –           | ชื่อที่จัดเก็บไฟล์ที่จะใช้งาน หากไม่ระบุ จะใช้ที่จัดเก็บไฟล์เริ่มต้น         |

### คำอธิบายการตอบกลับ

```json
{}
```

การดำเนินการจะไม่ส่งเนื้อหาใดๆ กลับมาหากสำเร็จ รหัสสถานะ HTTP ที่พบบ่อยมีดังนี้:

**รหัสสถานะ HTTP**

| รหัส HTTP | สถานะ HTTP            | คำอธิบาย                                                                      |
|-----------|-----------------------|--------------------------------------------------------------------------------|
| 200       | OK (สำเร็จ)          | เรียกใช้ Web API สำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ               |
| 400       | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)                 |
| 401       | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย                                                 |
| 413       | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                              |
| 500       | Internal Server Error | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                      |

## ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}