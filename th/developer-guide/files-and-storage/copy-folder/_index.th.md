---
title: "API สำเนาโฟลเดอร์ของ Aspose.Cells Cloud – การสำเนาโฟลเดอร์อย่างรวดเร็วในคลาวด์"
second_title: "เอกสาร"
ArticleTitle: "โซลูชันการจัดการไฟล์ Excel บนคลาวด์ – คำอธิบายโดยละเอียดเกี่ยวกับฟังก์ชันการสำเนาแบบแบตช์ของ API Aspose.Cells Copy Folder"
linktype: "docs"
url: /th/copy-folder/
keywords: "สำเนาโฟลเดอร์, Aspose.Cells Cloud, REST API, การจัดเก็บข้อมูลบนคลาวด์, การจัดการสเปรดชีต"
description: "เรียนรู้วิธีการสำเนาโฟลเดอร์ในพื้นที่จัดเก็บข้อมูลของ Aspose.Cells Cloud ด้วยคำขอ REST ครั้งเดียว รวมถึง endpoint, พารามิเตอร์, ตัวอย่างคำขอ, รหัสข้อผิดพลาด และตัวอย่าง SDK"
weight: 100
---

**CopyFolder** API คัดลอกโฟลเดอร์ที่มีอยู่ภายในพื้นที่จัดเก็บข้อมูลของ Aspose.Cells Cloud ซึ่งมีประโยชน์ในการสร้างสำเนาสำรอง จัดระเบียบข้อมูลใหม่ หรือเตรียมโครงสร้างโฟลเดอร์สำหรับการประมวลผลเพิ่มเติมโดยไม่ต้องย้ายไฟล์ด้วยตนเอง

## **API สำหรับ Excel: สำเนาโฟลเดอร์**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์ที่ API CopyFolder รับ

| ชื่อพารามิเตอร์ | จำเป็น | ประเภท | ตำแหน่ง (Path/Query) | คำอธิบาย |
| ----------------- | -------- | ------ | --------------------- | ---------------------------------------------------------------------- |
| `srcPath`         | ใช่      | สตริง | Path                  | เส้นทางของโฟลเดอร์ต้นทางที่จะคัดลอก |
| `destPath`        | ใช่      | สตริง | Query                 | เส้นทางที่จะสร้างโฟลเดอร์ใหม่ |
| `srcStorageName`  | ไม่จำเป็น | สตริง | Query                 | ชื่อของพื้นที่จัดเก็บข้อมูลที่มีโฟลเดอร์ต้นทาง |
| `destStorageName` | ไม่จำเป็น | สตริง | Query                 | ชื่อของพื้นที่จัดเก็บข้อมูลปลายทางที่จะคัดลอกโฟลเดอร์ไป |

### ตัวอย่างการตอบกลับ

การเรียกที่สำเร็จจะส่งกลับ **HTTP 200** พร้อมกับเนื้อหา JSON ว่างเปล่า:

```json
{}
```

**ตัวอย่างคำสั่ง cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย              | คำอธิบาย |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | กรองข้อมูลสำเร็จ; การตอบกลับมีรายละเอียดของคำสั่ง |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือไม่มี |
| 413  | ข้อมูลหนักเกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบแบบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ที่มีทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}