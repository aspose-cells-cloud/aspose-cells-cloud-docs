---
title: "วิธีการลบแผ่นงานในสมุดงาน Excel"
second_title: "Document"
linktype: "ลบ"
type: docs
url: /worksheets/delete/
keywords: "Aspose.Cells, Cloud, REST API, Delete Worksheet, Excel, C#, Java, Python"
description: "เรียนรู้วิธีการลบแผ่นงานเดียวหรือหลายแผ่นจากสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่างโค้ด C#, Java และ Python รวมถึงข้อกำหนดเบื้องต้น เคล็ดลับการจัดการข้อผิดพลาด และการดำเนินการที่เกี่ยวข้องอื่นๆ"
weight: 20
ArticleTitle: "ลบแผ่นงานในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

## การทำงานกับการลบแผ่นงานในสมุดงาน Excel

เมื่อแอปพลิเคชันสร้างหรือแก้ไขไฟล์ Excel แบบไดนามิก คุณอาจจำเป็นต้องลบแผ่นงานที่ไม่จำเป็นอีกต่อไป เช่น รายงานชั่วคราว แผ่นงานตัวอย่าง หรือข้อมูลที่ล้าสมัย Aspose.Cells Cloud API ช่วยให้คุณลบแผ่นงานเดียวหรือหลายแผ่นในคำขอเดียวได้อย่างง่ายดาย

**อ้างอิง API**

| รายการ | รายละเอียด |
|--------|-------------|
| **HTTP Method** | `DELETE` |
| **Endpoint** | `/cells/{fileName}/worksheets` |
| **Path Parameters** | `fileName` – ชื่อไฟล์ Excel (จำเป็นต้องระบุ) |
| **Query Parameters** | `sheetName` – ชื่อแผ่นงานที่ต้องการลบ (ไม่บังคับ, สำหรับการลบแผ่นเดียว) <br> `folder` – โฟลเดอร์ต้นทางในพื้นที่เก็บข้อมูล (ไม่บังคับ) <br> `storage` – ชื่อพื้นที่เก็บข้อมูลของ Aspose Cloud (ไม่บังคับ) |
| **Request Body** | *ไม่มี* |
| **Success Response** | `200 OK` – ลบแผ่นงานเรียบร้อยแล้ว ส่งคืนออบเจกต์ JSON พร้อมสถานะการดำเนินการ |
| **Error Responses** | `400 Bad Request` – พารามิเตอร์ไม่ถูกต้อง <br> `401 Unauthorized` – การยืนยันตัวตนล้มเหลว <br> `404 Not Found` – ไม่พบไฟล์หรือแผ่นงาน <br> `500 Internal Server Error` – ปัญหาฝั่งเซิร์ฟเวอร์ |

**คำขอ**  

เพื่อลบแผ่นงานหนึ่งแผ่นหรือหลายแผ่น ให้ส่งคำขอ `DELETE` ไปยัง endpoint ดังกล่าว โดยรวมพารามิเตอร์ `fileName` ที่จำเป็น และอาจรวมพารามิเตอร์ `sheetName` สำหรับการลบแผ่นงานเดียว เมื่อไม่ระบุ `sheetName` API จะลบแผ่นงานทั้งหมดในสมุดงาน

**พารามิเตอร์**  

- `fileName` (string, จำเป็น): ชื่อไฟล์ Excel พร้อมนามสกุลไฟล์  
- `sheetName` (string, ไม่บังคับ): ชื่อแผ่นงานที่ต้องการลบ หากไม่ระบุ API จะลบแผ่นงานทั้งหมด  
- `folder` (string, ไม่บังคับ): เส้นทางไปยังโฟลเดอร์ที่เก็บไฟล์ไว้ในพื้นที่เก็บข้อมูล  
- `storage` (string, ไม่บังคับ): ชื่อพื้นที่เก็บข้อมูลของ Aspose Cloud ที่จะใช้งาน

**การตอบกลับ**  

- **200 OK** – ตัวอย่าง JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "ลบแผ่นงานเรียบร้อยแล้ว"
  }
  ```
- **400 Bad Request** – พารามิเตอร์คำขอไม่ถูกต้อง  
- **401 Unauthorized** – ไม่มีหรือโทเค็นยืนยันตัวตนไม่ถูกต้อง  
- **404 Not Found** – ไฟล์หรือแผ่นงานที่ระบุไม่มีอยู่  
- **500 Internal Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์

**ตัวอย่าง**  

*ด้านล่างนี้คือตัวอย่างโค้ดสั้นๆ ที่แสดงวิธีการเรียก endpoint การลบโดยใช้ภาษาที่นิยมสามภาษา*

**ตัวอย่าง C#**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"สถานะ: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"ข้อผิดพลาด: {ex.Message}");
}
```

**ตัวอย่าง Java**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("สถานะ: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("ข้อผิดพลาด: " + e.getMessage());
        }
    }
}
```

**ตัวอย่าง Python**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"สถานะ: {response.status}")
except ApiException as e:
    print(f"ข้อผิดพลาด: {e}")
```

**การจัดการข้อผิดพลาด**  

- ตรวจสอบให้แน่ใจว่าโทเค็นยืนยันตัวตนยังใช้งานได้ก่อนส่งคำขอ  
- ตรวจสอบโค้ดสถานะการตอบกลับ และจัดการตามแต่ละกรณีของ `400`, `401`, `404`, และ `500`  
- ใช้บล็อก try-catch (หรือกลไกที่เทียบเท่า) เพื่อจับข้อผิดพลาดด้านเครือข่ายหรือ SDK

**การดำเนินการที่เกี่ยวข้อง**  

- [เพิ่มแผ่นงาน](/worksheets/add/) – สร้างแผ่นงานใหม่ในสมุดงานที่มีอยู่  
- [คัดลอกแผ่นงาน](/worksheets/copy/) – ทำซ้ำแผ่นงานที่มีอยู่  
- [เปลี่ยนชื่อแผ่นงาน](/worksheets/rename/) – เปลี่ยนชื่อของแผ่นงาน  
- [ย้ายแผ่นงาน](/worksheets/move/) – เรียงลำดับแผ่นงานใหม่ภายในสมุดงาน  
---