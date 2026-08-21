---
---
title: "Aspose.Cells Cloud API – รับรายการไฟล์ (เนื้อหาโฟลเดอร์)"
description: "ดึงรายการไฟล์และโฟลเดอร์ย่อยจากโฟลเดอร์ที่ระบุในพื้นที่เก็บข้อมูล Aspose.Cells Cloud"
keywords:
  - Aspose.Cells
  - API
  - Get Files List
  - Cloud Storage
  - Excel
  - REST
type: docs
weight: 100
---

การทำงาน **Get Files List** จะส่งคืนคอลเลกชันของไฟล์และโฟลเดอร์ย่อยที่เก็บอยู่ในโฟลเดอร์ที่ระบุของพื้นที่เก็บข้อมูล Aspose.Cells Cloud  
เป็นจุดเริ่มต้นหลักสำหรับการเรียกดูสมุดค่าบันทึก (workbook) Excel ที่อยู่บนคลาวด์ ไฟล์สำเนาสำรอง และไฟล์ประเภทอื่นๆ ที่รองรับ

## Aspose.Cells Cloud API – รับรายการไฟล์ (เนื้อหาโฟลเดอร์)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ตำแหน่ง | ประเภทข้อมูล | จำเป็น | คำอธิบาย                                                                 |
| ---------------- | -------- | ------------ | ------ | ------------------------------------------------------------------------ |
| **path**         | Path     | string       | ใช่    | เส้นทางไปยังโฟลเดอร์ในพื้นที่เก็บข้อมูลบนคลาวด์                         |
| **storageName**  | Query    | string       | ไม่จำเป็น | ชื่อของพื้นที่เก็บข้อมูลที่ต้องการใช้ หากไม่ระบุ จะใช้พื้นที่เก็บข้อมูลเริ่มต้น |
| **pageSize**     | Query    | integer      | ไม่จำเป็น | จำนวนสูงสุดของรายการที่จะส่งคืนต่อหน้า (ค่าเริ่มต้น: 100)                |
| **pageNumber**   | Query    | integer      | ไม่จำเป็น | หมายเลขหน้าที่ต้องการดึงข้อมูล (เริ่มต้นที่ 1, ค่าเริ่มต้น: 1)            |

- **Value** – อาเรย์ของออบเจกต์ `StorageFile` ออบเจกต์แต่ละตัวมีข้อมูลดังนี้:
  - `Name` – ชื่อไฟล์หรือโฟลเดอร์
  - `IsFolder` – เป็นค่า `true` หากรายการนี้เป็นโฟลเดอร์
  - `Size` – ขนาดเป็นไบต์ (โฟลเดอร์จะรายงานค่า `0`)
  - `ModifiedDate` – วันที่และเวลาของการแก้ไขครั้งล่าสุด (รูปแบบ ISO 8601)

### **การตอบกลับ**

**รหัสสถานะ HTTP**

| รหัส HTTP | สถานะ HTTP            | คำอธิบาย                                                           |
| --------- | --------------------- | ------------------------------------------------------------------ |
| 200       | OK                    | เรียกใช้เว็บ API สำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400       | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ)   |
| 401       | Unauthorized          | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                   |
| 413       | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                |
| 500       | Internal Server Error | เกิดข้อผิดพลาดของเซิร์ฟเวอร์โดยไม่คาดคิด                        |
|           |                       |                                                                    |

## ข้อมูลจำเพาะ OpenAPI

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการเชื่อมต่อผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานของโปรเจกต์ได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

---