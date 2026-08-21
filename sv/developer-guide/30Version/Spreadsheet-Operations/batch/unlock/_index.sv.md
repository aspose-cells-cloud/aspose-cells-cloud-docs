---
title: "Massupplåsning"
second_title: "Dokument"
type: docs
url: /sv/batch/unlock
keywords: "massupplåsning, Aspose.Cells Cloud, Excel, REST API, kalkylark, molntjänst"
description: "Lås upp flera Excel-filer i batch med Aspose.Cells Cloud REST API. Stöder SDK:er för C#, Java, Python och andra språk."
weight: 100
---

Denna REST API låser upp berättigade Excel-filer i batch.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameter_name | Typ | Plats | Beskrivning |
|----------------|------|----------|-------------|
| **BatchLockRequest** |  | body | Begärandetext som innehåller upplåsningsinställningarna. |

### **BatchLockRequest**-egenskaper

| Namn            | Typ                      | Beskrivning                                      | Anteckningar |
|-----------------|--------------------------|--------------------------------------------------|--------------|
| SourceFolder    | sträng                   | Mapp som innehåller käll-Excel-filerna.         | [valfritt]   |
| MatchCondition  | MatchConditionRequest    | Kriterier som används för att välja filer att låsa upp. | [valfritt]   |
| Password        | sträng                   | Lösenord som gäller för skyddade arbetsböcker.   | [valfritt]   |
| OutFolder       | sträng                   | Målmappe för de upplåsta filerna.                | [valfritt]   |

### **MatchConditionRequest**-egenskaper

| Namn               | Typ       | Beskrivning                               | Anteckningar |
|--------------------|-----------|-------------------------------------------|--------------|
| RegexPattern       | sträng    | reguljärt uttryck för att matcha filnamn. | [valfritt]   |
| FullMatchConditions| sträng[]  | Exakta filnamnsvillkor att matcha.       | [valfritt]   |

### Begärandetextparameter

| Parameter_name | Typ | Beskrivning                                |
| -------------- | --- | ------------------------------------------ |
| data           | fil | Binärt innehåll i arbetsboken som ska skapas. |

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

| Kod | Betydelse                     | När den returneras                     |
|-----|-------------------------------|---------------------------------------|
| 200 OK | Arbetsboken skapades framgångsrikt | Normalt flöde                          |
| 201 Created | Arbetsboken skapades (alternativt svar) | När API:et returnerar statusen 'created' |
| 400 Bad Request | Ogiltiga parametrar | Klientfel                             |
| 401 Unauthorized | Saknas eller ogiltig token | Autentiseringsfel                     |
| 409 Conflict | Filen finns och `isWriteOver=false` | Konflikt med befintlig fil            |

## Hur du använder PostBatchLock API med SDK:er

### PostBatchLock API-specificering

[OpenAPI-specificationen](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

Att använda ett SDK är det snabbaste sättet att utveckla upplåsningsfunktionalitet. Ett SDK abstraher bort detaljer på låg nivå så att du kan fokusera på din affärslogik. Kontrollera [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}
---