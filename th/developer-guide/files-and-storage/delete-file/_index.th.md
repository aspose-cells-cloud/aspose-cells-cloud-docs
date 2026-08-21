---
---
title: "Aspose.Cells Cloud – API สำหรับลบไฟล์"
second title: "เอกสาร"
ArticleTitle: "Aspose.Cells Cloud – API สำหรับลบไฟล์"
linktitle: "ลบไฟล์"
type: docs
url: /delete-file/
keywords: "Aspose Cells, API สำหรับลบไฟล์, พื้นที่จัดเก็บข้อมูลบนคลาวด์สำหรับ Excel, REST API, การจัดการไฟล์"
description: "ลบไฟล์ Excel ออกจากพื้นที่จัดเก็บข้อมูลบนคลาวด์ของ Aspose.Cells Cloud โดยใช้ RESTful Delete File API ซึ่งรวมถึง endpoint, พารามิเตอร์, การยืนยันตัวตน และโค้ดตัวอย่าง"
weight: 100
---

**deleteFile** API จะลบไฟล์ที่ระบุออกจากพื้นที่จัดเก็บข้อมูลบนคลาวด์ ช่วยให้คุณจัดการทรัพยากรและข้อมูลได้อย่างมีประสิทธิภาพ

## **Excel API : ลบไฟล์**

### Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                      |
| :------------- | :----- | :------- | :------------------------------------------------------------------------------------------ |
| `path`         | string | Path     | เส้นทาง (URL-encoded) ของไฟล์ที่ต้องการลบ                                                      |
| `storageName`  | string | Query    | ชื่อของพื้นที่จัดเก็บข้อมูลที่ไฟล์นั้นอยู่ ไม่ต้องระบุหากใช้พื้นที่จัดเก็บข้อมูลเริ่มต้น              |
| `versionId`    | string | Query    | ตัวระบุเวอร์ชันของไฟล์ที่ต้องการลบ หากไม่ระบุ จะลบเวอร์ชันล่าสุดออก                           |

### คำอธิบายคำตอบ

หากคำขอมีความสำเร็จ จะได้รับ **HTTP 200** พร้อมเนื้อหาคำตอบว่างเปล่า ไม่มี JSON payload คืนกลับมา

```json
{}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                | คำอธิบาย                                                           |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)             | แอ็คชันถูกดำเนินการเรียบร้อย; คำตอบประกอบด้วยรายละเอียดของ operation         |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์สูญหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                          |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือไม่ได้ระบุ                                            |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                                      |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                    |

## ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST interactions โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
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

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ