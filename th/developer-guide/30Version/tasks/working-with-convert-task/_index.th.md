---
title: "การทำงานกับงาน Convert"
second_title: "เอกสาร"
type: docs
url: /tasks/convert/
aliases: [/working-with-convert-task/]
keywords: "Aspose.Cells Cloud, REST API, งาน Convert, Excel, สเปรดชีต, PDF, CSV, JSON, Markdown"
description: "API ของ Cells Cloud สำหรับ Excel มีการรองรับงานสำหรับการแปลงไฟล์ Excel เป็นรูปแบบต่างๆ"
weight: 30
---

## REST API

|**API**|**ประเภท**|**คำอธิบาย**|**ลิงก์ทรัพยากร**|
| :- | :- | :- | :- |
|/cells/task/runtask|POST|รันงาน|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการเชื่อมต่อแบบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์  

คุณสามารถใช้เครื่องมือ **cURL** ที่รันผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำร้องขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```java
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData>\t<Tasks>\t<TaskDescription>\t\t<TaskType>SmartMarker</TaskType>\t\t<SmartMarkerTaskParameter>\t\t<SourceWorkbook>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>Book1.xlsx</FilePath>\t\t</SourceWorkbook>\t\t<DestinationWorkbook>\t\t\t<FileSourceType>InMemoryFiles</FileSourceType>\t\t\t<FilePath>ReportTask.xlsx</FilePath>\t\t</DestinationWorkbook>\t\t<xmlFile>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>ReportData.xml</FilePath>\t\t</xmlFile>\t\t</SmartMarkerTaskParameter>\t</TaskDescription>\t<TaskDescription>\t\t<TaskType>SaveResult</TaskType>\t\t<SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t\t<DestinationType>OutputStream</DestinationType>\t\t\t<InputFile>ReportTask.xlsx</InputFile>\t\t\t<OutputFile>Output.xlsx</OutputFile>\t\t</ResultDestination>\t\t</SaveResultTaskParameter>\t</TaskDescription>\t</Tasks></TaskData>}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
HttpResponseMessage ที่มีผลลัพธ์ของการดำเนินการ
```

{{< /tab >}}

{{< /tabs >}}

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [ kho ของ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}

```csharp
var xml = @"<TaskData>

                <Tasks>

                <TaskDescription>

                    <TaskType>SmartMarker</TaskType>

                    <SmartMarkerTaskParameter>

                    <SourceWorkbook>

                        <FileSourceType>CloudFileSystem</FileSourceType>

                        <FilePath>Book1.xlsx</FilePath>

                    </SourceWorkbook>

                    <DestinationWorkbook>

                        <FileSourceType>InMemoryFiles</FileSourceType>

                        <FilePath>ReportTask.xlsx</FilePath>

                    </DestinationWorkbook>

                    <xmlFile>

                        <FileSourceType>CloudFileSystem</FileSourceType>

                        <FilePath>ReportData.xml</FilePath>

                    </xmlFile>

                    </SmartMarkerTaskParameter>

                </TaskDescription>

                <TaskDescription>

                    <TaskType>SaveResult</TaskType>

                    <SaveResultTaskParameter>

                    <ResultSource>InMemoryFiles</ResultSource>

                    <ResultDestination>

                        <DestinationType>OutputStream</DestinationType>

                        <InputFile>ReportTask.xlsx</InputFile>

                        <OutputFile>Output.xlsx</OutputFile>

                    </ResultDestination>

                    </SaveResultTaskParameter>

                </TaskDescription>

                </Tasks>

            </TaskData>";


ServiceHelper helper = new ServiceHelper(sid, key);

using (HttpWebResponse response = helper.CallPost("http://api.aspose.com/v3.0/cells/task/runtask", xml, "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        System.Console.WriteLine("OK");
        Stream st = response.GetResponseStream();
        FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate);
        st.CopyTo(fs);
    }
}//using
```

{{< /tab >}}

{{< /tabs >}}
---