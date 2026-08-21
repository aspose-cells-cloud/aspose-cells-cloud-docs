---
title: "ตัวเลือกการแปลงสมุดงาน"
second_title: "เอกสาร"
linktitle: "ตัวเลือกการแปลงสมุดงาน"
type: docs
url: /convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, การแปลง Excel, PDF, CSV, API"
description: "ตัวเลือกการแปลงสมุดงาน – ตั้งค่าการแปลงสมุดงาน Excel เป็น PDF, CSV, HTML และรูปแบบอื่นๆ ด้วย API ของ Aspose.Cells Cloud"
weight: 79
ArticleTitle: "ตัวเลือกการแปลงสมุดงาน – API ของ Aspose.Cells Cloud"
---

# คุณสมบัติของ ConvertWorkbookOptions

**เวอร์ชัน API:** 23.12 (2024‑03)

`ConvertWorkbookOptions` เป็นโมเดลคำขอที่ใช้โดย API การแปลงของ Aspose.Cells Cloud เพื่อระบุวิธีการแปลงสมุดงาน Excel เป็นรูปแบบอื่น (เช่น PDF, CSV, HTML เป็นต้น) โดยโมเดลนี้รวมข้อมูลไฟล์ต้นทาง รูปแบบปลายทาง การตั้งค่าการตั้งค่าหน้ากระดาษ และตัวเลือกการบันทึกเฉพาะรูปแบบ

| ชื่อ                                | ประเภท        | คำอธิบาย                                                                                                   | หมายเหตุ |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | แหล่งข้อมูลไฟล์: `CloudFileSystem`, `RequestFiles` หรือ `HttpUri`                                            |       |
| **[FileInfo](/cells/file-info/)**   | **Object**  | อธิบายชื่อไฟล์ ขนาด และเนื้อหาที่เข้ารหัส base‑64                                                            |       |
| **[PageSetup](/cells/page-setup/)** | **Object**  | คุณสมบัติการตั้งค่าหน้ากระดาษ เช่น ระยะขอบ ทิศทาง และการปรับขนาด                                              |       |
| **SaveOptions**                     | **Object**  | คอนเทนเนอร์สำหรับวัตถุตัวเลือกการบันทึกเฉพาะรูปแบบ (เช่น `PdfSaveOptions`, `HtmlSaveOptions`)                |       |
| **ConvertFormat**                   | **string**  | รูปแบบไฟล์ปลายทาง (เช่น **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF** เป็นต้น)                              |       |
| **CheckExcelRestriction**           | **boolean** | รับหรือตั้งค่าการบังคับใช้ข้อจำกัดเฉพาะของ Excel (เช่น จำนวนแถวสูงสุด คอลัมน์ สูงสุด ความยาวชื่อชีตสูงสุด เป็นต้น) |       |

**ข้อกำหนดเบื้องต้น**

- ต้องได้รับโทเคนการเข้าถึง OAuth 2.0 ที่ถูกต้องสำหรับ Aspose.Cells Cloud  
- ต้องแน่ใจว่าไฟล์ต้นทางสามารถเข้าถึงได้ผ่านหนึ่งในประเภท `DataSource` ที่รองรับ

**ตัวอย่างด่วน**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<เนื้อหาที่เข้ารหัส base64>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**รายละเอียดคำขอ API**

การดำเนินการแปลงจะดำเนินการด้วยคำขอ **POST** ไปยังปลายทาง:

```
https://api.aspose.cloud/v3.0/cells/convert
```

หัวข้อที่จำเป็น:

| หัวข้อ                | ค่า                                |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

เนื้อหาคำขอต้องเป็นการแทนค่า JSON ของ `ConvertWorkbookOptions` (ดูตัวอย่างข้างต้น) คุณสมบัติทั้งหมดเป็นค่าที่ไม่บังคับเว้นแต่จะมีความจำเป็นตาม `ConvertFormat` ที่เลือก

**การตอบกลับของ API**

การแปลงที่สำเร็จจะส่งกลับ **HTTP 200 OK** (หรือ **202 Accepted** สำหรับการประมวลผลแบบไม่ประสาน) พร้อมส่งไฟล์ที่แปลงแล้วแบบสตรีมในเนื้อหาการตอบกลับ เมื่อมีการส่งกลับแบบสตรีม หัวข้อ `Content-Disposition` จะมีชื่อไฟล์ที่แนะนำ

ตัวอย่างการตอบกลับ JSON สำหรับคำขอแบบไม่ประสาน:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**โค้ดสถานะ**

| โค้ด | ความหมาย                                 |
|------|------------------------------------------|
| 200  | การแปลงเสร็จสมบูรณ์; ส่งกลับไฟล์แล้ว     |
| 202  | ยอมรับการแปลง; ผลลัพธ์พร้อมใช้งานในภายหลัง |
| 400  | คำขอไม่ถูกต้อง – ขาดหรือมีพารามิเตอร์ไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต – โทเคนไม่ถูกต้องหรือขาดหาย |
| 403  | ถูกปฏิเสธ – สิทธิ์ไม่เพียงพอ             |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์                |

**หมายเหตุ / ข้อจำกัด**

- ฟลาก `CheckExcelRestriction` บังคับใช้ข้อจำกัดของ Excel เช่น จำนวนแถวสูงสุด (1,048,576) และคอลัมน์สูงสุด (16,384)  
- ไม่ใช่ทุกรูปแบบปลายทางที่รองรับคุณสมบัติ `SaveOptions` ทุกประการ; ตัวเลือกที่ไม่รองรับจะถูกละเว้น  
- เมื่อใช้ `HttpUri` เป็นแหล่งข้อมูล ต้องสามารถเข้าถึง URL ได้แบบสาธารณะโดยไม่ต้องยืนยันตัวตน  
- ได้เพิ่มข้อมูลเมธอดและปลายทางของ API เพื่อเพิ่มความชัดเจนให้กับนักพัฒนาและลดข้อผิดพลาดในการผสานรวม  

## คุณสมบัติของ FileSource

| ชื่อคุณสมบัติ | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                                               |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | ระบุประเภทแหล่งที่มา (`CloudFileSystem`, `RequestFiles`, `HttpUri`) |
| FilePath       | String        | true     | false    |               | ตำแหน่งเส้นทางไฟล์                                                       |

## คุณสมบัติของ DbfSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | เมื่อเป็น **true** จะส่งออกค่าตัวเลขเป็นสตริง     |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ DBF                      |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว               |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                  |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน            |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ       |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก           |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร               |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน             |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้              |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                    |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง   |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์          |

## คุณสมบัติของ DifSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ DIF                      |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว               |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                  |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน            |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ       |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก           |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร               |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน             |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้              |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                    |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง   |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์          |

## คุณสมบัติของ DocxSaveOptions

| ชื่อคุณสมบัติ                    | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | แบบอักษรที่ใช้เมื่อไม่สามารถใช้แบบอักษรต้นทางได้     |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | ตรวจสอบว่าใช้แบบอักษรเริ่มต้นของสมุดงานหรือไม่       |
| CheckFontCompatibility            | Boolean       | true     | false    |               | ตรวจสอบความเข้ากันได้ของแบบอักษรสำหรับรูปแบบปลายทาง |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | ควบคุมการแทนที่แบบอักษรระดับตัวอักษร                |
| OnePagePerSheet                   | Boolean       | true     | false    |               | บังคับให้แต่ละชีตอยู่ในหน้าแยกต่างหาก             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | จัดให้คอลัมน์ทั้งหมดของชีตอยู่ในหน้าเดียว          |
| IgnoreError                       | Boolean       | true     | false    |               | ละเลยข้อผิดพลาดที่ไม่สำคัญระหว่างการแปลง          |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | สร้างหน้าว่างหากไม่มีสิ่งที่ต้องเรนเดอร์             |
| PageIndex                         | Integer       | true     | false    |               | ดัชนีของหน้าแรกที่จะส่งออก                        |
| PageCount                         | Integer       | true     | false    |               | จำนวนหน้าที่จะส่งออก                               |
| PrintingPageType                  | String        | true     | false    |               | ระบุประเภทหน้าสำหรับการพิมพ์                        |
| GridlineType                      | String        | true     | false    |               | ระบุวิธีการเรนเดอร์เส้นตาราง                        |
| TextCrossType                     | String        | true     | false    |               | กำหนดประเภทการข้ามสำหรับการเรนเดอร์ข้อความ         |
| DefaultEditLanguage               | String        | true     | false    |               | ภาษาเริ่มต้นสำหรับการแก้ไขข้อความ                   |
| EmfRenderSetting                  | String        | true     | false    |               | การตั้งค่าสำหรับการเรนเดอร์ EMF                     |
| MergeAreas                        | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้               |
| SortExternalNames                 | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                     |
| UpdateSmartArt                    | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด            |
| SaveFormat                        | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ DOCX                       |
| CachedFileFolder                  | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                |
| ClearData                         | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                   |
| CreateDirectory                   | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน             |
| EnableHttpCompression             | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ         |
| RefreshChartCache                 | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก             |
| SortNames                         | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                |
| ValidateMergedAreas               | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง     |
| EncryptDocumentProperties          | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์            |

## คุณสมบัติของ HtmlSaveOptions

| ชื่อคุณสมบัติ                   | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | รวมส่วนหัวหน้าในผลลัพธ์ HTML                       |
| ExportPageFooters               | Boolean       | true     | false    |               | รวมส่วนท้ายหน้าในผลลัพธ์ HTML                       |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | ส่งออกส่วนหัวแถวและคอลัมน์                          |
| ShowAllSheets                   | Boolean       | true     | false    |               | แสดงชีตทั้งหมดในไฟล์ HTML เดียว                     |
| ImageOptions                    | Class         | true     | false    |               | การตั้งค่าที่ควบคุมการเรนเดอร์ภาพ                   |
| SaveAsSingleFile                | Boolean       | true     | false    |               | บันทึกสมุดงานทั้งหมดเป็นไฟล์ HTML เดียว             |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | รวมชีตที่ซ่อนอยู่ในการส่งออก                        |
| ExportGridLines                 | Boolean       | true     | false    |               | เรนเดอร์เส้นตารางในผลลัพธ์ HTML                     |
| PresentationPreference          | Boolean       | true     | false    |               | ปรับแต่ง HTML ให้เหมาะสมสำหรับโหมดพรีเซนเทชัน      |
| CellCssPrefix                   | String        | true     | false    |               | คำนำหน้าที่เพิ่มลงในชื่อคลาส CSS ที่สร้างสำหรับเซลล์ |
| TableCssId                      | String        | true     | false    |               | แอตทริบิวต์ ID สำหรับตาราง HTML ที่สร้างขึ้น         |
| IsFullPathLink                  | Boolean       | true     | false    |               | สร้างลิงก์แบบเต็มเส้นทางสำหรับทรัพยากร              |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | ใส่ CSS ของแต่ละชีตในไฟล์แยกต่างหาก                 |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | รวมสไตล์เส้นขอบที่คล้ายกันเพื่อลดขนาด CSS          |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | บังคับผสานองค์ประกอบ `<td>` ที่ว่างเปล่า            |
| ExportCellCoordinate            | Boolean       | true     | false    |               | รวมพิกัดเซลล์ (เช่น A1) ใน HTML                     |
| ExportExtraHeadings             | Boolean       | true     | false    |               | เพิ่มแถว/คอลัมน์ส่วนหัวพิเศษเมื่อจำเป็น              |
| ExportHeadings                  | Boolean       | true     | false    |               | ส่งออกส่วนหัวแถวและคอลัมน์                          |
| ExportFormula                   | Boolean       | true     | false    |               | แสดงสูตรแทนค่าที่คำนวณแล้ว                          |
| AddTooltipText                  | Boolean       | true     | false    |               | เพิ่มข้อความคำอธิบายประกอบด้วยคำอธิบายของเซลล์     |
| ExportBogusRowData              | Boolean       | true     | false    |               | รวมแถวตัวอย่างสำหรับข้อมูลที่ว่างเปล่า               |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | ลบสไตล์ CSS ที่ไม่ได้ใช้                            |
| ExportDocumentProperties        | Boolean       | true     | false    |               | เขียนคุณสมบัติระดับเอกสารลงในแท็กเมตา HTML         |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | เขียนคุณสมบัติระดับชีตลงใน HTML                     |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | เขียนคุณสมบัติระดับสมุดงานลงใน HTML                 |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | รวมสคริปต์และคุณสมบัติสำหรับเฟรม                    |
| AttachedFilesDirectory          | String        | true     | false    |               | เส้นทางไดเรกทอรีสำหรับไฟล์ที่แนบมา                  |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | คำนำหน้า URL สำหรับไฟล์ที่แนบมา                     |
| Encoding                        | String        | true     | false    |               | การเข้ารหัสอักขระสำหรับไฟล์ HTML                    |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | ส่งออกเฉพาะชีตที่ใช้งานอยู่                         |
| ExportChartImageFormat          | String        | true     | false    |               | รูปแบบภาพที่ใช้สำหรับแผนภูมิที่ฝังตัว                |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | เข้ารหัสภาพเป็นสตริง Base64                          |
| HiddenColDisplayType            | String        | true     | false    |               | วิธีการแสดงคอลัมน์ที่ซ่อนอยู่                        |
| HiddenRowDisplayType            | String        | true     | false    |               | วิธีการแสดงแถวที่ซ่อนอยู่                             |
| HtmlCrossStringType             | String        | true     | false    |               | กำหนดวิธีการเรนเดอร์ข้อมูลข้ามสตริง                  |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | ส่งออกภาพไปยังไดเรกทอรีชั่วคราว                     |
| PageTitle                       | String        | true     | false    |               | ชื่อที่ใช้สำหรับหน้า HTML ที่สร้างขึ้น                |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | แยกวิเคราะห์แท็ก HTML ที่มีอยู่ในค่าเซลล์           |
| CellNameAttribute               | String        | true     | false    |               | ชื่อแอตทริบิวต์ที่เก็บการอ้างอิงเซลล์               |
| SaveFormat                      | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ HTML                        |
| CachedFileFolder                | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                  |
| ClearData                       | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                     |
| CreateDirectory                 | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน              |
| EnableHttpCompression           | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ          |
| RefreshChartCache               | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก              |
| SortNames                       | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                 |
| ValidateMergedAreas             | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน               |
| MergeAreas                      | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                |
| SortExternalNames               | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                      |
| CheckExcelRestriction           | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง      |
| UpdateSmartArt                  | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด             |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์             |

## คุณสมบัติของ ImageSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | รูปแบบภาพที่ใช้สำหรับการเรนเดอร์แผนภูมิ          |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | ชื่อที่กำหนดให้กับภาพที่ฝังตัวในผลลัพธ์ SVG      |
| HorizontalResolution      | Integer       | true     | false    |               | DPI แนวนอนของภาพที่ส่งออก                        |
| ImageFormat               | String        | true     | false    |               | รูปแบบภาพปลายทาง (PNG, JPG เป็นต้น)              |
| IsCellAutoFit             | Boolean       | true     | false    |               | ปรับเนื้อหาเซลล์ให้พอดีกับขนาดภาพ                 |
| OnePagePerSheet           | Boolean       | true     | false    |               | เรนเดอร์แต่ละชีตในหน้าแยกต่างหาก                  |
| OnlyArea                  | Boolean       | true     | false    |               | ส่งออกเฉพาะพื้นที่ที่กำหนดของชีต                  |
| PrintingPage              | String        | true     | false    |               | โครงร่างหน้าที่ใช้สำหรับการพิมพ์                   |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | แสดงกล่องโต้ตอบสถานะระหว่างการพิมพ์              |
| Quality                   | Integer       | true     | false    |               | คุณภาพการบีบอัดสำหรับภาพ JPEG (0‑100)            |
| TiffCompression           | String        | true     | false    |               | ประเภทการบีบอัดสำหรับภาพ TIFF                     |
| VerticalResolution        | Integer       | true     | false    |               | DPI แนวตั้งของภาพที่ส่งออก                        |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ภาพ                         |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                  |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน            |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ       |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก           |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร               |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน             |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้              |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                    |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง   |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์          |

## คุณสมบัติของ JsonSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Class         | true     | false    |               | กำหนดพื้นที่ชีตที่จะส่งออก                             |
| HasHeaderRow              | Boolean       | true     | false    |               | ระบุว่าแถวแรกมีส่วนหัวคอลัมน์หรือไม่                   |
| ExportAsString            | Boolean       | true     | false    |               | ส่งออกค่าทั้งหมดเป็นสตริง                               |
| Indent                    | String        | true     | false    |               | สตริงที่ใช้สำหรับการเยื้อง (เช่น ช่องว่างสองช่อง)        |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ JSON                           |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                    |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                       |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน                 |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ             |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก                 |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                    |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน                  |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                   |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง         |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด                |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์                |

## คุณสมบัติของ MarkdownSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | การเข้ารหัสอักขระสำหรับไฟล์ markdown                        |
| FormatStrategy            | String        | true     | false    |               | กลยุทธ์ที่ใช้ในการจัดรูปแบบ markdown (เช่น GitHub, CommonMark) |
| LineSeparator             | String        | true     | false    |               | อักขระหรือชุดอักขระที่ใช้สำหรับขึ้นบรรทัดใหม่                |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ markdown                            |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                          |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                            |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ                 |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก                     |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                        |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน                      |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                       |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง            |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด                   |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์                   |

## คุณสมบัติของ OoxmlSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | รวมชื่อเซลล์ในไฟล์ที่ส่งออก                       |
| UpdateZoom                | Boolean       | true     | false    |               | อัปเดตระดับการซูมในเอกสารผลลัพธ์                  |
| EnableZip64               | Boolean       | true     | false    |               | เปิดใช้งานส่วนขยาย ZIP64 สำหรับไฟล์ขนาดใหญ่       |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | ฝัง OOXML เป็นวัตถุ OLE                           |
| CompressionType           | String        | true     | false    |               | ประเภทการบีบอัดที่ใช้ (เช่น Normal, Maximum)       |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ OOXML                      |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                  |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน            |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ       |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก           |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร               |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน             |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้              |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                    |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง   |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์          |

## คุณสมบัติของ PclSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | ชื่อเต็มของแบบอักษรที่จะใช้                      |
| fontPclName               | String        | true     | false    |               | ชื่อแบบอักษรเฉพาะ PCL                            |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ PCL                       |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว              |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                 |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน          |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ      |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก          |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร             |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน           |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้            |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                  |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์         |

## คุณสมบัติของ PDFSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | ใช้ชื่อเอกสารเป็นชื่อ PDF                           |
| ExportDocumentStructure   | Boolean       | true     | false    |               | รักษาโครงสร้างเชิงตรรกะของเอกสารไว้                |
| EmfRenderSetting          | String        | true     | false    |               | การตั้งค่าสำหรับการเรนเดอร์ภาพ EMF                 |
| CustomPropertiesExport    | String        | true     | false    |               | ควบคุมการส่งออกคุณสมบัติเอกสารที่กำหนดเอง         |
| OptimizationType          | String        | true     | false    |               | ประเภทการปรับแต่ง PDF (เช่น Size, Speed)           |
| Producer                  | String        | true     | false    |               | ชื่อแอปพลิเคชันผู้ผลิต PDF                         |
| PDFCompression            | String        | true     | false    |               | อัลกอริทึมการบีบอัดสำหรับสตรีม PDF                  |
| FontEncoding              | String        | true     | false    |               | การเข้ารหัสที่ใช้สำหรับแบบอักษรที่ฝังตัว             |
| Watermark                 | Class         | true     | false    |               | การตั้งค่าน้ำเครื่องหมายที่ใช้กับ PDF               |
| CalculateFormula          | Boolean       | true     | false    |               | คำนวณสูตรก่อนการส่งออก                             |
| CheckFontCompatibility    | Boolean       | true     | false    |               | ตรวจสอบความเข้ากันได้ของแบบอักษรสำหรับการเรนเดอร์ PDF |
| Compliance                | String        | true     | false    |               | ระดับความสอดคล้องของ PDF/A หรือ PDF/X             |
| DefaultFont               | String        | true     | false    |               | แบบอักษรที่ใช้เมื่อไม่สามารถใช้แบบอักษรต้นทางได้     |
| OnePagePerSheet           | Boolean       | true     | false    |               | วางแต่ละชีตในหน้า PDF แยกต่างหาก                  |
| PrintingPageType          | String        | true     | false    |               | ระบุประเภทหน้าสำหรับการพิมพ์                        |
| SecurityOptions           | Class         | true     | false    |               | การตั้งค่าความปลอดภัย เช่น รหัสผ่านและสิทธิ์         |
| desiredPPI                | Integer       | true     | false    |               | ความละเอียดพิกเซลต่อนิ้วที่ต้องการ                 |
| jpegQuality               | Integer       | true     | false    |               | คุณภาพภาพ JPEG (0‑100)                             |
| ImageType                 | String        | true     | false    |               | ประเภทภาพที่ใช้สำหรับการเรนเดอร์แบบเรียงซ้อน        |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ PDF                         |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                  |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน            |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ       |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก           |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร               |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน             |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้              |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                    |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง   |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์          |

## คุณสมบัติของ PptxSaveOptions

| ชื่อคุณสมบัติ                    | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | ข้ามแถวที่ซ่อนอยู่ระหว่างการส่งออก                  |
| AdjustFontSizeForRowType          | String        | true     | false    |               | ควบคุมการปรับขนาดตัวอักษรตามประเภทแถว               |
| ExportViewType                    | String        | true     | false    |               | กำหนดมุมมองที่จะส่งออก (สไลด์, โน้ต)                |
| DefaultFont                       | String        | true     | false    |               | แบบอักษรที่ใช้เมื่อไม่สามารถใช้แบบอักษรต้นทางได้      |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | ตรวจสอบว่าใช้แบบอักษรเริ่มต้นของสมุดงานหรือไม่        |
| CheckFontCompatibility            | Boolean       | true     | false    |               | ตรวจสอบความเข้ากันได้ของแบบอักษรสำหรับรูปแบบปลายทาง |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | ควบคุมการแทนที่แบบอักษรระดับตัวอักษร                 |
| OnePagePerSheet                   | Boolean       | true     | false    |               | วางแต่ละชีตในสไลด์แยกต่างหาก                         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | จัดให้คอลัมน์ทั้งหมดของชีตอยู่ในสไลด์เดียว          |
| IgnoreError                       | Boolean       | true     | false    |               | ละเลยข้อผิดพลาดที่ไม่สำคัญระหว่างการแปลง           |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | สร้างสไลด์ว่างหากไม่มีสิ่งที่ต้องเรนเดอร์             |
| PageIndex                         | Integer       | true     | false    |               | ดัชนีของสไลด์แรกที่จะส่งออก                         |
| PageCount                         | Integer       | true     | false    |               | จำนวนสไลด์ที่จะส่งออก                                |
| PrintingPageType                  | String        | true     | false    |               | ระบุประเภทหน้าสำหรับการพิมพ์                         |
| GridlineType                      | String        | true     | false    |               | ระบุวิธีการเรนเดอร์เส้นตาราง                         |
| TextCrossType                     | String        | true     | false    |               | กำหนดประเภทการข้ามสำหรับการเรนเดอร์ข้อความ          |
| DefaultEditLanguage               | String        | true     | false    |               | ภาษาเริ่มต้นสำหรับการแก้ไขข้อความ                    |
| EmfRenderSetting                  | String        | true     | false    |               | การตั้งค่าสำหรับการเรนเดอร์ EMF                      |
| MergeAreas                        | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                |
| SortExternalNames                 | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด            |
| SaveFormat                        | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ PPTX                         |
| CachedFileFolder                  | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                 |
| ClearData                         | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                    |
| CreateDirectory                   | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน             |
| EnableHttpCompression             | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ         |
| RefreshChartCache                 | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก            |
| SortNames                         | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                |
| ValidateMergedAreas               | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์            |

## คุณสมบัติของ SqlScriptSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | ตรวจสอบว่าตารางปลายทางมีอยู่แล้วหรือไม่                |
| ColumnTypeMap             | String        | true     | false    |               | การแมปชื่อคอลัมน์ไปยังประเภทข้อมูล SQL                 |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | สแกนแถวทั้งหมดเพื่ออนุมานประเภทคอลัมน์                  |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | แทรกบรรทัดว่างระหว่างแถวที่สร้างขึ้น                     |
| Separator                 | String        | true     | false    |               | อักขระที่ใช้แยกคอลัมน์ (เช่น คอมมา แท็บ)                |
| OperatorType              | String        | true     | false    |               | ตัวดำเนินการ SQL ที่ใช้ (INSERT, UPDATE เป็นต้น)        |
| PrimaryKey                | Integer       | true     | false    |               | ดัชนีคอลัมน์ที่ทำหน้าที่เป็นคีย์หลัก                   |
| CreateTable               | Boolean       | true     | false    |               | สร้างคำสั่ง CREATE TABLE                                 |
| IdName                    | String        | true     | false    |               | ชื่อคอลัมน์ตัวระบุ                                       |
| StartId                   | Integer       | true     | false    |               | ค่าเริ่มต้นสำหรับ ID ที่เพิ่มขึ้นอัตโนมัติ               |
| TableName                 | String        | true     | false    |               | ชื่อตารางฐานข้อมูลปลายทาง                               |
| ExportAsString            | Boolean       | true     | false    |               | ส่งออกค่าทั้งหมดเป็นสตริง                                |
| ExportArea                | Class         | true     | false    |               | กำหนดพื้นที่ชีตที่จะส่งออก                              |
| HasHeaderRow              | Boolean       | true     | false    |               | ระบุว่าแถวแรกมีส่วนหัวคอลัมน์หรือไม่                    |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์สคริปต์ SQL                       |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                      |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                        |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน                  |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ              |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก                  |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                     |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน                   |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                    |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                          |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง         |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด                 |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์                 |

## คุณสมบัติของ SvgSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | ดัชนีของชีตที่จะส่งออก                           |
| ChartImageType            | String        | true     | false    |               | รูปแบบภาพที่ใช้สำหรับการเรนเดอร์แผนภูมิ          |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | ชื่อที่กำหนดให้กับภาพที่ฝังตัวในผลลัพธ์ SVG      |
| HorizontalResolution      | Integer       | true     | false    |               | DPI แนวนอนของ SVG ที่ส่งออก                       |
| ImageFormat               | String        | true     | false    |               | รูปแบบภาพปลายทางสำหรับองค์ประกอบแบบเรียงซ้อน    |
| IsCellAutoFit             | Boolean       | true     | false    |               | ปรับเนื้อหาเซลล์ให้พอดีกับขนาด SVG               |
| OnePagePerSheet           | Boolean       | true     | false    |               | เรนเดอร์แต่ละชีตในหน้า SVG แยกต่างหาก            |
| OnlyArea                  | Boolean       | true     | false    |               | ส่งออกเฉพาะพื้นที่ที่กำหนดของชีต                  |
| PrintingPage              | String        | true     | false    |               | โครงร่างหน้าที่ใช้สำหรับการพิมพ์                   |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | แสดงกล่องโต้ตอบสถานะระหว่างการพิมพ์              |
| Quality                   | Integer       | true     | false    |               | คุณภาพการบีบอัดสำหรับภาพแบบเรียงซ้อน              |
| TiffCompression           | String        | true     | false    |               | ประเภทการบีบอัดสำหรับภาพ TIFF ที่ฝังใน SVG        |
| VerticalResolution        | Integer       | true     | false    |               | DPI แนวตั้งของ SVG ที่ส่งออก                       |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ SVG                        |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                  |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน            |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ       |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก           |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร               |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน             |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้              |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                    |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง   |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์          |

## คุณสมบัติของ TxtSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | ประเภทการอ้างอิงที่ใช้ (เช่น สองอัญประกาศเดี่ยว)                       |
| Separator                 | String        | true     | false    |               | อักขระตัวคั่นคอลัมน์ (เช่น คอมมา แท็บ)                               |
| SeparatorString           | String        | true     | false    |               | สตริงทั้งหมดที่ใช้เป็นตัวคั่นเมื่อต้องการมากกว่าหนึ่งอักขระ           |
| AlwaysQuoted              | Boolean       | true     | false    |               | บังคับให้ทุกฟิลด์อยู่ในเครื่องหมายอ้างอิง                           |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ TXT                                           |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                                   |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                                      |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน                                |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ                           |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก                               |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน                                |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                                 |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                                       |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง                      |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด                              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์                             |

## คุณสมบัติของ XlsSaveOptions และ XlsbSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | รักษาสีเซลล์ที่แม่นยำระหว่างการส่งออก          |
| WpsCompatibility          | Boolean       | true     | false    |               | เปิดใช้งานความเข้ากันได้กับ WPS Office          |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ XLS/XLSB                  |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว              |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                 |
| CreateDirectory           | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน          |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ      |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก          |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร             |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน           |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้            |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                  |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์         |

## คุณสมบัติของ XmlSaveOptions

| ชื่อคุณสมบัติ            | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Array         | true     | false    |               | รายการดัชนีของชีตที่จะรวมในการส่งออก                  |
| ExportArea                | Class         | true     | false    |               | กำหนดพื้นที่ชีตที่จะส่งออก                             |
| HasHeaderRow              | Boolean       | true     | false    |               | ระบุว่าแถวแรกมีส่วนหัวคอลัมน์หรือไม่                   |
| XmlMapName                | String        | true     | false    |               | ชื่อของแผนที่ XML ที่ใช้กับชีต                          |
| SheetNameAsElementName    | Boolean       | true     | false    |               | ใช้ชื่อชีตเป็นชื่อองค์ประกอบ XML                        |
| DataAsAttribute           | Boolean       | true     | false    |               | ส่งออกข้อมูลเซลล์เป็นแอตทริบิวต์ XML แทนองค์ประกอบ   |
| SaveFormat                | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ XML                             |
| CachedFileFolder          | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                     |
| ClearData                 | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                       |
| CreateDirectory           | String        | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน                 |
| EnableHttpCompression     | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ             |
| RefreshChartCache         | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก                 |
| SortNames                 | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                    |
| ValidateMergedAreas       | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน                  |
| MergeAreas                | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                   |
| SortExternalNames         | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง         |
| UpdateSmartArt            | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด                |
| EncryptDocumentProperties | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์                |

## คุณสมบัติของ XpsSaveOptions

| ชื่อคุณสมบัติ                    | ประเภทคุณสมบัติ | ค่า null ได้ | อ่านอย่างเดียว | ค่าเริ่มต้น | คำอธิบาย                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | แบบอักษรที่ใช้เมื่อไม่สามารถใช้แบบอักษรต้นทางได้     |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | ตรวจสอบว่าใช้แบบอักษรเริ่มต้นของสมุดงานหรือไม่       |
| CheckFontCompatibility            | Boolean       | true     | false    |               | ตรวจสอบความเข้ากันได้ของแบบอักษรสำหรับรูปแบบปลายทาง |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | ควบคุมการแทนที่แบบอักษรระดับตัวอักษร                |
| OnePagePerSheet                   | Boolean       | true     | false    |               | วางแต่ละชีตในหน้า XPS แยกต่างหาก                    |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | จัดให้คอลัมน์ทั้งหมดของชีตอยู่ในหน้าเดียว           |
| IgnoreError                       | Boolean       | true     | false    |               | ละเลยข้อผิดพลาดที่ไม่สำคัญระหว่างการแปลง           |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | สร้างหน้าว่างหากไม่มีสิ่งที่ต้องเรนเดอร์             |
| PageIndex                         | Integer       | true     | false    |               | ดัชนีของหน้าแรกที่จะส่งออก                          |
| PageCount                         | Integer       | true     | false    |               | จำนวนหน้าที่จะส่งออก                                 |
| PrintingPageType                  | String        | true     | false    |               | ระบุประเภทหน้าสำหรับการพิมพ์                          |
| GridlineType                      | String        | true     | false    |               | ระบุวิธีการเรนเดอร์เส้นตาราง                          |
| TextCrossType                     | String        | true     | false    |               | กำหนดประเภทการข้ามสำหรับการเรนเดอร์ข้อความ           |
| DefaultEditLanguage               | String        | true     | false    |               | ภาษาเริ่มต้นสำหรับการแก้ไขข้อความ                     |
| EmfRenderSetting                  | String        | true     | false    |               | การตั้งค่าสำหรับการเรนเดอร์ EMF                       |
| MergeAreas                        | Boolean       | true     | false    |               | ผสานเซลล์ที่อยู่ติดกันเมื่อเป็นไปได้                 |
| SortExternalNames                 | Boolean       | true     | false    |               | เรียงลำดับการอ้างอิงชื่อภายนอก                        |
| UpdateSmartArt                    | Boolean       | true     | false    |               | อัปเดตวัตถุ SmartArt เป็นเวอร์ชันล่าสุด              |
| SaveFormat                        | String        | true     | false    |               | ตัวระบุรูปแบบสำหรับไฟล์ XPS                            |
| CachedFileFolder                  | String        | true     | false    |               | โฟลเดอร์ที่ใช้สำหรับไฟล์แคชชั่วคราว                   |
| ClearData                         | Boolean       | true     | false    |               | ล้างข้อมูลที่มีอยู่ก่อนการบันทึก                     |
| CreateDirectory                   | Boolean       | true     | false    |               | สร้างไดเรกทอรีปลายทางหากไม่มีอยู่ก่อน               |
| EnableHttpCompression             | Boolean       | true     | false    |               | เปิดใช้งานการบีบอัด HTTP สำหรับการตอบกลับ           |
| RefreshChartCache                 | Boolean       | true     | false    |               | รีเฟรชข้อมูลแคชของแผนภูมิก่อนการบันทึก              |
| SortNames                         | Boolean       | true     | false    |               | เรียงลำดับช่วงที่ตั้งชื่อตามตัวอักษร                 |
| ValidateMergedAreas               | Boolean       | true     | false    |               | ตรวจสอบความถูกต้องของเซลล์ที่ผสานกัน               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | บังคับใช้ข้อจำกัดเฉพาะของ Excel ระหว่างการแปลง      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | เข้ารหัสคุณสมบัติของเอกสารในไฟล์ผลลัพธ์             |