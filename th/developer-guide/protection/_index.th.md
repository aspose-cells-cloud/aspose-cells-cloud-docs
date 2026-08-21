---
---
title: "Aspose.Cells Cloud Web API – ตั้งค่า/แก้ไขรหัสผ่านการเปิดไฟล์สำหรับไฟล์ Excel"
second_title: "คู่มือนักพัฒนาอย่างครบถ้วน"
ArticleTitle: "การป้องกันสเปรดชีต – ตั้งค่ารหัสผ่านการเปิดและรหัสผ่านการแก้ไข"
linktype: "docs"
url: "/protection/"
keywords: "Aspose.Cells, Cloud, API, สเปรดชีต, การป้องกัน, รหัสผ่านการเปิด, รหัสผ่านการอ่าน-เขียน, Excel"
description: "เรียนรู้วิธีการป้องกันสมุดงาน Excel ด้วยรหัสผ่านการเปิดหรือรหัสผ่านการอ่าน-เขียนโดยใช้ Aspose.Cells Cloud REST API ประกอบด้วยไวยากรณ์คำร้องขอ ตัวอย่างโค้ด และการจัดการข้อผิดพลาด"
weight: 60
---

ในคู่มือนี้คุณจะได้เรียนรู้วิธีการตั้งค่า แก้ไข และลบ **รหัสผ่านการเปิด** และ **รหัสผ่านการอ่าน-เขียน** สำหรับสเปรดชีตโดยใช้ Aspose.Cells Cloud Web API คุณสมบัติเหล่านี้ช่วยปกป้องข้อมูลที่ละเอียดอ่อนในสมุดงาน Excel ของคุณ

**ข้อกำหนดเบื้องต้น**  
- บัญชี Aspose.Cells Cloud ที่ยังไม่หมดอายุพร้อมคีย์ API และ SID ที่ถูกต้อง  
- สมุดงานที่คุณต้องการป้องกันต้องถูกอัปโหลดลงในพื้นที่จัดเก็บของ Aspose Cloud หรือเข้าถึงได้ผ่าน URL สาธารณะ  

**การอ้างอิง API**  

| **วิธี HTTP** | **จุดปลายทาง (Endpoint)** | **พารามิเตอร์แบบ Query / Path** | **คำอธิบาย** |
|-----------------|--------------|----------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (path) – ชื่อสมุดงาน<br>`openPassword` (query, ไม่บังคับ) – รหัสผ่านที่ต้องใช้เพื่อเปิดไฟล์<br>`readWritePassword` (query, ไม่บังคับ) – รหัสผ่านที่ต้องใช้เพื่อแก้ไขไฟล์ | ตั้งค่าหรืออัปเดตรหัสผ่านการเปิดและ/หรือรหัสผ่านการอ่าน-เขียนสำหรับสมุดงานที่ระบุ |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (path) – ชื่อสมุดงาน | ลบรหัสผ่านที่ป้องกันสมุดงานทั้งหมด |

**ตัวอย่างเนื้อหาคำร้อง (JSON)**  

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**ตัวอย่างการตอบกลับ (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "อัปเดตการป้องกันสมุดงานเรียบร้อยแล้ว"
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำร้องขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งไปใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

**ตัวอย่างโค้ด**

*C# (Aspose.Cells Cloud SDK)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (Aspose.Cells Cloud SDK)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**การจัดการข้อผิดพลาด**  
เมื่อเกิดข้อผิดพลาด API จะส่งกลับ JSON ที่มี `Code`, `Message` และอาจมี `Description` ด้วย ให้ตรวจสอบโค้ดสถานะและจัดการตามตรรกะของแอปพลิเคชันของคุณ

**หัวข้อที่เกี่ยวข้อง**  

- **[วิธีการป้องกันสเปรดชีตด้วยรหัสผ่านโดยใช้ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/)**  
- **[วิธีการยกเลิกการป้องกันสเปรดชีตด้วยรหัสผ่านโดยใช้ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/)**  
---