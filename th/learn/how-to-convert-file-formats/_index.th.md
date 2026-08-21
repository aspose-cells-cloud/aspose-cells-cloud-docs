---
---
title: "วิธีการแปลงรูปแบบไฟล์สเปรดชีตด้วย Aspose.Cells Cloud"
linktype: "วิธีการแปลงรูปแบบไฟล์สเปรดชีต"
type: docs
url: /how-to-convert-file-formats
description: "วิธีการแปลงรูปแบบไฟล์ด้วย Aspose.Cells Cloud"
weight: 10
kwords: Excel, Office Cloud, REST API, สเปรดชีต, PDF, CSV, JSON, Markdown, วิธีการแปลงรูปแบบไฟล์ผ่าน Aspose.Cells Cloud
---

## บทนำ

API สเปรดชีตของ Aspose.Cells Cloud มีอินเทอร์เฟซแบบสองช่องทางสำหรับการแปลงไฟล์สเปรดชีตที่อยู่บนเครื่องและบนคลาวด์ รองรับรูปแบบต่างๆ เช่น Excel (XLS, XLSX), CSV, HTML และ PDF ทำให้การแปลงเป็นเรื่องง่ายและตอบโจทย์ความต้องการที่หลากหลาย

### สามโหมดการแปลง · โมเดลวัตถุแบบรวม · ครอบคลุมทุกรูปแบบ

![Conversion Modes](image.png)

## **เมทริกซ์การแปลงหลัก**

| ประเภทการแปลง       | ระดับวัตถุ (Object) | API ที่ใช้บ่อย              | รูปแบบผลลัพธ์                        |
|---------------------|---------------------|----------------------------|---------------------------------------|
| **การแปลงไฟล์บนเครื่อง** | Workbook            | `ConvertSpreadsheet`       | PDF/XLSX/JSON/.... มากกว่า 30 รูปแบบ |
|                       | Worksheet           | `ConvertWorksheetToImage`  | PNG/JPEG/SVG                          |
|                       |                     | `ConvertWorksheetToPdf`    | PDF                                   |
|                       | Table               | `ConvertTableToImage`      | PNG/JPEG/SVG/....                     |
|                       |                     | `ConvertTableToPdf`        | PDF                                   |
|                       |                     | `ConvertTableToCsv`        | CSV                                   |
|                       |                     | `ConvertTableToHtml`       | HTML                                  |
|                       |                     | `ConvertTableToJson`       | JSON                                  |
|                       | Range               | `ConvertRangeToImage`      | PNG/JPEG/SVG/....                     |
|                       |                     | `ConvertRangeToPdf`        | PDF                                   |
|                       |                     | `ConvertRangeToCsv`        | CSV                                   |
|                       |                     | `ConvertRangeToHtml`       | HTML                                  |
|                       |                     | `ConvertRangeToJson`       | JSON                                  |
|                       | Chart               | `ConvertChartToImage`      | PNG/JPEG/SVG/....                     |
|                       |                     | `ConvertChartToPdf`        | PDF                                   |
| **การแปลงไฟล์บนคลาวด์** | Workbook            | `ExportSpreadsheetAsFormat`| PDF/XLSX/JSON/.... มากกว่า 30 รูปแบบ |
|                       | Worksheet           | `ExportWorksheetAsFormat`  | PDF/XLSX/JSON/.... มากกว่า 30 รูปแบบ |
|                       | Table               | `ExportTableAsFormat`      | PDF/XLSX/JSON/.... มากกว่า 30 รูปแบบ |
|                       | Range               | `ExportRangeAsFormat`      | PDF/XLSX/JSON/.... มากกว่า 30 รูปแบบ |
|                       | Chart               | `ExportChartAsFormat`      | PDF/XLSX/JSON/.... มากกว่า 30 รูปแบบ |
| **บันทึกบนคลาวด์ (Cloud Save As)** | Workbook            | `SaveSpreadsheetAs`        | PDF/XLSX/JSON/.... มากกว่า 30 รูปแบบ |

### **การแปลงไฟล์บนเครื่อง**

```csharp
// รับไคลเอนต์ API ของ Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **การแปลงไฟล์ Excel**

```c#
// แปลงไฟล์ Excel บนเครื่องเป็น PDF
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **แปลงแผนภูมิใน Excel เป็นไฟล์ SVG**

```c#
// แปลงแผนภูมิ Excel บนเครื่องเป็น SVG
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **แปลงตารางเป็นไฟล์ CSV**

```C#
// แปลงตาราง SaleLogs ในชีต Sales เป็น CSV
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **การแปลงไฟล์บนคลาวด์**

ต้องรับไคลเอนต์ API ของ Aspose Cells Cloud เช่นเดียวกัน

```csharp
// รับไคลเอนต์ API ของ Cells Cloud
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **แปลง Excel เป็น PDF**

```csharp
// แปลงไฟล์ Excel บนคลาวด์เป็น PDF และบันทึกเป็นไฟล์ในเครื่อง
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **แปลงชีตใน Excel เป็น PDF**

```csharp
// แปลงชีตในไฟล์ Excel บนคลาวด์เป็น PDF และบันทึกเป็นไฟล์ในเครื่อง
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// แปลงชีตในไฟล์ Excel บนคลาวด์เป็น PDF และบันทึกเป็นไฟล์ในเครื่อง
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## การติดตั้งและเริ่มต้นใช้งาน Aspose.Cells Cloud SDK

ติดตั้งแพ็กเกจ NuGet ของ Aspose.Cells-Cloud ในโปรเจกต์ .NET ของคุณ โดยสามารถใช้ Package Manager Console หรือ NuGet Package Manager ใน Visual Studio ได้  
นี่คือวิธีการติดตั้งแพ็กเกจผ่าน Package Manager Console:

```powershell

Install-Package Aspose.Cells-Cloud

```

สร้างอินสแตนซ์ใหม่ของคลาส CellsApi โดยเริ่มต้นด้วย Client ID และ Client Secret ของคุณ รายละเอียดของโค้ดที่กล่าวมาข้างต้นคือ:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

โปรดแทนที่ YOUR_API_KEY, YOUR_APP_SID และ YOUR_APP_KEY ด้วย API key, Application SID และ Application key ที่คุณมีจริง

## **กรณีการใช้งานการแปลงรูปแบบไฟล์**  

API ของ Aspose Cells Cloud มีความสามารถในการ **แปลงสเปรดชีต** ในระดับองค์กรสำหรับสถานการณ์ทางธุรกิจที่สำคัญ:  

1. **Excel → PDF**  
   สร้างรายงานพร้อมพิมพ์ที่รักษารูปแบบต้นฉบับไว้ครบถ้วน  
2. **สเปรดชีต → HTML**  
   ฝังตารางแบบโต้ตอบในแอปพลิเคชันเว็บ  
3. **CSV → Excel (XLSX)**  
   แปลงข้อมูลดิบให้เป็นสมุดงานที่สามารถวิเคราะห์ได้  
4. **การแปลงรูปแบบแบบกำหนดเอง**  
   แปลงระหว่างรูปแบบมากกว่า 20 แบบ (XLS, XLSB, ODS, FODS, TSV)  
![Conversion from input formats to output formats](image-1.png)

## **สรุป: ทำให้การแปลงเป็นไปอย่างราบรื่นด้วยหนึ่งคำสั่ง API**  

---