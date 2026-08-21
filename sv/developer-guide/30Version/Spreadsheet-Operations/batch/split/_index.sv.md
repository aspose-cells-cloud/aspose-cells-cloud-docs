---
title: "Batch Split"
second: "Dokument"
type: docs
url: /batch/split
keywords: "Batch Split, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, Kalkylark, Molntjänst SDK"
description: "Dokumentation för Aspose.Cells Clouds Batch Split API, som delar upp kalkylarksfiler i flera format såsom PDF, CSV eller JSON. Inkluderar begärandedetaljer, exempel på cURL-kommandon och användning av SDK:i för olika programmeringsspråk."
weight: 100
---

Denna REST API utför en **batchdelning** av lämpliga filer.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameter Name   | Typ                | Sökväg/Fråga/Sträng/HTTPBody | Beskrivning                                  |
|------------------|--------------------|------------------------------|----------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                         | Begärandepayload som innehåller delningsalternativ. |

### **BatchSplitRequest**-egenskaper

| Namn             | Typ                 | Beskrivning                                        | Noteringar     |
|------------------|---------------------|----------------------------------------------------|----------------|
| SourceFolder     | string              | Mapp som innehåller källfilen.                    | [valfritt]     |
| SourceStorage    | string              | Lagringsnamn där källfilen finns.                 | [valfritt]     |
| MatchCondition   | MatchConditionRequest| Villkor som används för att välja filer för delning.| [valfritt]     |
| Format           | string              | Önskat utdataformat (t.ex. pdf, csv).             | [valfritt]     |
| FromIndex        | integer             | Startindex för sidorna som ska delas.             | [valfritt]     |
| ToIndex          | integer             | Slutindex för sidorna som ska delas.              | [valfritt]     |
| OutFolder        | string              | Målmap för de delade filerna.                     | [valfritt]     |
| SaveOptions      | SaveOptions         | Ytterligare alternativ för att spara utdata.      | [valfritt]     |

### **MatchConditionRequest**-egenskaper

| Namn                 | Typ       | Beskrivning                                   | Noteringar     |
|----------------------|-----------|-----------------------------------------------|----------------|
| RegexPattern         | string    | reguljärt uttryck för att matcha filnamn.     | [valfritt]     |
| FullMatchConditions  | string[]  | Lista med exakta matchningsvillkor.           | [valfritt]     |

### Begärandetextparameter

| Parameter Name | Typ  | Beskrivning                                     |
| -------------- | ---- | ----------------------------------------------- |
| data           | file | Binärt innehåll i arbetsbokensfil som ska skapas. |

### **Svar**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                      | När den returneras                        |
|-----|--------------------------------|-------------------------------------------|
| 200 OK | Arbetsboken skapades framgångsrikt | Normal flödessituation                   |
| 201 Created | Arbetsboken skapades (alternativt svar) | När API:et returnerar statusen "created" |
| 400 Bad Request | Ogiltiga parametrar | Fel på klientens sida                    |
| 401 Unauthorized | Saknas eller ogiltig token | Autentiseringsfel                         |
| 409 Conflict | Filen finns och `isWriteOver=false` | Konflikt med befintlig fil               |


## Hur man använder PostBatchSplit API med SDK:i

### PostBatchSplit API-specificering

[OpenAPI-specificeringen](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:i

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina delningsuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:i.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:i:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---