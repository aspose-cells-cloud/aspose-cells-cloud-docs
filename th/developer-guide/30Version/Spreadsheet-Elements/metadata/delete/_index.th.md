---
title: "ลบ metadata จากไฟล์ Excel"
second_title: "เอกสาร"
linktype: "ลบโดยไม่ใช้พื้นที่จัดเก็บ"
type: docs
url: "/metadata/delete/"
keywords: "Aspose.Cells, ลบ metadata, Excel API, คุณสมบัติเวิร์กบุ๊ก"
description: "ลบ metadata ของเวิร์กบุ๊ก (ผู้แต่ง, ชื่อ, ข้อมูลที่ปรับแต่งเอง) ผ่าน Aspose.Cells Cloud API รวมถึง endpoint, การตรวจสอบสิทธิ์, พารามิเตอร์, ตัวอย่าง cURL และ SDK"
weight: 55
ArticleTitle: "ลบ metadata จากไฟล์ Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

**ภาพรวม**  
การดำเนินการลบ metadata จะลบคุณสมบัติของเวิร์กบุ๊กทั้งหมด (มาตรฐานและปรับแต่งเอง) ออกจากไฟล์ Excel ที่อัปโหลด และส่งคืนไฟล์ที่ประมวลผลแล้วใน response

**ข้อกำหนดเบื้องต้น**
- JWT token ที่ถูกต้องของ Aspose.Cells Cloud (รับได้ผ่านกระบวนการตรวจสอบสิทธิ์ OAuth 2.0)
- รุ่น API **v3.0** (endpoint ที่ใช้ในตัวอย่างนี้)
- สำหรับการใช้งาน SDK ติดตั้ง Aspose.Cells Cloud SDK ที่เหมาะสมกับภาษาของคุณ (เช่น ผ่าน NuGet, Maven, npm, pip, CPAN หรือ Go modules)

API นี้เป็น REST API ที่ใช้ลบ **metadata** จากไฟล์ Excel หนึ่งไฟล์หรือหลายไฟล์ โดยจะลบคุณสมบัติของเวิร์กบุ๊ก เช่น ผู้แต่ง, ชื่อ และข้อมูลที่ปรับแต่งเอง จากนั้นส่งคืนไฟล์ที่ไม่มีข้อมูล metadata แล้ว

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

### **พารามิเตอร์ของ request**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| ---------------- | ------ | -------- | --------------------------------------------------------- |
| file             | file   | formData | ไฟล์ Excel ที่จะอัปโหลดเพื่อลบ **metadata** |
| type             | string | query    | ประเภทการดำเนินการ; ตั้งค่าเป็น **all** เพื่อลบ **metadata** ทั้งหมด |

<a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> กำหนด programming interface ที่เข้าถึงได้สาธารณะ และช่วยให้คุณสามารถเรียกใช้การโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่อยู่ใน command-line เพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**การตอบกลับข้อผิดพลาด** อาจประกอบด้วย:

- **400 Bad Request** – ขาดไฟล์หรือค่า `type` ไม่ถูกต้อง
- **401 Unauthorized** – JWT token ไม่ถูกต้องหรือขาดหายไป
- **500 Internal Server Error** – เกิดข้อผิดพลาดในการประมวลผลที่ฝั่งเซิร์ฟเวอร์

API จะส่งคืน JSON object ที่มีฟิลด์ `Error` พร้อมรายละเอียดสำหรับแต่ละกรณี

| โค้ด | ความหมาย | คำอธิบาย |
|------|----------|----------|
| 200 | OK | ลบ metadata แล้วและส่งคืนไฟล์ |
| 400 | Bad Request | ขาดไฟล์หรือค่า `type` ไม่ถูกต้อง |
| 401 | Unauthorized | JWT ไม่ถูกต้องหรือขาดหายไป |
| 500 | Internal Server Error | การประมวลผลที่เซิร์ฟเวอร์ล้มเหลว |

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดู <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้ Aspose.Cells web services โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}