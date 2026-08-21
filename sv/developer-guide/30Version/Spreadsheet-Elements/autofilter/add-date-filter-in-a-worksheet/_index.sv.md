---
title: "Lägg till datumfilter i ett Excel-ark"
second_title: "Dokument"
linktitle: "Lägg till datumfilter"
type: docs
url: /sv/autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "Lär dig hur du lägger till ett datumfilter i ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Inkluderar cURL-exempel, SDK-utdrag (C#, Java, Python m.m.), parametrar och felhantering."
weight: 65
ArticleTitle: "Lägg till datumfilter i ett Excel-ark | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel-datumfilter, AutoFilter API, REST API, moln-SDK, cURL, kalkylarkautomation"
---

Denna REST API lägger till ett **datumfilter** i ett Excel-ark.

**Förutsättningar:** Du måste ha ett giltigt JWT-token, och den mål-bok som ska filteras måste redan finnas på den angivna lagringsplatsen. Begäran kräver inte en JSON-kropp.

## PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar


| Parameternamn            | Typ     | Position | Beskrivning                                                                                                                                                         |
| ------------------------ | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Sökväg   | Namnet på arbetsboken.                                                                                                                                              |
| **sheetName**            | string  | Sökväg   | Namnet på arket.                                                                                                                                                    |
| **range**                | string  | Fråga    | Excel-område som filtertillämpningen gäller för (t.ex. `A1:B1`).                                                                                                    |
| **fieldIndex**           | integer | Fråga    | Nollbaserat index för kolumnen som ska filteras.                                                                                                                      |
| **dateTimeGroupingType** | string  | Fråga    | Grupperingstyp för datum-/tidfiltret. Tillåtna värden är `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. Värden är skiftlägeskänsliga; standardvärdet är `Day`. |
| **year**                 | integer | Fråga    | Årsdel av filtervärdet.                                                                                                                                             |
| **month**                | integer | Fråga    | Månadsdel av filtervärdet.                                                                                                                                          |
| **day**                  | integer | Fråga    | Dagsdel av filtervärdet.                                                                                                                                            |
| **hour**                 | integer | Fråga    | Timdel av filtervärdet.                                                                                                                                             |
| **minute**               | integer | Fråga    | Minutdel av filtervärdet.                                                                                                                                           |
| **second**               | integer | Fråga    | Sekunddel av filtervärdet.                                                                                                                                          |
| **matchBlanks**          | boolean | Fråga    | Inkludera tomma celler (`true` eller `false`).                                                                                                                      |
| **refresh**              | boolean | Fråga    | Uppdatera filtret efter tillämpning (`true` eller `false`).                                                                                                         |
| **folder**               | string  | Fråga    | Sökvägen till mappen för den ursprungliga arbetsboken.                                                                                                              |
| **storageName**          | string  | Fråga    | Namn på lagringstjänsten.                                                                                                                                           |

*Begäran med PUT kräver inte en begärankropp; alla parametrar skickas via frågesträngen.*

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 200 | OK                          | Filtret tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer.      |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).           |
| 401 | Obehörig                    | Ogiltigt eller saknat JWT-token.                                            |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.                           |
| 500 | Internt serverfel           | Oväntat serverfel.                                                          |

## Hur du använder PutWorksheetDateFilter API med SDK:n

### PutWorksheetDateFilter API-specificering


<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">OpenAPI-specificeringen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till moln-API:n med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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



### Använd Aspose.Cells Cloud SDK:n

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljnivådetaljer så att du kan fokusera på dina projektuppgifter. Kontrollera <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}