---
---
title: "API คัดลอกไฟล์ Aspose.Cells Cloud – อินเทอร์เฟซสำหรับการคัดลอกไฟล์ Excel และดำเนินการแบบแบตช์ในคลาวด์อย่างรวดเร็ว"
second_title: "เอกสาร"
ArticleTitle: "โซลูชันจัดการไฟล์ Excel บนคลาวด์ – คำอธิบายรายละเอียดเกี่ยวกับฟังก์ชันการคัดลอกแบบแบตช์ของ API คัดลอกไฟล์ Aspose.Cells"
linktype: "คัดลอกไฟล์"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, การคัดลอกไฟล์ Excel, การจัดเก็บข้อมูลบนคลาวด์, REST API"
description: "เรียนรู้วิธีใช้ API CopyFile ของ Aspose.Cells Cloud เพื่อคัดลอกไฟล์ Excel อย่างมีประสิทธิภาพและจัดการไฟล์ระหว่างตำแหน่งการจัดเก็บข้อมูลต่างๆ"
weight: 100
---

**copyFile** API ช่วยให้ผู้ใช้สามารถคัดลอกไฟล์ Excel จากเส้นทางต้นทางไปยังเส้นทางปลายทางได้ โดยรองรับการเลือกใช้ระบบการจัดเก็บข้อมูลต่างๆ

## **API สำหรับ Excel: คัดลอกไฟล์**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์ของคำขอสำหรับ **copyFile** API มีดังนี้

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTPBody | คำอธิบาย                                     |
| ---------------- | ---------- | -------------------------- | -------------------------------------------- |
| srcPath          | String     | Path                       | เส้นทางต้นทางของไฟล์ที่ต้องการคัดลอก       |
| destPath         | String     | Query                      | เส้นทางปลายทางที่ไฟล์จะถูกบันทึก           |
| srcStorageName   | String     | Query                      | ชื่อของระบบการจัดเก็บข้อมูลต้นทาง           |
| destStorageName  | String     | Query                      | ชื่อของระบบการจัดเก็บข้อมูลปลายทาง          |
| versionId        | String     | Query                      | ID รุ่นของไฟล์ที่ต้องการคัดลอก (ไม่บังคับ)   |

### **การตอบกลับ**

หากดำเนินการสำเร็จ การตอบกลับจะไม่มีเนื้อหาใดๆ กลับมา โดยโค้ดสถานะ HTTP ที่พบบ่อยมีดังนี้:

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย             | คำอธิบาย                                                       |
| ---- | --------------------- | -------------------------------------------------------------- |
| 200  | OK (สำเร็จ)          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request (คำขอไม่ถูกต้อง) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)       |
| 401  | Unauthorized (ไม่ได้รับอนุญาต) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                               |
| 413  | Payload Too Large (ข้อมูลส่งไปมีขนาดใหญ่เกินไป) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด                      |
| 500  | Internal Server Error (ข้อผิดพลาดภายในเซิร์ฟเวอร์) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์                     |

## วิธีใช้ Copy File API ผ่าน SDK?

### ข้อมูลจำเพาะ API คัดลอกไฟล์

[ข้อมูลจำเพาะ API คัดลอกไฟล์](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) จัดเตรียมอินเทอร์เฟซโปรแกรมที่เปิดเผยให้ใช้งานได้โดยสาธารณะ เพื่อให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
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

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้เบื้องหลัง ทำให้คุณสามารถแปลงข้อมูลตารางในสเปรดชีตเป็นภาพได้ด้วยโค้ดเพียงไม่กี่บรรทัด โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ: