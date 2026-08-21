---
title: "ปลดล็อกไฟล์ Excel"
second_title: "เอกสาร"
linktype: "ปลดล็อกไฟล์ Excel"
type: docs
url: /unlock-excel-files/
aliases: [/unlock/without-storage/, /unlock/, /unlock/without-using-storage/]
keywords: "ปลดล็อก Excel, Aspose.Cells Cloud, REST API, การปลดล็อก Excel, สมุดงานที่ป้องกันด้วยรหัสผ่าน, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Aspose.Cells Cloud REST API มี endpoint สำหรับปลดล็อกไฟล์ Excel ที่ป้องกันด้วยรหัสผ่าน มี SDK สำหรับภาษาโปรแกรมต่าง ๆ หลายภาษา ได้แก่ Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby และ Swift"
ArticleTitle: "ปลดล็อกไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API"
weight: 70
---

REST API นี้ใช้สำหรับปลดล็อกไฟล์ Excel

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### ความปลอดภัยและการพิสูจน์ตัวตน

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การพิสูจน์ตัวตนด้วย JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------ | -------------------- | ------------------------------------------ |
| file           | ไฟล์   | formData (HTTP body) | ไฟล์ที่จะอัปโหลด |
| password       | สตริง | query string         | รหัสผ่านสำหรับปลดล็อกไฟล์ (หากมีการป้องกันไว้) |

### การตอบกลับ

```json
{
  "Status":"OK",
  "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | กรองถูกใช้งานเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ operation |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | JWT token ไม่ถูกต้องหรือหายไป |
| 413  | ข้อมูลส่งไปขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ PostUnlock API ด้วย SDK

### ข้อกำหนด PostUnlock API

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) กำหนด API ที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

**หมายเหตุ**  
- API สามารถปลดล็อกไฟล์ Excel หลายไฟล์ในคำขอเดียว โดยแต่ละไฟล์จะถูกส่งกลับใน array `Files` ของการตอบกลับ  
- ตรวจสอบให้แน่ใจว่าเวอร์ชัน SDK ของคุณตรงกับเวอร์ชัน API (`v3.0`) เพื่อหลีกเลี่ยงปัญหาเรื่องความเข้ากันได้

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่าง ๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}