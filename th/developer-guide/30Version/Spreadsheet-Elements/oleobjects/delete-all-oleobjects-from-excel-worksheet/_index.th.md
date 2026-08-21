---
title: ลบวัตถุ OLE ทั้งหมดในแผ่นงาน Excel
description: เรียนรู้วิธีการลบวัตถุ OLE ทั้งหมดออกจากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมถึง endpoint, พารามิเตอร์, ตัวอย่างคำขอ/คำตอบ, โค้ดตัวอย่าง SDK, การยืนยันตัวตน, การจัดการข้อผิดพลาด และคำถามที่พบบ่อย
keywords: Aspose.Cells Cloud, ลบวัตถุ OLE, Excel API, REST API, ล้างวัตถุ OLE ในแผ่นงาน, cloud SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# ลบวัตถุ OLE ทั้งหมดในแผ่นงาน Excel

**OleObjects – Clear** ลบ **วัตถุ OLE (Object Linking and Embedding)** ทั้งหมดออกจากแผ่นงานที่ระบุ โดยไม่ส่งผลต่อข้อมูลในเซลล์ การดำเนินการนี้มีประโยชน์สำหรับการทำความสะอาดสเปรดชีตแบบเก่า หรือการเตรียมสมุดบันทึกสำหรับการแจกจ่ายใหม่

---

## ข้อกำหนดเบื้องต้น

- โทเคนการเข้าถึง JWT ของ Aspose Cloud ที่ถูกต้อง (OAuth 2.0)  
- สมุดบันทึกเป้าหมายต้องถูกจัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud (หรือคุณต้องระบุ `folder`/`storageName` ที่ตำแหน่งของไฟล์)  
- เวอร์ชัน API **v3.0** หรือสูงกว่า  

> **หมายเหตุ:** การดำเนินการนี้เป็น *idempotent* – การเรียกใช้งานเมื่อไม่มีวัตถุ OLE อยู่จะส่งกลับสถานะ `200 OK` ที่ประสบความสำเร็จ

---

## คำขอ HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### พารามิเตอร์ในเส้นทาง (Path parameters)

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | จำเป็น | คำอธิบาย |
|------------------|-------------|--------|-----------|
| `name` | ข้อความ | ✔️ | ชื่อไฟล์สมุดบันทึก |
| `sheetName` | ข้อความ | ✔️ | ชื่อแผ่นงาน |

### พารามิเตอร์แบบ Query

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | จำเป็น | คำอธิบาย |
|------------------|-------------|--------|-----------|
| `folder` | ข้อความ | ไม่บังคับ | โฟลเดอร์ที่มีสมุดบันทึก |
| `storageName` | ข้อความ | ไม่บังคับ | ชื่อพื้นที่จัดเก็บที่สมุดบันทึกถูกจัดเก็บไว้ |

**ส่วนหัว (Headers)**

| ส่วนหัว | ค่า |
|---------|-----|
| `Authorization` | `Bearer <jwt token>` |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

---

## ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*แทนที่ `<jwt token>` ด้วยโทเคนการเข้าถึงที่ถูกต้อง และปรับค่า `folder`/`storageName` ตามความเหมาะสม*

---

## คำตอบที่ประสบความสำเร็จ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|----------|----------|
| 200 | OK | ตัวกรองถูกใช้งานเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400 | Bad Request | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload Too Large | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500 | Internal Server Error | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

---

## ตัวอย่าง SDK

โค้ดตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ **DeleteWorksheetOleObjects** โดยใช้ SDK ทางการของ Aspose.Cells Cloud แทนที่ค่า placeholder (`<YOUR_TOKEN>`, `<FILE_NAME>` เป็นต้น) ด้วยข้อมูลของคุณเอง

| ภาษา | ตัวอย่าง |
|------|---------|
| **C#** | <details><summary>แสดงตัวอย่าง C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>แสดงตัวอย่าง Java</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>แสดงตัวอย่าง Python</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>แสดงตัวอย่าง Node.js</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>แสดงตัวอย่าง Go</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("All OLE objects deleted")\n}\n```</details> |

*ไฟล์ซอร์สโค้ดเต็มรูปแบบสำหรับภาษาที่รองรับทั้งหมดมีอยู่ใน [GitHub repository ของ Aspose.Cells Cloud](https://github.com/aspose-cells-cloud)*

---

## ข้อผิดพลาดและการจัดการ

- **ความเป็นอิสระต่อการเรียกซ้ำ (Idempotency)** – การลบวัตถุ OLE จากแผ่นงานที่ไม่มีวัตถุ OLE อยู่แล้วจะยังคงส่งกลับ `200 OK`  
- **โทเคนหมดอายุ** – หากได้รับข้อผิดพลาด `401 Unauthorized` ให้ขอโทเคน JWT ใหม่แล้วลองอีกครั้ง  
- **ชื่อแผ่นงานไม่ถูกต้อง** – ตรวจสอบให้แน่ใจว่าชื่อแผ่นงานตรงกับกรณีการใช้ตัวพิมพ์ใหญ่-เล็กในสมุดบันทึก มิฉะนั้นจะส่งกลับ `400 Bad Request`  

จัดการข้อผิดพลาดแบบชั่วคราว (เช่น `500`) โดยใช้ตรรกะการลองใหม่พร้อมการหน่วงเวลาแบบ exponential back-off

---

## คำถามที่พบบ่อย

**Q1: ฉันจำเป็นต้องระบุพารามิเตอร์ `folder` และ `storageName` หรือไม่?**  
**A:** ไม่จำเป็น หากไม่ระบุ Aspose Cloud จะใช้พื้นที่จัดเก็บเริ่มต้นและโฟลเดอร์รากเป็นค่าเริ่มต้น

**Q2: ฉันสามารถลบวัตถุ OLE จากเซลล์ที่ระบุเท่านั้นได้หรือไม่?**  
**A:** endpoint นี้จะลบ **วัตถุ OLE ทั้งหมด** ออกจากแผ่นงาน หากต้องการลบวัตถุเพียงหนึ่งชิ้น ให้ใช้การดำเนินการ *ลบวัตถุ OLE ที่ระบุ*

**Q3: เกิดอะไรขึ้นหากสมุดบันทึกถูกล็อกสำหรับการแก้ไข?**  
**A:** API จะส่งกลับ `400 Bad Request` พร้อมข้อความระบุว่าไฟล์ถูกล็อก ตรวจสอบให้แน่ใจว่าไฟล์ไม่ได้ถูกเปิดใช้งานที่อื่นก่อนเรียก endpoint

**Q4: มีข้อจำกัดขนาดสำหรับสมุดบันทึกหรือไม่?**  
**A:** บริการนี้ใช้ข้อจำกัดขนาดไฟล์ทั่วไปของ Aspose Cloud (ปัจจุบันสูงสุดที่ 2 GB ต่อไฟล์) ไฟล์ที่มีขนาดใหญ่กว่านั้นอาจต้องแบ่งหรือประมวลผลเป็นชุดๆ

---

## แนวทางปฏิบัติที่ดี

- **ประสิทธิภาพ** – ใช้คุณสมบัติ `async` หรือ `defer` เมื่อโหลดสคริปต์จากบุคคลที่สามบนเว็บไซต์เอกสารของคุณ เพื่อลดเวลาโหลดหน้าเว็บในครั้งแรก  
- **ความปลอดภัย** – เพิ่ม `rel="noopener noreferrer"` สำหรับลิงก์ภายนอกที่เปิดในแท็บใหม่  
- **การเข้าถึง (Accessibility)** – ไอคอนที่ไม่จำเป็น (เช่น ลูกศรชี้ลงข้างล่างในเมนูด้านข้าง) ควรมี `alt=""` และ `role="presentation"` เพื่อให้สอดคล้องกับมาตรฐาน WCAG AA  
- **ความสอดคล้อง** – ใช้รูปแบบวันที่แบบ ISO-8601 (`YYYY-MM-DD`) เพื่อหลีกเลี่ยงปัญหาการเข้ารหัส

---

## การดำเนินการที่เกี่ยวข้อง

- **เพิ่มวัตถุ OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **ลบวัตถุ OLE ที่ระบุ** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

ใช้ลิงก์นำทางที่ด้านล่างของหน้าเพื่อเปลี่ยนไปยังการดำเนินการ API ที่เกี่ยวข้อง