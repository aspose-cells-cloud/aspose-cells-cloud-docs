---
title: "API ของ Aspose.Cells Cloud สำหรับดึงข้อมูลเวอร์ชันไฟล์ – การดึงข้อมูลประวัติเวอร์ชันไฟล์อย่างรวดเร็ว"
second_title: "เอกสาร"
ArticleTitle: "การจัดการ Excel บนคลาวด์ – ดึงข้อมูลประวัติเวอร์ชันไฟล์ได้อย่างรวดเร็วใน Aspose.Cells Cloud"
linktype: "docs"
url: /th/get-file-versions/
keywords: "API Aspose Cells, เวอร์ชันไฟล์, การจัดการเวอร์ชันสเปรดชีต, API พื้นที่จัดเก็บบนคลาวด์, REST, ประวัติไฟล์ Excel"
description: "ดึงรายชื่อประวัติเวอร์ชันทั้งหมดสำหรับไฟล์ Excel ที่จัดเก็บไว้ใน Aspose.Cells Cloud รองรับการเลือกพื้นที่จัดเก็บ การยืนยันตัวตน และรหัสข้อผิดพลาดแบบละเอียด"
weight: 100
---

ดึงรายชื่อเวอร์ชันทั้งหมดของไฟล์สเปรดชีตที่ระบุซึ่งจัดเก็บไว้ใน Aspose.Cells Cloud ปลายทางนี้ช่วยให้นักพัฒนาสามารถติดตามการเปลี่ยนแปลง ตรวจสอบการแก้ไข และใช้งานเวิร์กโฟลว์การควบคุมเวอร์ชันได้โดยตรงจากพื้นที่จัดเก็บบนคลาวด์

API **GetFileVersions** จะส่งคืนเวอร์ชันทั้งหมดของไฟล์สเปรดชีตที่ระบุซึ่งจัดเก็บไว้ใน Aspose.Cells Cloud ช่วยให้คุณรักษาประวัติการเปลี่ยนแปลงที่สมบูรณ์สำหรับแต่ละไฟล์

## **API สำหรับ Excel: ดึงข้อมูลเวอร์ชันไฟล์**

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **การรักษาความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเคน JWT</a>

### พารามิเตอร์คำขอของ API **GetFileVersions** มีดังนี้

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย                                                                                   |
| ---------------- | ------ | -------- | ------------------------------------------------------------------------------------------- |
| `path`           | String | Path     | **จำเป็น** ระบุเส้นทางแบบเต็มของไฟล์ที่ต้องการดึงข้อมูลเวอร์ชัน                           |
| `storageName`    | String | Query    | ไม่บังคับ ชื่อของพื้นที่จัดเก็บที่มีไฟล์ หากไม่ระบุจะใช้พื้นที่จัดเก็บเริ่มต้น               |

### **การตอบกลับ**

```json
{
  "Name": "FileVersions",
  "Description": [
    "มีรายชื่อเวอร์ชันของไฟล์สำหรับเอกสารที่ระบุ"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["คอลเลกชันของรายละเอียดเวอร์ชันไฟล์"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

เมื่อคำขอสำเร็จ API จะส่งคืน **HTTP 200 OK** พร้อมข้อมูล JSON ที่มีอาร์เรย์ `Value` ของวัตถุเวอร์ชันไฟล์ ดังตัวอย่างข้างต้น

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย              | คำอธิบาย                                                          |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | สำเร็จ (OK)           | ประมวลผลตัวกรองสำเร็จ การตอบกลับมีรายละเอียดการดำเนินการ     |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)         |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                  |
| 413  | ข้อมูลที่ส่งมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                               |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์                         |

## ข้อกำหนด OpenAPI

[ข้อกำหนด OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) มีอินเทอร์เฟซโปรแกรมมิ่งที่ครอบคลุมสำหรับการดำเนินการ REST ผ่านเบราว์เซอร์เว็บโดยตรง

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK จะช่วยให้การพัฒนาเป็นไปอย่างคล่องตัว โดยซ่อนความซับซ้อนระดับต่ำไว้ ทำให้นักพัฒนาสามารถมุ่งเน้นไปที่ฟังก์ชันหลักได้ คุณสามารถดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมดได้ที่ [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการโต้ตอบกับบริการเว็บของ Aspose.Cells ผ่านภาษาการเขียนโปรแกรมต่างๆ:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}