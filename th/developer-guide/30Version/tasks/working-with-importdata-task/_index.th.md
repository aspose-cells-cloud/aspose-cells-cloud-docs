---
title: "งาน ImportData – เอกสารอ้างอิง API Aspose.Cells Cloud และตัวอย่าง cURL"  
second_title: "เอกสาร"  
type: docs  
url: /th/tasks/importdata/
aliases: [  /th/working-with-importdata-task/ ]
keywords: "Aspose.Cells, งาน ImportData, API Excel, REST, cURL, SDK"  
description: "เรียนรู้วิธีการนำข้อมูลจำนวนมากเข้าสู่สมุดงาน Excel โดยใช้งาน ImportData Task ของ Aspose.Cells Cloud รวมถึงไวยากรณ์ cURL, โครงสร้างคำขอ, ตัวอย่าง SDK (C#, PHP, Ruby, Node.js) และการจัดการข้อผิดพลาด"  
weight: 40  
---  

## API REST  

| **API** | **ประเภท** | **คำอธิบาย** | **ลิงก์ทรัพยากร** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | รันงาน | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้จากภายนอก เพื่อให้สามารถใช้งาน REST โดยตรงจากเว็บเบราว์เซอร์ได้  

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเรียกใช้บริการ Aspose.Cells Cloud ตัวอย่างด้านล่างแสดงวิธีการรันงาน **ImportData** ด้วยข้อมูล JSON ที่จัดรูปแบบอย่างถูกต้อง  

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}  

{{< tab tabNum="1" >}}  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
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
  "Status": "OK",
  "TaskId": "12345678",
  "Result": {
    "FilePath": "ImpDataBook.xlsx",
    "DownloadUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
  }
}
```

{{< /tab >}}  

{{< /tabs >}}  

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการผสานรวมการดำเนินการเหล่านี้เข้ากับแอปพลิเคชันของคุณ SDK จะจัดการการยืนยันตัวตน การสร้างคำขอ และการแยกวิเคราะห์การตอบกลับ ช่วยให้คุณมุ่งเน้นที่ตรรกะทางธุรกิจได้ตามต้องการ สำหรับรายการ SDK ทั้งหมดของ Aspose.Cells Cloud โปรดดูที่ [คลัง GitHub](https://github.com/aspose-cells-cloud)  

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:  

{{< tabs tabTotal="5" tabID="8" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" >}}  

{{< tab tabNum="1" >}}  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Tasks-ImportTaskData-1.cs" >}}  

{{< /tab >}}  

{{< tab tabNum="2" >}}  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}  

{{< /tab >}}  

{{< tab tabNum="3" >}}  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_run_task-.rb" >}}  

{{< /tab >}}  

{{< tab tabNum="4" >}}  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Tasks-ImportTaskData-1.js" >}}  

{{< /tab >}}  

{{< tab tabNum="5" >}}  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ImportData-postImportDataMultipartContent-1.pl" >}}  

{{< /tab >}}  

{{< /tabs >}}