---
title: "Stöd förfrågningsfil i Task API"
second_title: "Document"
type: docs
url: /sv/tasks/support-request-file/
aliases: [  /sv/support-request-file-in-task-api/ ]
keywords: "Aspose.Cells, REST API, Excel, moln"
description: "Aspose.Cells Cloud API möjliggör uppgiftsbaserad bearbetning av förfrågningsfiler för Excel-arbetsböcker."
weight: 10
ArticleTitle: "Stöd förfrågningsfil i Aspose.Cells Task API"
---

## REST API

| **API** | **Typ** | **Beskrivning** | **Resurslänk** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Kör uppgift | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

**Förfrågningsparametrar**

| Parameter | Typ | Krävs | Beskrivning |
|-----------|------|----------|-------------|
| TaskDescription | objekt | Ja | Container för en enskild uppgiftsdefinition. |
| TaskType | sträng | Ja | Uppgiftstyp, t.ex. `ImportData` eller `SaveResult`. |
| Workbook.FileSourceType | sträng | Ja | Källa för arbetsboksfilen (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | sträng | Ja | Sökväg till arbetsboksfilen i den valda källan. |
| ImportBatchDataOption.DestinationWorksheet | sträng | Ja | Målarbetsbladets namn för importerad data. |
| ImportBatchDataOption.IsInsert | boolean | Ja | Om rader ska infogas (`true`) eller skrivas över (`false`). |
| ImportBatchDataOption.Source.FileSourceType | sträng | Ja | Källa för förfrågningsfilen (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | sträng | Ja | Sökväg till förfrågningsfilen som innehåller batchdata. |
| SaveResultTaskParameter.ResultSource | sträng | Ja | Källa för resultattfilen (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | sträng | Ja | Måltyp för resultatet (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | sträng | Ja | Namn på indataarbetsboksfil. |
| SaveResultTaskParameter.ResultDestination.OutputFile | sträng | Ja | Önskat namn på utdatafil. |

**Svar**

| Fält | Typ | Beskrivning |
|------|-----|-------------|
| Code | heltal | HTTP-statuskod (t.ex. 200 för lyckad åtgärd). |
| Status | sträng | Åtgärdens status (`OK` eller felmeddelande). |
| Result | objekt | Detaljerad information om uppgiftskörningen, inklusive eventuellt genererade filer. |

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

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

Mer information om relaterade uppgifter finns på sidorna [ImportData-uppgiften](/sv/cells/tasks/importdata/) och [SaveResult-uppgiften](/sv/cells/tasks/save-result/).

## Moln SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:n:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}