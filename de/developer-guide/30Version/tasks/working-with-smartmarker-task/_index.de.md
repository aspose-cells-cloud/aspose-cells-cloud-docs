---
title: "Arbeiten mit der SmartMarker-Aufgabe in der Aspose.Cells Cloud API"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "SmartMarker-Aufgabe, Aspose.Cells Cloud, REST API, Excel, Tabellenkalkulationsautomatisierung"
description: "Erfahren Sie, wie Sie die SmartMarker-Aufgabe der Aspose.Cells Cloud API mit cURL- und SDK-Beispielen verwenden, einschließlich Anforderungsschema und Fehlerbehandlung."
weight: 60
ArticleTitle: "Arbeiten mit der SmartMarker-Aufgabe in der Aspose.Cells Cloud API"
---

## REST API

**SmartMarker** ist eine Funktion der Aspose.Cells Cloud API, die Daten aus XML- oder JSON-Quellen in Platzhalter innerhalb einer Excel-Vorlagendatei einfügt und so eine vollständig gefüllte Arbeitsmappe erzeugt. Sie wird typischerweise für die Berichterstellung, Mail-Merge-Funktionen und datengesteuerte Tabellenkalkulationsaufgaben verwendet.

**Voraussetzungen**

- Aspose.Cells Cloud API Version 3.0 oder neuer.  
- Ein gültiges OAuth2/JWT-Zugriffstoken (wird im Header `Authorization: Bearer <token>` übermittelt).  
- Quelldateien (Vorlagenarbeitsmappe und Datendatei) müssen in den Aspose-Cloud-Speicher hochgeladen oder über einen unterstützten Dateisystemtyp zugänglich sein.  
- HTTPS-Endpunkt (alle Anforderungen müssen TLS verwenden).

| **API** | **Typ** | **Beschreibung** | **Ressourcenlink** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Aufgabe ausführen | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie eine SmartMarker-Aufgabe ausgeführt und das Ergebnis als Arbeitsmappe gespeichert wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

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

### Anforderungsschema (Auszug)

| Element | Typ | Erforderlich | Beschreibung |
| ------- | ---- | -------- | ----------- |
| `TaskData` | Objekt | Ja | Wurzelelement, das ein oder mehrere `TaskDescription`-Objekte enthält. |
| `Tasks` | Array von Objekten | Ja | Sammlung von Aufgaben, die in der angegebenen Reihenfolge ausgeführt werden. |
| `TaskDescription.TaskType` | Zeichenfolge | Ja | Der Aufgabentyp (`SmartMarker`, `SaveResult`, usw.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | Objekt | Ja | Gibt den Speicherort der Vorlagenarbeitsmappe an. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | Objekt | Ja | Gibt an, wo die Zwischenarbeitsmappe gespeichert wird. |
| `SmartMarkerTaskParameter.xmlFile` | Objekt | Ja | Datenquelle (XML/JSON), die von SmartMarker verwendet wird. |
| `SaveResultTaskParameter.ResultDestination` | Objekt | Ja | Definiert, wie die endgültige Arbeitsmappe zurückgegeben wird (z. B. `OutputStream`). |

### Fehlerbehandlung

Die API kann die folgenden HTTP-Statuscodes zurückgeben:

- **400 Bad Request** – fehlerhafter Anforderungstext oder fehlende erforderliche Felder.  
- **401 Unauthorized** – ungültiges oder fehlendes Authentifizierungstoken.  
- **404 Not Found** – eine der angegebenen Quelldateien konnte nicht gefunden werden.  
- **500 Internal Server Error** – ein unerwarteter serverseitiger Fehler ist aufgetreten.

Prüfen Sie den Antworttext auf ein `Error`-Objekt, das einen `Code` und eine beschreibende `Message` enthält.

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektanforderungen zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

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