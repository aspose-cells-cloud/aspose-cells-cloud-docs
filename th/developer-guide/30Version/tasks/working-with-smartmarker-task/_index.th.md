---
---
title: "การทำงานกับงาน SmartMarker ใน Aspose.Cells Cloud API"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "งาน SmartMarker, Aspose.Cells Cloud, REST API, Excel, การสร้างสเปรดชีตอัตโนมัติ"
description: "เรียนรู้วิธีใช้งานงาน SmartMarker ของ Aspose.Cells Cloud API พร้อมตัวอย่าง cURL และ SDK รวมถึงโครงสร้างคำขอและการจัดการข้อผิดพลาด"
weight: 60
ArticleTitle: "การทำงานกับงาน SmartMarker ใน Aspose.Cells Cloud API"
---

## API แบบ REST

**SmartMarker** คือคุณลักษณะหนึ่งของ Aspose.Cells Cloud API ที่ใช้รวมข้อมูลจากแหล่งข้อมูล XML หรือ JSON เข้ากับตัวยึดตำแหน่ง (placeholder) ที่อยู่ในเทมเพลตสมุดงาน Excel เพื่อสร้างสมุดงานที่เต็มไปด้วยข้อมูลเรียบร้อยแล้ว โดยคุณลักษณะนี้มักถูกนำไปใช้ในการสร้างรายงาน การรวมข้อมูลแบบเมลล์เมิร์จ และการสร้างสเปรดชีตที่ขับเคลื่อนด้วยข้อมูล

**ข้อกำหนดเบื้องต้น**

- Aspose.Cells Cloud API เวอร์ชัน 3.0 หรือใหม่กว่า  
- โทเค็นการยืนยันตัวตน OAuth2/JWT ที่ถูกต้อง (ส่งผ่านในส่วนหัว `Authorization: Bearer <token>`)  
- ไฟล์ต้นทาง (สมุดงานเทมเพลตและไฟล์ข้อมูล) ถูกอัปโหลดไว้ในพื้นที่จัดเก็บของ Aspose Cloud หรือสามารถเข้าถึงได้ผ่านระบบไฟล์ที่รองรับ  
- จุดสิ้นสุด HTTPS (คำขอทั้งหมดต้องใช้ TLS)

| **API** | **ประเภท** | **คำอธิบาย** | **ลิงก์ทรัพยากร** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | รันงาน | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการรันงาน SmartMarker และบันทึกผลลัพธ์สมุดงานที่ได้

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <your_access_token>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### โครงสร้างคำขอ (ส่วนย่อ)

| องค์ประกอบ | ประเภท | จำเป็น | คำอธิบาย |
| ------- | ---- | -------- | ----------- |
| `TaskData` | ออบเจกต์ | จำเป็น | องค์ประกอบรากที่มีออบเจกต์ `TaskDescription` อย่างน้อยหนึ่งตัว |
| `Tasks` | อาร์เรย์ของออบเจกต์ | จำเป็น | คอลเลกชันของงานที่จะดำเนินการตามลำดับ |
| `TaskDescription.TaskType` | สตริง | จำเป็น | ประเภทของงาน (เช่น `SmartMarker`, `SaveResult` เป็นต้น) |
| `SmartMarkerTaskParameter.SourceWorkbook` | ออบเจกต์ | จำเป็น | ระบุตำแหน่งของสมุดงานเทมเพลต |
| `SmartMarkerTaskParameter.DestinationWorkbook` | ออบเจกต์ | จำเป็น | ระบุตำแหน่งที่เก็บสมุดงานระดับกลาง |
| `SmartMarkerTaskParameter.xmlFile` | ออบเจกต์ | จำเป็น | แหล่งข้อมูล (XML/JSON) ที่ใช้โดย SmartMarker |
| `SaveResultTaskParameter.ResultDestination` | ออบเจกต์ | จำเป็น | กำหนดวิธีการส่งคืนสมุดงานสุดท้าย (เช่น `OutputStream`) |

### การจัดการข้อผิดพลาด

API อาจส่งกลับสถานะ HTTP ต่อไปนี้:

- **400 Bad Request** – ข้อมูลคำขอเสียรูปหรือขาดองค์ประกอบที่จำเป็น  
- **401 Unauthorized** – โทเค็นการยืนยันตัวตนไม่ถูกต้องหรือไม่มีการระบุ  
- **404 Not Found** – ไม่พบหนึ่งในไฟล์ต้นทางที่ระบุไว้  
- **500 Internal Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์

ตรวจสอบเนื้อหาในส่วนตอบกลับเพื่อดูออบเจกต์ `Error` ซึ่งประกอบด้วย `Code` และ `Message` ที่ให้คำอธิบายรายละเอียด

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

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
                    <FilePath>Designer.xlsx</FilePath>
                </SourceWorkbook>
                <DestinationWorkbook>
                    <FileSourceType>InMemoryFiles</FileSourceType>
                    <FilePath>Temp.xlsx</FilePath>
                </DestinationWorkbook>
                <xmlFile>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>DataSet.xml</FilePath>
                </xmlFile>
            </SmartMarkerTaskParameter>
        </TaskDescription>
        <TaskDescription>
            <TaskType>SaveResult</TaskType>
            <SaveResultTaskParameter>
                <ResultSource>InMemoryFiles</ResultSource>
                <ResultDestination>
                    <DestinationType>OutputStream</DestinationType>
                    <InputFile>Temp.xlsx</InputFile>
                    <OutputFile>Output.xlsx</OutputFile>
                </ResultDestination>
            </SaveResultTaskParameter>
        </TaskDescription>
    </Tasks>
</TaskData>";

ServiceHelper helper = new ServiceHelper(sid, key);
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}
---