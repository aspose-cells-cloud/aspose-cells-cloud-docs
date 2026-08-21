---
title: "วิธีการรวมไฟล์สเปรดชีตหลายไฟล์ด้วย Aspose.Cells Cloud"
linktype: "วิธีการรวมไฟล์สเปรดชีตหลายไฟล์"
type: docs
url: /th/how-to-merge-multiple-files
description: "วิธีการรวมไฟล์สเปรดชีตหลายไฟล์ด้วย Aspose.Cells Cloud"
weight: 10
kwords: Excel, Office Cloud, REST API, สเปรดชีต, PDF, CSV, JSON, Markdown, วิธีการรวมไฟล์หลายไฟล์ผ่าน Aspose.Cells Cloud
---

## บทนำ

API ของ Aspose.Cells Cloud เป็นโซลูชันบนคลาวด์ที่ทรงพลังซึ่งถูกออกแบบมาเพื่อสร้าง แก้ไข และแปลงไฟล์สเปรดชีต ในบทความนี้ เราจะแนะนำขั้นตอนการใช้ Aspose.Cells Cloud API เพื่อรวมไฟล์ในรูปแบบต่างๆ รวมถึงกรณีการใช้งานทั่วไปและตัวอย่างโค้ด

## ภาพรวม

Aspose.Cells Cloud API มี API ที่มีประสิทธิภาพสำหรับการรวมไฟล์สเปรดชีตหลายไฟล์ให้เป็นไฟล์เดียวในรูปแบบต่างๆ รูปแบบที่รองรับ ได้แก่ **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF** และอื่นๆ อีกมากมาย ด้วยการใช้ Aspose.Cells Cloud API คุณสามารถรวมไฟล์สเปรดชีตหลายไฟล์ให้เป็นไฟล์เดียวในรูปแบบที่นิยมใช้กันอย่างกว้างขวาง เพื่อตอบโจทย์ความต้องการที่หลากหลาย

มี API หลายตัวที่ใช้สำหรับการรวมไฟล์ โดยทั่วไปแล้วสามารถใช้งานได้กับสภาพแวดล้อมออนไลน์ต่างๆ ด้านล่างนี้คือคำอธิบายโดยละเอียดของ API เหล่านี้:

| ฟังก์ชัน | คำอธิบาย | อ้างอิง API |
| :------------------------- | :------------------------- | :------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | รวมไฟล์สเปรดชีตในเครื่องให้เป็นไฟล์ในรูปแบบที่ระบุ | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | รวมไฟล์สเปรดชีตในโฟลเดอร์ของพื้นที่จัดเก็บบนคลาวด์ให้เป็นไฟล์ในรูปแบบที่ระบุ | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | รวมไฟล์สเปรดชีตในโฟลเดอร์ของพื้นที่จัดเก็บบนคลาวด์ให้เป็นไฟล์ในรูปแบบที่ระบุ | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# วิธีการรวมไฟล์หลายไฟล์ให้เป็นไฟล์เดียวผ่าน Aspose.Cells Cloud

Aspose.Cells Cloud API มี [SDK ให้เลือกใช้หลายตัว](https://github.com/aspose-cells-cloud) สำหรับภาษาโปรแกรมต่างๆ เลือก SDK ที่ตรงกับภาษาโปรแกรมที่คุณต้องการใช้งาน และทำตามเอกสารประกอบที่ให้มาเพื่อการติดตั้งและเริ่มต้นใช้งาน หรือคุณสามารถสร้าง SDK ของคุณเองตาม [API reference](https://reference.aspose.cloud/cells/) ได้เช่นกัน ในส่วนนี้ เราจะใช้ C# เป็นตัวอย่างเพื่ออธิบายขั้นตอนการรวมไฟล์โดยละเอียด

## การลงทะเบียนและรับคีย์ API

ก่อนเริ่มต้นใช้งาน คุณจำเป็นต้อง [ลงทะเบียนบัญชี Aspose Cloud](https://id.containerize.com/signup) และ [รับคีย์ API เพื่อใช้ในการยืนยันตัวตน](https://dashboard.aspose.cloud/applications) โดยการเข้าสู่ระบบเว็บไซต์ทางการของ Aspose Cloud คุณสามารถสร้างบัญชีฟรีและรับคีย์ API เพื่อใช้ในการยืนยันตัวตน

สำหรับการดำเนินการขั้นสูงเพิ่มเติม โปรดดูเอกสารต่อไปนี้: [เริ่มต้นใช้งาน Cells Cloud อย่างรวดเร็ว](https://docs.aspose.cloud/cells/quickstart/)

## การติดตั้งและเริ่มต้นใช้งาน Aspose.Cells Cloud SDK

ติดตั้งแพ็กเกจ Aspose.Cells-Cloud ลงในโปรเจกต์ .NET ของคุณ โดยคุณสามารถใช้ NuGet Package Manager Console หรือ NuGet Package Manager ใน Visual Studio ได้  
ต่อไปนี้คือวิธีการติดตั้งแพ็กเกจผ่าน Package Manager Console:

```Powershell

Install-Package Aspose.Cells-Cloud

```

สร้างอินสแตนซ์ใหม่ของคลาส CellsApi และเริ่มต้นค่าด้วย client ID และ client secret ของคุณ โดยรายละเอียดของโค้ด snippet ดังกล่าวมีดังนี้:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

โปรดตรวจสอบให้แน่ใจว่าได้แทนที่ YOUR_API_KEY, YOUR_APP_SID, และ YOUR_APP_KEY ด้วย API key, application SID และ application key ของคุณจริงๆ

## การสร้างคำขอ API และเรียกใช้งาน API

### ใช้บริการคลาวด์เพื่อรวมสเปรดชีตในเครื่องและส่งออกไฟล์ที่รวมแล้วในรูปแบบที่ต้องการ ไม่ว่าจะเป็นการบันทึกเป็นไฟล์ในเครื่องหรือส่งออกเป็นสตรีมในหน่วยความจำ

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// สร้างคำขอรวมสเปรดชีต
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// กำหนดไฟล์ที่ต้องการรวม
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// กำหนดรูปแบบผลลัพธ์
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### รวมสเปรดชีตที่จัดเก็บในคลาวด์ผ่านบริการคลาวด์ และส่งออกไฟล์ที่รวมแล้ว ไม่ว่าจะเป็นการบันทึกเป็นไฟล์ในเครื่องหรือส่งกลับไปยังพื้นที่จัดเก็บบนคลาวด์ ในรูปแบบที่ต้องการ

```C#
// รับ Client ID และ Client Secret จาก https://dashboard.aspose.cloud (จำเป็นต้องลงทะเบียนฟรี)
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// สร้างพารามิเตอร์สำหรับคำขอรวม
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// กำหนดไฟล์หลักในคลาวด์
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// กำหนดไฟล์ที่จะรวมเข้าไป
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### รวมไฟล์ที่ตรงกับเงื่อนไขในไดเรกทอรีบนคลาวด์โดยอัตโนมัติ ส่งออกผลลัพธ์ที่รวมแล้วในรูปแบบที่กำหนด และส่งออกเป็นไฟล์ในเครื่องหรือส่งกลับไปยังพื้นที่จัดเก็บบนคลาวด์

```csharp
// รับ Client ID และ Client Secret จาก https://dashboard.aspose.cloud (จำเป็นต้องลงทะเบียนฟรี)
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// สร้างพารามิเตอร์สำหรับคำขอรวม
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// ไดเรกทอรีในคลาวด์ที่ต้องการรวมไฟล์
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## กรณีการใช้งาน

คุณสมบัติการรวมไฟล์หลายไฟล์ของ Aspose.Cells Cloud API สามารถประยุกต์ใช้ได้ในกรณีการใช้งานจริงที่หลากหลาย ต่อไปนี้คือสถานการณ์ที่พบบ่อย:

- **รวมไฟล์ Excel หลายไฟล์ให้เป็นไฟล์ Excel** เพื่อการวิเคราะห์และจัดเก็บข้อมูล
- **รวมไฟล์ข้อมูลหลายไฟล์ให้เป็นไฟล์ Excel** เพื่อการวิเคราะห์ข้อมูล
- **รวมไฟล์รูปภาพหลายไฟล์ให้เป็นไฟล์ PDF** เพื่อการแชร์อย่างง่ายดาย
- **รวมไฟล์หลายไฟล์ให้เป็นไฟล์ HTML** เพื่อการแสดงผลและการฝังในหน้าเว็บ

## บทสรุป

ด้วย Aspose.Cells Cloud API คุณสามารถรวมไฟล์สเปรดชีตหลายไฟล์ให้เป็นไฟล์เดียวได้อย่างง่ายดาย โดยการเรียกใช้งาน API อย่างง่ายและตั้งค่าตัวเลือกการรวมที่เหมาะสม คุณสามารถตอบสนองความต้องการการรวมไฟล์ต่างๆ ได้อย่างมีประสิทธิภาพ ผสานรวม Aspose.Cells Cloud API เข้ากับแอปพลิเคชันของคุณเพื่อเพิ่มประสิทธิภาพการทำงานและประหยัดเวลาในการพัฒนา

โปรดหมายเหตุว่าตัวอย่างโค้ดข้างต้นมีไว้เพื่อการอธิบายเท่านั้น และคุณจำเป็นต้องแทนที่ด้วยข้อมูลรับรองการยืนยันตัวตนที่ถูกต้องและเส้นทางไฟล์จริงเมื่อนำไปใช้งานจริง ยิ่งไปกว่านั้น Aspose.Cells Cloud API ยังมีคุณสมบัติอื่นๆ อีกมากมาย เช่น การสร้าง การแก้ไข การจัดการ และการประมวลผลข้อมูลสเปรดชีต เอกสารประกอบ API และตัวอย่างโค้ดโดยละเอียดสามารถดูได้ที่ [คู่มือนักพัฒนาของเว็บไซต์ทางการ Aspose](/developer-guide/)

เราหวังว่าบทความนี้จะช่วยให้คุณเข้าใจวิธีการใช้ Aspose.Cells Cloud API สำหรับการรวมไฟล์ ขอให้ประสบความสำเร็จในการนำวิธีการนี้ไปประยุกต์ใช้!