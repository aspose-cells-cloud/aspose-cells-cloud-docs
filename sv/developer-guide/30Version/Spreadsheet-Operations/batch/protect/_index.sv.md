---
title: "Skyddera Excel-filer i batch"
second_title: "Dokument"
type: docs
url: /batch/protect
keywords: "Skyddera Excel-filer i batch, Aspose Cells Cloud, REST API, Excel-skydd, batchskydd"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att skydda flera Excel-filer i batch. Innehåller begärandedetaljer, cURL-exempel och SDK-kodexempel för olika språk."
weight: 100
---

Detta REST API möjliggör **batchskydd** för lämpliga Excel-filer.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäran parametrar

| Parameternamn         | Typ                 | Plats   | Beskrivning                                                                                              |
|-----------------------|---------------------|---------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body    | JSON-payload som anger källmappen, matchningsvillkor, skyddstyp, lösenord och utdatamapp.                |

### Egenskaper för BatchProtectRequest

| Namn              | Typ                     | Beskrivning                                                                                | Anteckningar |
|-------------------|--------------------------|--------------------------------------------------------------------------------------------|--------------|
| SourceFolder      | string                   | Mapp som innehåller käll-Excel-filerna.                                                   | valfri       |
| MatchCondition    | MatchConditionRequest   | Kriterier som används för att välja filer för skydd.                                      | valfri       |
| ProtectionType    | string                   | Typ av skydd som ska tillämpas (t.ex. `All`, `ReadOnly`).                                 | valfri       |
| Password          | string                   | Lösenord som ska ställas in för de skyddade filerna.                                       | valfri       |
| OutFolder         | string                   | Målmappe för de skyddade filerna.                                                          | valfri       |

### Egenskaper för MatchConditionRequest

| Namn                | Typ        | Beskrivning                                   | Anteckningar |
|---------------------|------------|-----------------------------------------------|--------------|
| RegexPattern        | string     | Reguljärt uttryck som används för att matcha filnamn. | valfri       |
| FullMatchConditions | string[]   | Lista med exakta filnamnsvillkor.            | valfri       |

### Begäran brödtextparameter

| Parameternamn | Typ  | Beskrivning                                    |
|---------------|------|------------------------------------------------|
| data          | file | Binärt innehåll i arbetsboksfilen som ska skapas. |

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

| Kod | Betydelse                     | När den returneras                      |
|-----|-------------------------------|-----------------------------------------|
| 200 OK | Arbetsboken skapades utan problem | Normalt flöde                            |
| 201 Created | Arbetsboken skapades (alternativt svar) | När API:t returnerar statusen "created" |
| 400 Bad Request | Ogiltiga parametrar | Klientsidigt fel                         |
| 401 Unauthorized | Saknas eller ogiltig token | Autentiseringsfel                       |
| 409 Conflict | Filen finns och `isWriteOver=false` | Konflikt med befintlig fil             

## Hur man använder PostProtectConvert API med SDK:er

### PostProtectConvert API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PostProtectConvert) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör en anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projekttal. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}