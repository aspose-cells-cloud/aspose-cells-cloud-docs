---
title: "Batchkonvertera Excel-filer"
second_title: "Dokument"
type: docs
url: /batch/convert
keywords: "batchkonvertering, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, kalkylark"
description: "Lär dig hur du använder Aspose.Cells Cloud API för att batchkonvertera flera Excel-filer till format som PDF, CSV, JSON eller Markdown. Den här guiden innehåller information om REST-slutpunkter, begärparametrar, ett cURL-exempel och SDK-kodavsnitt för olika programmeringsspråk."
weight: 100
---

Detta REST API möjliggör **batchkonvertering** av lämpliga filer.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn       | Typ    | Plats | Beskrivning                                           |
|----------------------|--------|-------|-------------------------------------------------------|
| **batchConvertRequest** | objekt | body  | Begärandetext som innehåller konverteringsinställningar.         |

#### Egenskaper för BatchConvertRequest

| Namn               | Typ                 | Beskrivning                                           | Anteckningar |
|--------------------|---------------------|-------------------------------------------------------|--------------|
| **SourceFolder**   | sträng              | Sökväg till mappen som innehåller käll-Excel-filerna. | [valfri] |
| **MatchCondition** | MatchConditionRequest | Villkor används för att välja filer för konvertering.      | [valfri] |
| **Format**         | sträng              | Målformat för konvertering (t.ex. `pdf`, `csv`).   | [valfri] |
| **OutFolder**      | sträng              | Målmapp där konverterade filer sparas. | [valfri] |
| **SaveOptions**    | SaveOptions         | Ytterligare alternativ som styr hur filerna sparas. | [valfri] |

#### Egenskaper för MatchConditionRequest

| Namn                  | Typ       | Beskrivning                                          | Anteckningar |
|-----------------------|-----------|------------------------------------------------------|--------------|
| **RegexPattern**      | sträng    | Reguljärt uttryck som används för att filtrera filnamn.       | [valfri] |
| **FullMatchConditions** | sträng[] | Lista med exakta filnamnsvillkor för matchning.    | [valfri] |


### Begärparametrar i begärandetexten

| Parameternamn | Typ | Beskrivning                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | fil | Binärt innehåll i arbetsbokensfil som ska skapas. |
  
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

| Kod | Betydelse                     | När den returneras                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | Arbetsboken skapades framgångsrikt | Normal flödesväg                              |
| 201 Created | Arbetsboken skapades (alternativt svar) | När API:et returnerar statusen 'created' |
| 400 Bad Request | Ogiltiga parametrar | Klientsidfel                        |
| 401 Unauthorized | Saknas eller ogiltig token | Autentiseringsfel                    |
| 409 Conflict | Filen finns redan och `isWriteOver=false` | Konflikt med befintlig fil    

## Hur man använder PostBatchConvert API med SDK:er

### PostBatchConvert API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PostBatchConvert) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---