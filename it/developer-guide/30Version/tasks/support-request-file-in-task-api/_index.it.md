---
title: "File di richiesta supporto nell'API di Task"
second_title: "Documenti"
type: docs
url: /it/tasks/support-request-file/
aliases: [  /it/support-request-file-in-task-api/ ]
keywords: "Aspose.Cells, API REST, Excel, Cloud"
description: "L'API Cloud Aspose.Cells consente l'elaborazione basata su task dei file di richiesta per cartelle di lavoro Excel."
weight: 10
ArticleTitle: "File di richiesta supporto nell'API di Task di Aspose.Cells"
---

## API REST

| **API** | **Tipo** | **Descrizione** | **Collegamento alla risorsa** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Esegui Task | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

**Parametri della richiesta**

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|--------------|-------------|
| TaskDescription | object | Sì | Contenitore per una singola definizione di task. |
| TaskType | string | Sì | Tipo di task, ad esempio `ImportData` o `SaveResult`. |
| Workbook.FileSourceType | string | Sì | Origine del file della cartella di lavoro (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | string | Sì | Percorso del file della cartella di lavoro nell'origine selezionata. |
| ImportBatchDataOption.DestinationWorksheet | string | Sì | Nome del foglio di lavoro di destinazione per i dati importati. |
| ImportBatchDataOption.IsInsert | boolean | Sì | Indica se inserire righe (`true`) o sovrascrivere (`false`). |
| ImportBatchDataOption.Source.FileSourceType | string | Sì | Origine del file di richiesta (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | string | Sì | Percorso del file di richiesta contenente i dati in batch. |
| SaveResultTaskParameter.ResultSource | string | Sì | Origine del file di risultato (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | Sì | Tipo di destinazione per il risultato (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | string | Sì | Nome del file della cartella di lavoro di input. |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | Sì | Nome desiderato del file di output. |

**Risposta**

| Campo | Tipo | Descrizione |
|-------|------|-------------|
| Code | integer | Codice di stato HTTP (ad esempio, 200 per successo). |
| Status | string | Stato dell'operazione (`OK` o messaggio di errore). |
| Result | object | Dettagli dell'esecuzione del task, inclusi eventuali file generati. |

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

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

Per ulteriori informazioni sui task correlati, consulta le pagine [ImportData task](/it/cells/tasks/importdata/) e [SaveResult task](/it/cells/tasks/save-result/).

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}