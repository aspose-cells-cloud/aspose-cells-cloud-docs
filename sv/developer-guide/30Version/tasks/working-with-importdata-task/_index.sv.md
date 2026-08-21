---
title: "ImportData-uppgift – Aspose.Cells Cloud API-referens och cURL-exempel"  
second_title: "Dokument"  
type: docs  
url: /sv/tasks/importdata/
aliases: [  /sv/working-with-importdata-task/ ]
keywords: "Aspose.Cells, ImportData-uppgift, Excel API, REST, cURL, SDK"  
description: "Lär dig hur du importerar batchdata till Excel-arbetsböcker med Aspose.Cells Cloud ImportData-uppgift. Innehåller cURL-syntax, begäransschema, SDK-exempel (C#, PHP, Ruby, Node.js) och felhantering."  
weight: 40  
---  

## REST API  

| **API** | **Typ** | **Beskrivning** | **Resurslänk** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Kör uppgift | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definierar ett offentligt tillgängligt programmeringssnitt som möjliggör direkta REST-interaktioner från en webbläsare.  

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells Cloud-tjänster. Exempel nedan visar hur du kör en **ImportData**-uppgift med en korrekt formaterad JSON-payload.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

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

Att använda ett SDK är det mest effektiva sättet att integrera dessa åtgärder i din applikation. SDK:er hanterar autentisering, begäransskapande och svarsparsering, så att du kan fokusera på affärslogik. För en fullständig lista över Aspose.Cells Cloud SDK:er, se [GitHub-förrådet](https://github.com/aspose-cells-cloud).  

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

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