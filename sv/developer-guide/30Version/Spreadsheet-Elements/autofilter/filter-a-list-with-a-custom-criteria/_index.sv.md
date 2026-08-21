---
title: "Lägg till ett anpassat kriterium i ett Excel-arbetsark"
second_title: "Document"
linktype: "Lägg till anpassat filter"
type: docs
url: /sv/autofilter/add-custom-filter/
aliases: [/sv/filtera-en-lista-med-ett-anpassat-kriterium/,/sv/autofilter/lagg-till-ett-anpassat-filter/]
keywords: "Excel, anpassat filter, Aspose.Cells Cloud, REST API, autofilter, arbetsark, anpassat kriterium"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att lägga till ett anpassat filter i ett Excel-arbetsark. Innehåller begärandetext, ett cURL-exempel och SDK-kodfragment för flera programmeringsspråk."
weight: 65
ArticleTitle: "Lägg till ett anpassat kriterium i ett Excel-arbetsark – Aspose.Cells Cloud API"
---

Denna REST API filtrerar en lista med hjälp av ett **anpassat kriterium**.

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar:

| Parameternamn    | Typ     | Plats                        | Beskrivning                                                                 |
|------------------|---------|------------------------------|-----------------------------------------------------------------------------|
| name             | string  | path                         | Namn på Excel-filen.                                                        |
| sheetName        | string  | path                         | Namn på arbetsarket som innehåller data som ska filtreras.                 |
| range            | string  | query                        | Cellomfång som filtret ska tillämpas på (t.ex. `A1:B1`).                   |
| fieldIndex       | integer | query                        | Nollbaserat index för kolumnen som filtret ska tillämpas på.               |
| operatorType1    | string  | query                        | Förjämförelseoperator (t.ex. `LessOrEqual`, `Equal`).                      |
| criteria1        | string  | query                        | Första filtervärdet eller uttrycket.                                        |
| isAnd            | boolean | query                        | Om `true`, kombineras de två kriterierna med **OCH**; annars **ELLER**.    |
| operatorType2    | string  | query                        | Andra jämförelseoperator (valfritt).                                        |
| criteria2        | string  | query                        | Andra filtervärdet eller uttrycket (valfritt).                             |
| matchBlanks      | boolean | query                        | När `true`, ingår tomma celler i filterresultaten.                        |
| refresh          | boolean | query                        | Om `true`, tvingar arbetsarket att uppdateras efter tillämpning av filtret.|
| folder           | string  | query                        | Mappväg i lagringen där filen finns.                                       |
| storageName      | string  | query                        | Namn på lagringstjänsten.                                                   |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betyder                     | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder PutWorksheetCustomFilter API med SDK:er

### PutWorksheetCustomFilter API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
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


### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på din projekttjänst. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

För andra AutoFilter-åtgärder, såsom att lägga till ett standardfilter eller ett datumfilter, se relaterade dokumentationssidor i AutoFilter-sektionen.