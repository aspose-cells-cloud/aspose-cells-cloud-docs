---
title: "Hämta sammanfogade celler från ett Excel-arbetsblad – Aspose.Cells Cloud API"
type: docs
url: /sv/get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, sammanfogade celler, Excel-arbetsblad, REST API, Aspose.Cells SDK, Excel-sammanfogade celler"
description: "Lär dig hur du hämtar intervall med sammanfogade celler från ett Excel-arbetsblad med Aspose.Cells Cloud API (v3.0). Inkluderar autentiseringssteg, fullständig cURL-förfrågan, svarschema, felhantering och SDK-exempel i C#, Java, Python och mer."
---

Detta REST API returnerar information om **sammanfogade celler** i ett Excel-arbetsblad.

> **Obs!** – API-objektet heter **MergedCell** (ental). I texten hänvisar vi till *konceptet* med sammanfogade celler (plural).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parametrar för förfrågan

| Parameternamn    | Typ    | Plats  | Beskrivning                         |
|------------------|--------|--------|-------------------------------------|
| **name**         | string | path   | Filnamnet på Excel-filen.           |
| **sheetName**    | string | path   | Namnet på arbetsbladet.             |
| **folder**       | string | query  | Mapp som innehåller dokumentet.     |
| **storageName**  | string | query  | Namnet på den lagring som ska användas. |

## **Svar**

Returnerar MergedCellsResponse.

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400 | Ogiltig förfrågan           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur du använder GetWorksheetMergedCells API med SDK:er

### GetWorksheetMergedCells API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Exemplet nedan visar hur du gör en förfrågan till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla mot API:et. En SDK hanterar detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}