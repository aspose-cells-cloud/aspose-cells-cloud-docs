---
---
title: "API ดาวน์โหลดไฟล์ของ Aspose.Cells Cloud – อินเทอร์เฟซสำหรับการดาวน์โหลดไฟล์อย่างรวดเร็วในคลาวด์"
second_title: "เอกสาร"
ArticleTitle: "API ดาวน์โหลดไฟล์ของ Aspose.Cells Cloud – อินเทอร์เฟซสำหรับการดาวน์โหลดไฟล์อย่างรวดเร็วในคลาวด์"
linktitle: "API ดาวน์โหลดไฟล์"
type: docs
url: /download-file/
keywords: "Aspose.Cells, API ดาวน์โหลดไฟล์, พื้นที่จัดเก็บข้อมูล Excel บนคลาวด์, REST API, การดาวน์โหลดไฟล์, PDF, CSV, SDK"
description: "ดาวน์โหลดไฟล์ Excel, PDF, CSV และรูปแบบอื่นๆ จากพื้นที่จัดเก็บข้อมูล Aspose.Cells Cloud โดยใช้ API ดาวน์โหลดไฟล์ (v4.0) รวมถึง endpoint, พารามิเตอร์, รายละเอียดการตรวจสอบสิทธิ์ และตัวอย่างโค้ด"
weight: 100
---

**API ดาวน์โหลดไฟล์ (DownloadFile)** ช่วยให้คุณดึงข้อมูลไฟล์ที่จัดเก็บไว้ในพื้นที่จัดเก็บข้อมูล Aspose.Cells Cloud ได้ API ดาวน์โหลดไฟล์มีความจำเป็นสำหรับการเข้าถึงไฟล์สเปรดชีต Excel, PDF, CSV และรูปแบบอื่นๆ ที่รองรับโดยตรงจากคลาวด์

## **API สำหรับ Excel: ดาวน์โหลดไฟล์**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วย JWT token</a>

```bash
-H "Authorization: Bearer {access_token}"
```

### พารามิเตอร์คำขอของ **API ดาวน์โหลดไฟล์ (DownloadFile)** มีดังนี้

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง (Path / Query) | คำอธิบาย                                                                 |
|------------------|-------------|------------------------|--------------------------------------------------------------------------|
| path             | String      | Path                   | เส้นทางเสมือน (virtual path) ไปยังไฟล์ที่คุณต้องการดาวน์โหลด           |
| storageName      | String      | Query                  | ชื่อของพื้นที่จัดเก็บข้อมูลที่จะดึงไฟล์จากนั้น                                  |
| versionId        | String      | Query                  | ตัวระบุเวอร์ชันของไฟล์ที่ต้องการดาวน์โหลด (ถ้ามี)                            |

### **คำตอบที่ได้รับ (Response)**

API จะส่งกลับ **สตรีมไฟล์แบบไบนารี** เฮดเดอร์ `Content-Type` จะตรงกับรูปแบบไฟล์ (เช่น `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` สำหรับไฟล์ XLSX) โดยไม่มีการส่งกลับ JSON payload

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย             | คำอธิบาย                                                                 |
|-----|----------------------|--------------------------------------------------------------------------|
| 200 | คำขอสำเร็จ (OK)     | ใช้ตัวกรองสำเร็จ; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ                   |
| 400 | คำขอผิดรูปแบบ (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ประเภทที่ไม่รองรับ)                |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                                               |
| 413 | ข้อมูลที่ส่งมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                              |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                        |

## ข้อมูลจำเพาะ OpenAPI

[ข้อมูลจำเพาะ OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถใช้งาน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์โดยใช้ cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}