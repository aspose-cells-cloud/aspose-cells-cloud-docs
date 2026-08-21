---
title: "Support Request File in Task API"
second_title: "Dokument"
type: docs
url: /de/tasks/support-request-file/
aliases: [  /de/support-request-file-in-task-api/ ]
keywords: "Aspose.Cells, REST API, Excel, Cloud"
description: "Die Aspose.Cells Cloud API ermöglicht die aufgabenbasierte Verarbeitung von Anforderungsdateien für Excel-Arbeitsmappen."
weight: 10
ArticleTitle: "Support Request File in der Aspose.Cells Task API"
---

## REST API

| **API** | **Typ** | **Beschreibung** | **Ressourcenlink** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Task ausführen | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-basierte Interaktionen direkt aus einem Webbrowser.

**Anforderungsparameter**

| Parameter | Typ | Erforderlich | Beschreibung |
|-----------|------|----------|-------------|
| TaskDescription | Objekt | Ja | Container für eine einzelne Taskdefinition. |
| TaskType | Zeichenkette | Ja | Typ des Tasks, z. B. `ImportData` oder `SaveResult`. |
| Workbook.FileSourceType | Zeichenkette | Ja | Quelle der Arbeitsmappendatei (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | Zeichenkette | Ja | Pfad zur Arbeitsmappendatei in der ausgewählten Quelle. |
| ImportBatchDataOption.DestinationWorksheet | Zeichenkette | Ja | Name des Zielarbeitsblatts für die importierten Daten. |
| ImportBatchDataOption.IsInsert | Boolescher Wert | Ja | Gibt an, ob Zeilen eingefügt (`true`) oder überschrieben (`false`) werden sollen. |
| ImportBatchDataOption.Source.FileSourceType | Zeichenkette | Ja | Quelle der Anforderungsdatei (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | Zeichenkette | Ja | Pfad zur Anforderungsdatei, die die Stapeldaten enthält. |
| SaveResultTaskParameter.ResultSource | Zeichenkette | Ja | Quelle der Ergebnisdatei (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | Zeichenkette | Ja | Zielart für das Ergebnis (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | Zeichenkette | Ja | Name der Eingabe-Arbeitsmappendatei. |
| SaveResultTaskParameter.ResultDestination.OutputFile | Zeichenkette | Ja | Gewünschter Name der Ausgabedatei. |

**Antwort**

| Feld | Typ | Beschreibung |
|------|-----|-------------|
| Code | Ganzzahl | HTTP-Statuscode (z. B. 200 für Erfolg). |
| Status | Zeichenkette | Status der Operation (`OK` oder Fehlermeldung). |
| Result | Objekt | Details der Taskausführung, einschließlich aller generierten Dateien. |

Sie können das **cURL**-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie mithilfe von cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

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

Weitere Informationen zu verwandten Tasks finden Sie auf den Seiten zur [ImportData-Aufgabe](/cells/tasks/importdata/) und zur [SaveResult-Aufgabe](/cells/tasks/save-result/).

## Cloud SDK Family

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste durchgeführt werden:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}