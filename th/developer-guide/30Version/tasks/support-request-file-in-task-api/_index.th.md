---
---
title: "ไฟล์คำขอใน API งาน (Task API)"
second_title: "Document"
type: docs
url: /tasks/support-request-file/
aliases: [/support-request-file-in-task-api/]
keywords: "Aspose.Cells, REST API, Excel, Cloud"
description: "Aspose.Cells Cloud API ช่วยให้สามารถประมวลผลไฟล์คำขอแบบตั้งเป็นงาน (task-based) สำหรับสมุดงาน Excel ได้"
weight: 10
ArticleTitle: "ไฟล์คำขอใน Task API ของ Aspose.Cells"
---

## REST API

| **API** | **Type** | **คำอธิบาย** | **ลิงก์ทรัพยากร** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | รันงาน (Run Task) | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) กำหนด API ที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบแบบ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

**พารามิเตอร์คำขอ**

| พารามิเตอร์ | ประเภท | จำเป็น | คำอธิบาย |
|-----------|------|----------|-------------|
| TaskDescription | object | ใช่ | คอนเทนเนอร์สำหรับคำจำกัดความของงานหนึ่งงาน |
| TaskType | string | ใช่ | ประเภทของงาน เช่น `ImportData` หรือ `SaveResult` |
| Workbook.FileSourceType | string | ใช่ | แหล่งที่มาของไฟล์สมุดงาน (`CloudFileSystem`, `InMemoryFiles`) |
| Workbook.FilePath | string | ใช่ | เส้นทางไปยังไฟล์สมุดงานในแหล่งที่มาที่เลือก |
| ImportBatchDataOption.DestinationWorksheet | string | ใช่ | ชื่อแผ่นงานเป้าหมายสำหรับข้อมูลที่นำเข้า |
| ImportBatchDataOption.IsInsert | boolean | ใช่ | ระบุว่าจะเพิ่มแถว (`true`) หรือเขียนทับ (`false`) |
| ImportBatchDataOption.Source.FileSourceType | string | ใช่ | แหล่งที่มาของไฟล์คำขอ (`RequestFiles`) |
| ImportBatchDataOption.Source.FilePath | string | ใช่ | เส้นทางไปยังไฟล์คำขอที่มีข้อมูลแบตช์ |
| SaveResultTaskParameter.ResultSource | string | ใช่ | แหล่งที่มาของไฟล์ผลลัพธ์ (`InMemoryFiles`) |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | ใช่ | ประเภทปลายทางสำหรับผลลัพธ์ (`CloudFileSystem`) |
| SaveResultTaskParameter.ResultDestination.InputFile | string | ใช่ | ชื่อไฟล์สมุดงานอินพุต |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | ใช่ | ชื่อไฟล์เอาต์พุตที่ต้องการ |

**การตอบกลับ**

| ฟิลด์ | ประเภท | คำอธิบาย |
|-------|------|-------------|
| Code | integer | โค้ดสถานะ HTTP (เช่น 200 สำหรับความสำเร็จ) |
| Status | string | สถานะการดำเนินการ (`OK` หรือข้อความแสดงข้อผิดพลาด) |
| Result | object | รายละเอียดของการดำเนินงาน รวมถึงไฟล์ที่สร้างขึ้นใดๆ |

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
  -d '{
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet1",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml.txt"
              }
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet2",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml_2.txt"
              }
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
              "DestinationType": "CloudFileSystem",
              "InputFile": "TaskBook.xlsx",
              "OutputFile": "ImpDataBook.xlsx"
            }
          }
        }
      }
    ]
  }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับงานที่เกี่ยวข้อง โปรดดูหน้า [ImportData task](/cells/tasks/importdata/) และ [SaveResult task](/cells/tasks/save-result/)

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud แบบครบถ้วน

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}