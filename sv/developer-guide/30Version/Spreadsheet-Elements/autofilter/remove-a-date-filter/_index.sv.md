---
title: "Ta bort ett datumfilter – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Ta bort datumfilter"
type: docs
url: /sv/autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, ta bort datumfilter, Excel AutoFilter, REST API, SDK"
description: "Lär dig hur du tar bort ett datumfilter från ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar slutpunkt, parametrar, HTTPS-cURL-exempel, svarsnyttolast och SDK-kodexempel."
ArticleTitle: "Ta bort ett datumfilter – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API tar bort ett datumfilter från ett Excel-ark.

**Förutsättningar:** Se till att du har en giltig JWT-token, att arbetsboken lagras i Aspose Cloud-lagring och att du har lämpliga behörigheter för att ändra arket.

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn        | Typ     | Plats  | Beskrivning                                                                                      |
|----------------------|---------|--------|--------------------------------------------------------------------------------------------------|
| name                 | sträng  | path   | Namn på Excel-filen.                                                                             |
| sheetName            | sträng  | path   |Arkets namn.                                                                                      |
| fieldIndex           | heltal  | query  | Nollbaserat index för kolumnen som filtret tillämpas på.                                        |
| dateTimeGroupingType | sträng  | query  | Grupperingstyp för datumfiltret (t.ex. Year, Month, Day).                                       |
| year                 | heltal  | query  | Årskomponent för filtret (standardväde 0).                                                      |
| month                | heltal  | query  | Månadskomponent för filtret (standardväde 0).                                                   |
| day                  | heltal  | query  | Dagkomponent för filtret (standardväde 0).                                                      |
| hour                 | heltal  | query  | Timkomponent för filtret (standardväde 0).                                                      |
| minute               | heltal  | query  | Minutkomponent för filtret (standardväde 0).                                                    |
| second               | heltal  | query  | Sekundkomponent för filtret (standardväde 0).                                                   |
| folder               | sträng  | query  | Mappväg i lagringen där filen finns.                                                            |
| storageName          | sträng  | query  | Namn på Aspose Cloud-lagringen.                                                                  |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs         | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel           | Oväntat serverfel.                                      |

API:et returnerar standard-HTTP-statuskoder som indikerar resultatet av borttagningsåtgärden.

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Datumfiltret togs framgångsrikt bort; svaret innehåller åtgärdens status. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs         | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel           | Oväntat serverfel.                                      |

## Hur du använder DeleteWorksheetDateFilter API med SDK:er

### DeleteWorksheetDateFilter API-specifikation

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
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

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}