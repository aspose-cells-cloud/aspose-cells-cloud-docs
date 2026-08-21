---
title: "Lägg till en ikonfilter i ett Excel-ark"
second_title: "Dokument"
linktitle: "Lägg till ikonfilter"
type: docs
url: /autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud, Excel, Ikonfilter, AutoFilter, REST API"
description: "Lär dig hur du lägger till ett ikonfilter i ett Excel-ark med hjälp av Aspose.Cells Cloud REST API, inklusive begärandedetaljer, cURL-exempel, SDK-kodexempel och felhantering."
weight: 65
ArticleTitle: "Lägg till ett ikonfilter i ett Excel-ark – Aspose.Cells Cloud-dokumentation"
---

## REST API

Denna REST API lägger till ett **ikonfilter** i ett Excel-ark med hjälp av **Aspose.Cells Cloud REST API**.

**Bakgrund:** Ett ikonfilter tillämpar ett visuellt ikonset på celler baserat på deras värden, vilket möjliggör snabb visuell analys av datatrender. Vanliga användningsfall inkluderar att framhäva prestandamätare, statusindikatorer eller kategorisera värden med trafikljus-ikoner direkt i Excel-ark.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begärandeparametrar:

| Parameternamn | Typ    | Plats  | Beskrivning |
|---------------|--------|--------|-------------|
| name          | string | Path   | Arbetsbokens namn. |
| sheetName     | string | Path   | Arkets namn. |
| range         | string | Query  | Cellintervallet (t.ex. `A1:B1`) som filtret ska tillämpas på. |
| fieldIndex    | integer| Query  | Nollbaserat index för den kolumn som filtret riktar sig mot. |
| iconSetType   | string | Query  | Det ikonset som ska användas. Tillåtna värden: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId        | integer| Query  | Identifieraren för den specifika ikonen inom det valda ikonsetet. |
| matchBlanks   | boolean| Query  | Bestämmer om tomma celler inkluderas (`true` eller `false`). |
| refresh       | boolean| Query  | Anger om filtret ska uppdateras efter tillämpning (`true` eller `false`). |
| folder        | string | Query  | Mappen som innehåller den ursprungliga arbetsboken. |
| storageName   | string | Query  | Namnet på lagringsplatsen där arbetsboken finns. |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                    | Beskrivning |
|-----|------------------------------|-------------|
| 200 | OK                           | Filtret har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran             | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad                | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel            | Oväntat serverfel. |
## Hur du använder PutWorksheetIconFilter API med SDK:er

### PutWorksheetIconFilter API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
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

Möjliga svarsstatuskoder:

| Kod | Beskrivning |
|-----|-------------|
| 200 | Filtret har tillämpats framgångsrikt. |
| 400 | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401 | Oautentiserad – ogiltig eller saknad autentiseringstoken. |
| 404 | Arbetsbok, ark eller angivet intervall hittades inte. |
| 500 | Internt serverfel. |
{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivånivå, så att du kan fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

För övriga AutoFilter-funktioner, se dokumentationen för **[Lägg till färgfilter](/autofilter/add-color-filter/)**, **[Lägg till datumfilter](/autofilter/add-date-filter/)** och **[Rensa AutoFilter](/autofilter/clear-autofilter/)**.