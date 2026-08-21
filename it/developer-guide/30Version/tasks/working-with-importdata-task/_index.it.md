---
title: "Attività ImportData – Riferimento API Aspose.Cells Cloud ed esempi cURL"  
second_title: "Documento"  
type: docs  
url: /it/tasks/importdata/  
aliases: [/it/working-with-importdata-task/]  
keywords: "Aspose.Cells, Attività ImportData, API Excel, REST, cURL, SDK"  
description: "Scopri come importare dati in batch nei fogli di calcolo Excel utilizzando l'attività ImportData di Aspose.Cells Cloud. Include sintassi cURL, schema della richiesta, esempi di SDK (C#, PHP, Ruby, Node.js) e gestione degli errori."  
weight: 40  
---  

## API REST  

| **API** | **Tipo** | **Descrizione** | **Collegamento alla risorsa** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Esegui attività | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definisce un'interfaccia di programmazione accessibile pubblicamente che consente interazioni REST dirette da un browser web.  

Puoi utilizzare lo strumento a riga di comando **cURL** per richiamare i servizi Aspose.Cells Cloud. L'esempio seguente mostra come eseguire un'attività **ImportData** con un payload JSON correttamente formattato.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

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

Utilizzare un SDK rappresenta il modo più efficiente per integrare queste operazioni all'interno della tua applicazione. Gli SDK gestiscono l'autenticazione, la costruzione della richiesta e l'analisi della risposta, consentendoti di concentrarti sulla logica di business. Per un elenco completo degli SDK di Aspose.Cells Cloud, consulta il [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come richiamare i servizi web Aspose.Cells utilizzando vari SDK:

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