---
title: "Aspose.Cells Cloud API – แปลง ผสาน แยก และป้องกันไฟล์ Excel"
second_title: "เอกสาร"
ArticleTitle: "Aspose.Cells Cloud API – แปลง ผสาน แยก และป้องกันไฟล์ Excel"
linktitle: "ศูนย์สำหรับนักพัฒนา"
type: docs
url: /
description: "Aspose.Cells Cloud REST API ช่วยให้คุณสามารถแปลง ผสาน แยก ป้องกัน และประมวลผลสเปรดชีต Excel ได้อย่างครบถ้วน ใช้งานฟรี 150 ครั้งต่อเดือน มี SDK รองรับ 8 ภาษา"
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, การแปลงสเปรดชีต, ผสาน Excel, แยก Excel, ป้องกัน Excel, SDK สเปรดชีตบนคลาวด์, REST API, การประมวลผล Excel"
---

## Aspose.Cells Cloud APIs คืออะไร?

Aspose.Cells Cloud API คือชุดบริการสเปรดชีต/Excel ที่ทำงานบนคลาวด์ ไม่จำเป็นต้องติดตั้ง Microsoft Office หรือต้องตั้งค่าเซิร์ฟเวอร์ใดๆ — เพียงแค่ส่งคำขอ HTTP คุณก็สามารถสร้าง แก้ไข แปลง ล้างข้อมูล สร้างแผนภูมิ สร้างพีชคณิตแบบพิเศษ (pivot tables) เข้ารหัส แยก ผสาน เพิ่มลายน้ำ ใช้ลายเซ็นดิจิทัล และอื่นๆ อีกมากมาย จากภาษาโปรแกรมใดก็ได้

## ทำไมจึงควรใช้ Aspose.Cells Cloud APIs?

- สร้าง แก้ไข แปลง และวิเคราะห์สเปรดชีตบนที่เก็บข้อมูลบนคลาวด์โดยใช้บริการ Web API ของ Aspose.Cells Cloud  
- สร้าง แก้ไข แปลง และวิเคราะห์ไฟล์สเปรดชีตในเครื่องโดยใช้บริการ Web API ของ Aspose.Cells Cloud  
- รองรับรูปแบบไฟล์ 30 รูปแบบ ได้แก่ **xlsx**, **csv**, **ods**, **xlsb** เป็นต้น  
- จัดการสเปรดชีตผ่าน Aspose.Cells Cloud Web API โดยไม่จำเป็นต้องใช้ Microsoft Excel  
- แพ็กเกจฟรีมีการเรียกใช้งาน API สูงสุด 150 ครั้งต่อเดือน  
- คิดค่าใช้จ่ายตามการใช้งานจริง (pay-as-you-go)  
- **สิ่งที่ทำได้ในหนึ่งประโยค**:  
  - **แปลง XLSX เป็น PDF** → ConvertSpreadsheetToPdf  
  - **ลบช่องว่างส่วนเกินทั้งหมดในไฟล์** → TrimSpreadsheetContent  
  - **รวมไฟล์มากกว่า 10 ไฟล์เข้าเป็นรายงานเดียว** → MergeSpreadsheets  

## **วิธีใช้ Aspose.Cells Cloud APIs**

### ขั้นตอนที่ 1: **รับข้อมูลประจำตัว API**

- **[ลงทะเบียนบัญชี Aspose Cloud](https://dashboard.aspose.cloud/signup)**  
- **[รับข้อมูลประจำตัวไคลเอนต์](https://dashboard.aspose.cloud/#/applications)**  

### ขั้นตอนที่ 2: **เรียกใช้ Web APIs สำหรับสเปรดชีตผ่าน SDK (แนะนำ)**

แนะนำให้ใช้ SDK อย่างเป็นทางการเพื่อช่วยลดความซับซ้อนในการยืนยันตัวตนและจัดการคำขอ SDK จะจัดการการขอและรีเฟรชโทเค็นการเข้าถึงให้โดยอัตโนมัติ

#### **[ติดตั้ง .NET SDK (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### ตัวอย่าง: **แปลง Excel เป็น PDF โดยใช้ SDK**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### คำอธิบาย

- **Spreadsheet**: ชื่อไฟล์ Excel ที่อยู่ในที่เก็บข้อมูลท้องถิ่น  
- **Format**: รูปแบบเป้าหมาย (เช่น pdf, png, csv, json)  
- **ไฟล์ผลลัพธ์**: ไฟล์ที่ได้จะถูกบันทึกในเครื่องด้วยชื่อที่ระบุ  

## **ฟังก์ชันหลัก**

Aspose.Cells Cloud มีคุณสมบัติหลักต่อไปนี้ เพื่อตอบโจทย์ความต้องการด้านการปรับอัตโนมัติสเปรดชีตระดับองค์กร:

### **การแปลงสเปรดชีต**

- **[แปลงสเปรดชีตเป็นไฟล์ PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[แปลงแผนภูมิในสเปรดชีตเป็นรูปภาพ](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[บันทึกสเปรดชีตในรูปแบบอื่น](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **การประมวลผลข้อมูล**

- **[ผสานสเปรดชีต](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[แยกสเปรดชีต](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[ลบแถวว่างในสเปรดชีต](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[ลบคอลัมน์ว่างในสเปรดชีต](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[แทนที่เนื้อหาในสเปรดชีต](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **หมายเหตุ**: โครงสร้างคำขอ/คำตอบ วิธีการ HTTP พารามิเตอร์แบบ query และตัวอย่างคำตอบสำหรับแต่ละ endpoint สามารถดูได้ใน **เอกสารอ้างอิง Aspose.Cells Cloud Spreadsheet Web API** ซึ่งเชื่อมโยงไว้ด้านล่าง

**ตัวอย่าง endpoint แบบย่อ**

| การดำเนินการ | HTTP Method | เส้นทาง | พารามิเตอร์ที่จำเป็น | ตัวอย่างคำตอบ |
|--------------|-------------|--------|----------------------|----------------|
| แปลงสเปรดชีต | POST | `/cells/convert` | `Spreadsheet` (ไฟล์), `format` (สตริง) | ไฟล์ไบนารี (เช่น PDF) |
| ผสานสเปรดชีต | POST | `/cells/worksheets/merge` | `files` (รายการไฟล์) | สมุดงานที่ผสานแล้ว |
| แยกสเปรดชีต | POST | `/cells/worksheets/split` | `Spreadsheet` (ไฟล์), `format` (สตริง) | ไฟล์บีบอัดที่แยกแล้ว |
| ลบแถวว่าง | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (ไฟล์) | สมุดงานที่อัปเดตแล้ว |
| แทนที่เนื้อหา | POST | `/cells/replace` | `Spreadsheet` (ไฟล์), `oldValue`, `newValue` | สมุดงานที่อัปเดตแล้ว |

## SDK ที่รองรับ (**SDK ที่มีให้ใช้งาน**)

- Aspose.Cells Cloud มี [SDK](https://github.com/aspose-cells-cloud) พร้อมใช้งานในทุกภาษาหลัก — เพียงดึงโค้ดมา แก้ไข และนำไปใช้งานได้เลย:

| ภาษา | วิธีการติดตั้ง | คลัง GitHub ของ SDK |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [คลัง GitHub ของ Java SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [คลัง GitHub ของ .NET SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [คลัง GitHub ของ Python SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [คลัง GitHub ของ Node.js SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [คลัง GitHub ของ PHP SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [คลัง GitHub ของ GoLang SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [คลัง GitHub ของ Ruby SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [คลัง GitHub ของ Perl SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **API Endpoint** | [เอกสารอ้างอิง Aspose.Cells Cloud Spreadsheet Web API](https://reference.aspose.cloud/cells/) |  |

## **ตัวอย่างโค้ดและโครงการโอเพนซอร์ส**

SDK ทั้งหมดเป็นโอเพนซอร์สและมีตัวอย่างครบถ้วน:

- [ตัวอย่าง Java SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [ตัวอย่าง .NET SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [ตัวอย่าง Python SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [ตัวอย่าง Node.js SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [ตัวอย่าง PHP SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [ตัวอย่าง Go SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [ตัวอย่าง Ruby SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [ตัวอย่าง Perl SDK บน Github](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---