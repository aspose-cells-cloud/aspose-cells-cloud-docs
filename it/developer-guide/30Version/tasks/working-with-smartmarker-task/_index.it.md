---
title: "Lavorare con l'attività SmartMarker nell'API Aspose.Cells Cloud"
type: docs
url: /it/tasks/smartmarker/
aliases: [/it/working-with-smartmarker-task/]
keywords: "attività SmartMarker, Aspose.Cells Cloud, API REST, Excel, automazione dei fogli di calcolo"
description: "Scopri come utilizzare l'attività SmartMarker dell'API Aspose.Cells Cloud con esempi in cURL e SDK, inclusi lo schema della richiesta e la gestione degli errori."
weight: 60
ArticleTitle: "Lavorare con l'attività SmartMarker nell'API Aspose.Cells Cloud"
---

## API REST

**SmartMarker** è una funzionalità dell'API Aspose.Cells Cloud che consente di unire dati provenienti da origini XML o JSON all'interno di segnaposto in un modello Excel, generando un workbook completamente compilato. È comunemente utilizzata per la generazione di report, il mail‑merge e la creazione di fogli di calcolo guidata dai dati.

**Prerequisiti**

- API Aspose.Cells Cloud versione 3.0 o successiva.  
- Un token di accesso OAuth2/JWT valido (passato nell'intestazione `Authorization: Bearer <token>`).  
- File sorgente (workbook modello e file dati) caricati su Aspose Cloud Storage o accessibili tramite un tipo di file system supportato.  
- Endpoint HTTPS (tutte le richieste devono utilizzare TLS).

| **API** | **Tipo** | **Descrizione** | **Collegamento alla risorsa** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Esegui attività | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come eseguire un'attività SmartMarker e successivamente salvare il workbook risultante.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

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

### Schema della richiesta (estratto)

| Elemento | Tipo | Obbligatorio | Descrizione |
| ------- | ---- | -------- | ----------- |
| `TaskData` | object | Sì | Elemento radice che contiene uno o più oggetti `TaskDescription`. |
| `Tasks` | array di oggetti | Sì | Raccolta di attività da eseguire in ordine. |
| `TaskDescription.TaskType` | string | Sì | Tipo di attività (`SmartMarker`, `SaveResult`, ecc.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | object | Sì | Specifica la posizione del workbook modello. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | object | Sì | Specifica dove viene memorizzato il workbook intermedio. |
| `SmartMarkerTaskParameter.xmlFile` | object | Sì | Origine dati (XML/JSON) utilizzata da SmartMarker. |
| `SaveResultTaskParameter.ResultDestination` | object | Sì | Definisce come viene restituito il workbook finale (ad esempio, `OutputStream`). |

### Gestione degli errori

L'API può restituire i seguenti codici di stato HTTP:

- **400 Bad Request** – payload della richiesta non corretto o campi obbligatori mancanti.  
- **401 Unauthorized** – token di autenticazione non valido o mancante.  
- **404 Not Found** – uno dei file sorgente specificati non può essere individuato.  
- **500 Internal Server Error** – si è verificato un errore imprevisto lato server.

Controlla il corpo della risposta per un oggetto `Error` che include un `Code` e un `Message` descrittivo.

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

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