---
title: "Lås Excel-filer i batch"
second_title: "Dokument"
type: docs
url: /sv/batch/lock
keywords: "batchlåsning, Excel, Aspose.Cells, molntjänst, kalkylark, filskydd"
description: "Aspose.Cells molntjänst möjliggör batchlåsning av flera Excel-filer. Använd REST-slutpunkten eller någon av de stödda SDK:erna (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go etc.) för att låsa filer i batch."
weight: 100
---

Denna REST-tjänst tillåter **batchlåsning** av lämpliga Excel-filer.

## REST-tjänst

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Säkerhet och autentisering**

Aspose.Cells molntjänster är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begärparametrar

| Parameternamn    | Typ                | Plats    | Beskrivning                               |
|------------------|--------------------|----------|-------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body     | JSON-body som innehåller låsparametrar.  |

#### **BatchLockRequest**-egenskaper

| Namn           | Typ                      | Beskrivning                                           | Noteringar    |
|----------------|--------------------------|-------------------------------------------------------|---------------|
| SourceFolder   | string                   | Mapp som innehåller käll-Excel-filerna.             | valfri        |
| MatchCondition | MatchConditionRequest    | Villkor för att välja vilka filer som ska låsas.     | valfri        |
| Password       | string                   | Lösenord som ska appliceras på de låsta filerna.     | valfri        |
| OutFolder      | string                   | Målmap för de låsta filerna.                          | valfri        |

#### **MatchConditionRequest**-egenskaper

| Namn               | Typ       | Beskrivning                                          | Noteringar    |
|--------------------|-----------|------------------------------------------------------|---------------|
| RegexPattern       | string    | Mönster för reguljärt uttryck för att matcha filnamn.| valfri        |
| FullMatchConditions| string[]  | Exakta matchningar av filnamn för låsning.          | valfri        |

### Begärons body-parameter

| Parameternamn | Typ  | Beskrivning                                   |
| ------------- | ---- | --------------------------------------------- |
| data          | file | Binärt innehåll i arbetsboken som ska skapas. |

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

| Kod  | Betydelse                    | När returneras                        |
|------|------------------------------|---------------------------------------|
| 200 OK | Arbetsboken skapades framgångsrikt | Normalt flöde                        |
| 201 Created | Arbetsboken skapades (alternativt svar) | När API:et returnerar statusen "created" |
| 400 Bad Request | Ogiltiga parametrar | Klientsidorfel                        |
| 401 Unauthorized | Saknas eller ogiltig token | Autentiseringsfel                    |
| 409 Conflict | Filen finns och `isWriteOver=false` | Konflikt med existerande fil         |

## Hur man använder PostBatchLock-API:et med SDK:er

### PostBatchLock-API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Exemplet nedan visar hur man anropar molntjänsten med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina låsuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}