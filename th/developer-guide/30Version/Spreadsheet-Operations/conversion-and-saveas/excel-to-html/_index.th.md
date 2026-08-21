---
title: แปลง Excel เป็น HTML  
description: แปลงสมุดงาน Excel เป็นไฟล์ HTML โดยใช้ Aspose.Cells Cloud API เวอร์ชัน 3.0  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# แปลง Excel เป็น HTML  

Aspose.Cells Cloud มี REST endpoint ที่มีประสิทธิภาพสูงสำหรับการแปลงสมุดงาน Excel (XLS, XLSX, CSV เป็นต้น) ให้เป็นเอกสาร HTML ผลลัพธ์ที่ได้จะเป็นอ็อบเจกต์ **FileInfo** ซึ่งประกอบด้วยไฟล์ HTML ที่สร้างขึ้น (ชื่อไฟล์ ขนาด และเนื้อหาที่เข้ารหัสแบบ Base64)

---

## สิ่งที่ต้องมีก่อนเริ่มต้น

| ความต้องการ | วิธีการดำเนินการ |
|-------------|----------------|
| **บัญชี Aspose Cloud** | ลงทะเบียนที่ [aspose.cloud](https://www.aspose.cloud) |
| **โทเคน JWT** | รับโทเคนแบบ bearer จาก endpoint OAuth 2.0 `POST /connect/token` |
| **พื้นที่จัดเก็บ (ไม่บังคับ)** | หากต้องการให้ API อ่าน/เขียนไฟล์จากพื้นที่จัดเก็บเฉพาะ ให้สร้างพื้นที่จัดเก็บก่อน (เช่น Amazon S3, Azure Blob หรือพื้นที่จัดเก็บของ Aspose Cloud) |
| **cURL / SDK** | ไคลเอนต์ HTTP ใดก็ได้ที่รองรับ multipart/form-data (เช่น cURL, Postman หรือหนึ่งใน SDK ของ Aspose.Cells) |

---

## การยืนยันตัวตน

คำขอทั้งหมดที่ส่งไปยัง Aspose.Cells Cloud จำเป็นต้องใช้การยืนยันตัวตนแบบใช้โทเคน JWT

```http
Authorization: Bearer <access-token>
```

โทเคนต้องถูกรวมไว้ในส่วนหัว `Authorization` ของทุกคำขอ

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **หมายเหตุ** – คำขอต้องถูกส่งเป็น `multipart/form-data` โดยไฟล์ Excel จะเป็นส่วนแรกของเนื้อหาแบบ multipart

---

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยสูง และต้องใช้การยืนยันตัวตนแบบใช้โทเคน JWT <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">ตามเอกสารนี้</a>

## พารามิเตอร์ของคำขอ  

### พารามิเตอร์ Query  

| ชื่อพารามิเตอร์         | ชนิดข้อมูล | จำเป็น | ค่าเริ่มต้น | คำอธิบาย |
|--------------------------|------------|--------|-------------|-----------|
| `password`               | string     | ไม่จำเป็น | –           | รหัสผ่านสำหรับเปิดสมุดงานที่ได้รับการป้องกัน |
| `storageName`            | string     | ไม่จำเป็น | –           | ชื่อของพื้นที่จัดเก็บที่เก็บไฟล์ต้นฉบับไว้ |
| `checkExcelRestriction` | boolean    | ไม่จำเป็น | `true`      | เมื่อตั้งค่าเป็น `true` บริการจะตรวจสอบข้อจำกัดเฉพาะของ Excel (เช่น แผ่นงานที่ได้รับการป้องกัน) |
| `region`                 | string     | ไม่จำเป็น | –           | การตั้งค่าภูมิภาคสำหรับสมุดงาน (เช่น `en-US`) |
| `FontsLocation`          | string     | ไม่จำเป็น | –           | URL หรือพาธไปยังโฟลเดอร์ที่มีฟอนต์ที่ต้องการใช้ในการเรนเดอร์ |

### ข้อมูลแบบ Form (Multipart)  

| ชื่อ | ชนิดข้อมูล | จำเป็น | คำอธิบาย |
|------|------------|--------|-----------|
| **File** | file | **จำเป็น** | สมุดงาน Excel ที่ต้องการแปลง ต้องส่งเป็นส่วนแรกของคำขอแบบ multipart |

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## คำตอบกลับเมื่อประสบความสำเร็จ  

**สถานะโค้ด:** `200 OK`

| ฟิลด์        | ชนิดข้อมูล | คำอธิบาย |
|--------------|-------------|-----------|
| `Filename`   | string      | ชื่อไฟล์ HTML ที่สร้างขึ้น (เช่น `example.html`) |
| `FileSize`   | int         | ขนาดไฟล์ HTML เป็นไบต์ |
| `FileContent`| string      | เนื้อหา HTML ที่เข้ารหัสแบบ Base64 |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

โครงสร้างของคำตอบกลับถูกกำหนดโดยโมเดล **FileInfo**: [/cells/file-info](/cells/file-info/)

---

## คำตอบกลับเมื่อเกิดข้อผิดพลาด  

| โค้ด | ความหมาย                | ตัวอย่าง Payload |
|------|--------------------------|------------------|
| `400` | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง | ```json { "Code": "BadRequest", "Message": "ต้องมีส่วน 'File'" } ``` |
| `401` | ไม่ได้รับอนุญาต – โทเคน JWT ไม่ถูกต้องหรือขาดหาย | ```json { "Code": "InvalidToken", "Message": "โทเคนการเข้าถึงขาดหายหรือหมดอายุ" } ``` |
| `404` | ไม่พบ – ไฟล์ต้นฉบับไม่อยู่ในพื้นที่จัดเก็บที่ระบุ | ```json { "Code": "FileNotFound", "Message": "ไฟล์ 'my.xlsx' ไม่มีอยู่ในพื้นที่จัดเก็บ 'MyStorage'" } ``` |
| `413` | ข้อมูลหนักเกินไป – ไฟล์ที่อัปโหลดเกินขนาดที่อนุญาต | ```json { "Code": "RequestEntityTooLarge", "Message": "ไฟล์ที่อัปโหลดเกินขีดจำกัด 100 MB" } ``` |
| `429` | คำขอมากเกินไป –  vượtขีดจำกัดอัตราการเรียกใช้งาน | ```json { "Code": "TooManyRequests", "Message": "เกินขีดจำกัดอัตราการเรียกใช้งาน 60 ครั้งต่อนาที" } ``` |
| `500` | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดของเซิร์ฟเวอร์ | ```json { "Code": "InternalError", "Message": "เกิดข้อผิดพลาดที่ไม่คาดคิด กรุณาลองใหม่อีกครั้งในภายหลัง" } ``` |

---

## ขีดจำกัดอัตราการเรียกใช้งาน  

| ขีดจำกัด | คำอธิบาย |
|----------|-----------|
| **60 คำขอต่อนาที** ต่อบัญชี (ค่าเริ่มต้น) | หากเกินขีดจำกัดนี้จะได้รับคำตอบกลับ `429 Too Many Requests` ปรับเปลี่ยนตรรกะของไคลเอนต์หรือขอโควต้าที่สูงขึ้นผ่านพอร์ทัล Aspose Cloud |

---

## การรองรับ SDK  

Aspose มี SDK ชั้นนำสำหรับหลายภาษาที่ห่อหุ้ม endpoint นี้ไว้ ตัวอย่างด้านล่างแสดงการแปลงแบบเดียวกันโดยใช้ SDK ทางการ

| ภาษา | ตัวอย่าง |
|------|--------|
| C# | <details><summary>ดูตัวอย่าง</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java | <details><summary>ดูตัวอย่าง</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python | <details><summary>ดูตัวอย่าง</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js | <details><summary>ดูตัวอย่าง</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go | <details><summary>ดูตัวอย่าง</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP | <details><summary>ดูตัวอย่าง</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby | <details><summary>ดูตัวอย่าง</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl | <details><summary>ดูตัวอย่าง</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

สำหรับรายชื่อ SDK ที่รองรับทั้งหมดและคำแนะนำการติดตั้ง ดูที่ repository **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud>

---

## Endpoint ที่เกี่ยวข้อง  

| Endpoint | คำอธิบาย |
|----------|-----------|
| `POST /cells/{name}/saveAs` | บันทึกไฟล์ Excel ที่มีอยู่เป็น HTML (หรือรูปแบบอื่น) โดยตรงไปยังพื้นที่จัดเก็บ |
| `PUT /cells/convert` | แปลงสมุดงานเป็น HTML พร้อมตัวเลือกการแปลงเพิ่มเติม ผลลัพธ์จะถูกส่งกลับในส่วนเนื้อหาของคำตอบกลับ |
| `GET /cells/{name}` | ดึงข้อมูลสมุดงานที่จัดเก็บไว้แล้วในรูปแบบ HTML (หรือรูปแบบอื่น) พร้อมพารามิเตอร์ query ที่ระบุ |

---

## คำถามที่พบบ่อย  

**Q:** *ฉันจะยืนยันตัวตนเมื่อเรียกใช้ API แปลง Excel เป็น HTML ได้อย่างไร?*  
**A:** ใส่ส่วนหัว `Authorization: Bearer <access-token>` ที่ได้รับจาก endpoint OAuth 2.0 `/connect/token`

**Q:** *คำตอบกลับ `FileInfo` มีข้อมูลอะไรบ้าง?*  
**A:** มี 3 ฟิลด์คือ `Filename` (string), `FileSize` (integer, เป็นไบต์) และ `FileContent` (เนื้อหา HTML ที่เข้ารหัสแบบ Base64)

**Q:** *ฉันอาจเจอโค้ดข้อผิดพลาดอะไรบ้าง?*  
**A:** `400` (Bad Request), `401` (Unauthorized), `404` (File Not Found), `413` (Payload Too Large), `429` (Too Many Requests), `500` (Internal Server Error) แต่ละโค้ดจะส่ง JSON payload ที่มีฟิลด์ `Code` และ `Message`

**Q:** *ฉันสามารถระบุตำแหน่งฟอนต์ที่กำหนดเองได้หรือไม่?*  
**A:** ได้ ใช้พารามิเตอร์ query `FontsLocation` เพื่อชี้ไปยังโฟลเดอร์หรือ URL ที่มีฟอนต์ที่ต้องการใช้งาน

**Q:** *การดำเนินการนี้มีขีดจำกัดอัตราการเรียกใช้งานหรือไม่?*  
**A:** ขีดจำกัดเริ่มต้นคือ **60 ครั้งต่อนาที** ต่อบัญชี หากเกินขีดจำกัดนี้จะได้รับคำตอบกลับ `429 Too Many Requests`

---

## JSON‑LD Breadcrumb (ข้อมูลโครงสร้าง)

การเพิ่มบล็อกนี้จะช่วยปรับปรุง SEO โดยเปิดใช้งาน breadcrumb แบบ rich-snippet ในผลลัพธ์การค้นหา

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "หน้าแรก", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "ศูนย์พัฒนา", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "การแปลงข้อมูล", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel เป็น HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## บันทึกการเปลี่ยนแปลง  

| เวอร์ชัน | วันที่ | การเปลี่ยนแปลง |
|----------|--------|----------------|
| **v3.0** | 2024‑10‑01 | เวอร์ชันเปิดตัวครั้งแรกของ `PostConvertWorkbookToHtml` |
| **v3.1** | 2025‑04‑15 | เพิ่มพารามิเตอร์ query `region` และ `FontsLocation`; อัปเดตรูปแบบ payload ของข้อผิดพลาด |
| **v3.2** | 2026‑03‑20 | เพิ่มเอกสารขีดจำกัดอัตราการเรียกใช้งานและตัวอย่างคำตอบกลับข้อผิดพลาด |

--- 

*หากต้องการความช่วยเหลือเพิ่มเติม โปรดติดต่อทีมสนับสนุนของ Aspose หรือเข้าไปที่เอกสารอ้างอิง API ทางการ:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---