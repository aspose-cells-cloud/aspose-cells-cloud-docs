---
title: "Arbeta med SmartMarker-uppgiften i Aspose.Cells Cloud API"
type: docs
url: /sv/tasks/smartmarker/
aliases: [  /sv/working-with-smartmarker-task/ ]
keywords: "SmartMarker-uppgift, Aspose.Cells Cloud, REST API, Excel, kalkylark automation"
description: "Lär dig hur du använder SmartMarker-uppgiften i Aspose.Cells Cloud API med cURL- och SDK-exempel, inklusive begäransschema och felhantering."
weight: 60
ArticleTitle: "Arbeta med SmartMarker-uppgiften i Aspose.Cells Cloud API"
---

## REST API

**SmartMarker** är en funktion i Aspose.Cells Cloud API som sammanfogar data från XML- eller JSON-källor till platshållare i en Excel-mall, vilket producerar ett helt ifyllt arbetsboksdokument. Det används vanligtvis för rapportgenerering, brevmerge och datadrivna kalkylarksskapande.

**Förutsättningar**

- Aspose.Cells Cloud API version 3.0 eller senare.  
- En giltig OAuth2/JWT-åtkomsttoken (skickas i `Authorization: Bearer <token>`-headern).  
- Källfiler (mallarbetsbok och datafil) uppladdade till Aspose Cloud-lagring eller tillgängliga via en stödd filsystemstyp.  
- HTTPS-slutpunkt (alla förfrågningar måste använda TLS).

| **API** | **Typ** | **Beskrivning** | **Resurslänk** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Kör uppgift | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du kör en SmartMarker-uppgift och därefter sparar resultatarbetsboken.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <din_åtkomsttoken>" \
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

### Begäransschema (utdrag)

| Element | Typ | Obligatoriskt | Beskrivning |
| ------- | ---- | -------- | ----------- |
| `TaskData` | objekt | Ja | Rotelement som innehåller ett eller flera `TaskDescription`-objekt. |
| `Tasks` | array med objekt | Ja | Samling av uppgifter som ska utföras i ordning. |
| `TaskDescription.TaskType` | sträng | Ja | Uppgiftstypen (`SmartMarker`, `SaveResult`, etc.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | objekt | Ja | Anger platsen för mallarbetsboken. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | objekt | Ja | Anger var den mellanliggande arbetsboken lagras. |
| `SmartMarkerTaskParameter.xmlFile` | objekt | Ja | Datakälla (XML/JSON) som används av SmartMarker. |
| `SaveResultTaskParameter.ResultDestination` | objekt | Ja | Definierar hur den slutgiltiga arbetsboken returneras (t.ex. `OutputStream`). |

### Felhantering

API:t kan returnera följande HTTP-statuskoder:

- **400 Bad Request** – felaktigt formaterad begäran eller saknade obligatoriska fält.  
- **401 Unauthorized** – ogiltig eller saknad autentiseringstoken.  
- **404 Not Found** – en av de angivna källfilerna kan inte hittas.  
- **500 Internal Server Error** – ett oväntat serverfel inträffade.

Kontrollera svarsbodyt för ett `Error`-objekt som innehåller en `Code` och en beskrivande `Message`.

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivånivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med diverse SDK:n:

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