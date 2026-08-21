---
title: "Aspose.Cells Cloud API – การจัดการไฟล์และโฟลเดอร์ (อัปโหลด ดาวน์โหลด คัดลอก ย้าย)"
second_title: "เอกสาร"
ArticleTitle: "การจัดการไฟล์บนคลาวด์สำหรับ Excel – โซลูชันที่มีประสิทธิภาพและปลอดภัยสำหรับการจัดเก็บไฟล์ Excel และการจัดระเบียบอย่างชาญฉลาด"
linktype: "files-and-storage"
type: docs
url: /files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: "Aspose.Cells Cloud, API สำหรับการจัดเก็บไฟล์, อัปโหลดไฟล์ Excel, ดาวน์โหลดไฟล์ Excel, คัดลอกไฟล์, ย้ายไฟล์, ลบไฟล์, การจัดการโฟลเดอร์, REST API, ตัวอย่าง cURL"
description: "คู่มือแบบครอบคลุมเกี่ยวกับการจัดการไฟล์ Excel และโฟลเดอร์ในพื้นที่จัดเก็บของ Aspose.Cells Cloud ประกอบด้วยการดำเนินการอัปโหลด ดาวน์โหลด คัดลอก ย้าย ลบ และการจัดการโฟลเดอร์ พร้อมตัวอย่าง cURL พารามิเตอร์ที่จำเป็น และหมายเหตุเกี่ยวกับการยืนยันตัวตน"
weight: 100
---

Aspose.Cells Cloud มีฟังก์ชันช่วยที่ครอบคลุมสำหรับการใช้งานไฟล์ที่จัดเก็บไว้ในพื้นที่จัดเก็บของ Aspose.Cells Cloud หรือพื้นที่จัดเก็บบนคลาวด์ของบุคคลที่สามที่คุณเลือกใช้ หากต้องการความช่วยเหลือในการตั้งค่าพื้นที่จัดเก็บของบุคคลที่สาม โปรดดูที่ [หัวข้อช่วยเหลือของอินเทอร์เฟซผู้ใช้ Aspose Cloud](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics)

**Aspose.Cells Cloud มี API สำหรับการดำเนินการเกี่ยวกับไฟล์ โฟลเดอร์ และพื้นที่จัดเก็บหลากหลาย**

> **หมายเหตุ:** การเรียก API ทั้งหมดต้องใช้ **HTTPS** สำหรับรายละเอียดเกี่ยวกับการรับ JWT token โปรดดูที่ [คู่มือการยืนยันตัวตน](/cells/authentication/)

**ข้อกำหนดเบื้องต้น:** เพื่อใช้งาน API เหล่านี้ คุณต้องมีบัญชี Aspose Cloud ที่ถูกต้อง รับ JWT access token และมีการกำหนดค่าพื้นที่จัดเก็บไว้แล้ว (ไม่ว่าจะเป็นพื้นที่จัดเก็บของ Aspose Cloud หรือพื้นที่จัดเก็บของบุคคลที่สามที่เชื่อมต่อไว้)

**อัปเดตล่าสุด:** 2024-12-01

## **วิธีการอัปโหลดไฟล์**

### ข้อมูล API สำหรับการอัปโหลดไฟล์

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางที่จะอัปโหลดไฟล์ รวมถึงชื่อไฟล์และนามสกุล (เช่น `/folder1/Report.xlsx`) |
| file           | file      | formData | ไฟล์ที่จะอัปโหลด |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะใช้ |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | อัปโหลดไฟล์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT token ไม่ถูกต้องหรือขาดหาย |
| 404  | ไม่พบพื้นที่จัดเก็บ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการอัปโหลดไฟล์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการอัปโหลดไฟล์ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: ขนาดไฟล์สูงสุดที่สามารถอัปโหลดได้คือ 100 MB อาจมีข้อจำกัดด้านอัตราการเรียกใช้งาน*

## **วิธีการดาวน์โหลดไฟล์**

### ข้อมูล API สำหรับการดาวน์โหลดไฟล์

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางไฟล์ (เช่น `/folder/Report.xlsx`) |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะใช้ |
| versionId      | string    | query   | ตัวระบุเวอร์ชันไฟล์ที่จะดาวน์โหลด (ไม่บังคับ) |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ดาวน์โหลดไฟล์เรียบร้อยแล้ว สตรีมไบนารีถูกส่งกลับมา |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบไฟล์ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการดาวน์โหลดไฟล์

{{< tabs tabTotal="2" tabID="13" tabName13="คำขอ" tabName14="การตอบกลับ" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<ข้อมูลไบนารี>"
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การตอบกลับจะมีสตรีมไบนารีของไฟล์ ให้บันทึกผลลัพธ์เป็นไฟล์เมื่อใช้ cURL (`-o filename.xlsx`)*

## **วิธีการลบไฟล์**

### ข้อมูล API สำหรับการลบไฟล์

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางไฟล์ (เช่น `/folder/Report.xlsx`) |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะใช้ |
| versionId      | string    | query   | ตัวระบุเวอร์ชันไฟล์ที่จะลบ (ไม่บังคับ) |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ลบไฟล์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT token ไม่ถูกต้อง |
| 404  | ไม่พบไฟล์ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการลบไฟล์

{{< tabs tabTotal="2" tabID="15" tabName15="คำขอ" tabName16="การตอบกลับ" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การลบไฟล์เป็นการกระทำที่ถาวร ตรวจสอบให้แน่ใจว่ามีการสำรองข้อมูลไว้หากจำเป็น*

## **วิธีการคัดลอกไฟล์**

### ข้อมูล API สำหรับการคัดลอกไฟล์

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| srcPath        | string    | path    | เส้นทางไฟล์ต้นทาง (เช่น `/folder/Source.xlsx`) |
| destPath       | string    | query   | เส้นทางไฟล์ปลายทาง (เช่น `/folder/Destination.xlsx`) |
| srcStorageName | string    | query   | ชื่อพื้นที่จัดเก็บต้นทาง (ไม่บังคับ) |
| destStorageName| string    | query   | ชื่อพื้นที่จัดเก็บปลายทาง (ไม่บังคับ) |
| versionId      | string    | query   | ตัวระบุเวอร์ชันไฟล์ที่จะคัดลอก (ไม่บังคับ) |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | คัดลอกไฟล์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบไฟล์ต้นทาง |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการคัดลอกไฟล์

{{< tabs tabTotal="2" tabID="17" tabName17="คำขอ" tabName18="การตอบกลับ" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Report.xlsx?destPath=MyFolder/ReportCopy.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การดำเนินการคัดลอกไม่ได้ลบไฟล์ต้นทาง*

## **วิธีการย้ายไฟล์**

### ข้อมูล API สำหรับการย้ายไฟล์

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| srcPath        | string    | path    | เส้นทางไฟล์ต้นทาง (เช่น `/folder/Source.xlsx`) |
| destPath       | string    | query   | เส้นทางไฟล์ปลายทาง (เช่น `/folder/Destination.xlsx`) |
| srcStorageName | string    | query   | ชื่อพื้นที่จัดเก็บต้นทาง (ไม่บังคับ) |
| destStorageName| string    | query   | ชื่อพื้นที่จัดเก็บปลายทาง (ไม่บังคับ) |
| versionId      | string    | query   | ตัวระบุเวอร์ชันไฟล์ที่จะย้าย (ไม่บังคับ) |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ย้ายไฟล์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบไฟล์ต้นทาง |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการย้ายไฟล์

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Report.xlsx?destPath=MyFolder/ReportMoved.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การย้ายไฟล์จะรักษาประวัติเวอร์ชันของไฟล์ไว้*

## **วิธีการสร้างโฟลเดอร์**

### ข้อมูล API สำหรับการสร้างโฟลเดอร์

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางโฟลเดอร์ที่จะสร้าง (เช่น `folder1/folder2/`) |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะใช้ |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | สร้างโฟลเดอร์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – เส้นทางหรือพารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการสร้างโฟลเดอร์

{{< tabs tabTotal="2" tabID="3" tabName3="คำขอ" tabName4="การตอบกลับ" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "newfolder"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: เส้นทางโฟลเดอร์มีการแยกแยะตัวพิมพ์เล็ก-ใหญ่*

## **วิธีการรับรายการไฟล์ในโฟลเดอร์**

### ข้อมูล API สำหรับการรับรายการไฟล์

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางโฟลเดอร์ (เช่น `/folder`) |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะใช้ |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ส่งกลับรายการไฟล์และโฟลเดอร์ย่อย |
| 400  | คำขอไม่ถูกต้อง – เส้นทางไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบโฟลเดอร์ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการรับรายการไฟล์

{{< tabs tabTotal="2" tabID="5" tabName5="คำขอ" tabName6="การตอบกลับ" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การตอบกลับจะแสดงรายการทั้งไฟล์และโฟลเดอร์ย่อยภายในเส้นทางที่ระบุ*

## **วิธีการลบโฟลเดอร์**

### ข้อมูล API สำหรับการลบโฟลเดอร์

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางโฟลเดอร์ (เช่น `/folder`) |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะใช้ |
| recursive      | boolean   | query   | ตั้งค่าเป็น `true` เพื่อลบโฟลเดอร์แบบเรียกซีฟ |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ลบโฟลเดอร์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบโฟลเดอร์ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการลบโฟลเดอร์

{{< tabs tabTotal="2" tabID="7" tabName7="คำขอ" tabName8="การตอบกลับ" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การลบโฟลเดอร์ด้วย `recursive=true` จะลบเนื้อหาทั้งหมดภายในโฟลเดอร์อย่างถาวร*

## **วิธีการคัดลอกโฟลเดอร์**

### ข้อมูล API สำหรับการคัดลอกโฟลเดอร์

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| srcPath        | string    | path    | เส้นทางโฟลเดอร์ต้นทาง (เช่น `/src`) |
| destPath       | string    | query   | เส้นทางโฟลเดอร์ปลายทาง (เช่น `/dst`) |
| srcStorageName | string    | query   | ชื่อพื้นที่จัดเก็บต้นทาง (ไม่บังคับ) |
| destStorageName| string    | query   | ชื่อพื้นที่จัดเก็บปลายทาง (ไม่บังคับ) |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | คัดลอกโฟลเดอร์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบโฟลเดอร์ต้นทาง |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการคัดลอกโฟลเดอร์

{{< tabs tabTotal="2" tabID="21" tabName21="คำขอ" tabName22="การตอบกลับ" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การดำเนินการคัดลอกจะสร้างโฟลเดอร์ใหม่ที่มีเนื้อหาเหมือนกับต้นทาง*

## **วิธีการย้ายโฟลเดอร์**

### ข้อมูล API สำหรับการย้ายโฟลเดอร์

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| srcPath        | string    | path    | เส้นทางโฟลเดอร์ต้นทาง (เช่น `/folder`) |
| destPath       | string    | query   | เส้นทางโฟลเดอร์ปลายทาง (เช่น `/dst`) |
| srcStorageName | string    | query   | ชื่อพื้นที่จัดเก็บต้นทาง (ไม่บังคับ) |
| destStorageName| string    | query   | ชื่อพื้นที่จัดเก็บปลายทาง (ไม่บังคับ) |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ย้ายโฟลเดอร์เรียบร้อยแล้ว |
| 400  | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบโฟลเดอร์ต้นทาง |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการย้ายโฟลเดอร์

{{< tabs tabTotal="2" tabID="23" tabName23="คำขอ" tabName24="การตอบกลับ" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=destfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*หมายเหตุ: การย้ายโฟลเดอร์จะรักษาโครงสร้างภายในและเวอร์ชันของไฟล์ไว้*

## **วิธีการตรวจสอบว่ามีพื้นที่จัดเก็บอยู่หรือไม่**

### ข้อมูล API สำหรับการตรวจสอบพื้นที่จัดเก็บ

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| storageName    | string    | path    | ชื่อพื้นที่จัดเก็บที่จะตรวจสอบ |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ส่งกลับข้อมูลความมีอยู่ของพื้นที่จัดเก็บ (`true` หรือ `false`) |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบพื้นที่จัดเก็บ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการตรวจสอบพื้นที่จัดเก็บ

{{< tabs tabTotal="2" tabID="33" tabName33="คำขอ" tabName34="การตอบกลับ" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **วิธีการตรวจสอบว่ามีไฟล์หรือโฟลเดอร์อยู่หรือไม่**

### ข้อมูล API สำหรับการตรวจสอบวัตถุ

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางไฟล์หรือโฟลเดอร์ (เช่น `/file.xlsx` หรือ `/folder`) |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะตรวจสอบ |
| versionId      | string    | query   | ตัวระบุเวอร์ชันไฟล์ (ไม่บังคับ) |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ส่งกลับข้อมูลความมีอยู่ |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบไฟล์หรือโฟลเดอร์ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการตรวจสอบวัตถุ

{{< tabs tabTotal="2" tabID="37" tabName37="คำขอ" tabName38="การตอบกลับ" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **วิธีการดูการใช้งานดิสก์**

### ข้อมูล API สำหรับการดูการใช้งานดิสก์

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะสอบถาม |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ส่งกลับข้อมูลการใช้งานดิสก์ |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการดูการใช้งานดิสก์

{{< tabs tabTotal="2" tabID="40" tabName40="คำขอ" tabName41="การตอบกลับ" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **วิธีการรับเวอร์ชันของไฟล์**

### ข้อมูล API สำหรับการรับเวอร์ชันของไฟล์

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

พารามิเตอร์คำขอแสดงอยู่ในตารางด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|----------------|-----------|---------|-----------|
| path           | string    | path    | เส้นทางไฟล์ (เช่น `/file.xlsx`) |
| storageName    | string    | query   | ชื่อพื้นที่จัดเก็บที่จะสอบถาม |

**การตอบกลับ HTTP**

| โค้ด | คำอธิบาย |
|------|----------|
| 200  | ส่งกลับรายการเวอร์ชันของไฟล์ |
| 401  | ไม่ได้รับอนุญาต – JWT ขาดหายหรือไม่ถูกต้อง |
| 404  | ไม่พบไฟล์ |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก ช่วยให้สามารถโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่างการรับเวอร์ชันของไฟล์

{{< tabs tabTotal="2" tabID="46" tabName46="คำขอ" tabName47="การตอบกลับ" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}