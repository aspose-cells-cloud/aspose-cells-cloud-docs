---
title: "Beräkna cellformel – Aspose.Cells Cloud API"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, beräkna cellformel, Excel API, REST API, SDK"
description: "Beräkna en Excel-cellformel via Aspose.Cells Cloud REST API (v3.0). Inkluderar endpoint, parametrar, cURL-exempel och SDK-utdrag."
ArticleTitle: "Beräkna cellformel – Aspose.Cells Cloud API-dokumentation"
---

## REST API

Detta REST API beräknar **cellformeln** i en Excel-arbetsbok.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Begäranparametrar

| Parameter Name | Typ    | Parameterplats (path/query/body) | Beskrivning                                                          |
| -------------- | ------ | -------------------------------- | -------------------------------------------------------------------- |
| name           | string | path                             | Namn på Excel-filen (t.ex. `Book1.xlsx`).                           |
| sheetName      | string | path                             | Namn på kalkylbladet som innehåller cellen.                         |
| cellName       | string | path                             | Adress till cellen som ska beräknas (t.ex. `A1`).                   |
| options        | object | body                             | JSON-objekt med beräkningsalternativ (se tabellen **Options object**). |
| folder         | string | query                            | Mapp i lagringen där filen finns.                                   |
| storageName    | string | query                            | Namn på Aspose Cloud-lagringen.                                      |

#### Options object

| Fält          | Typ     | Beskrivning                                                                    | Standardvärde |
| ------------- | ------- | ------------------------------------------------------------------------------ | ------------- |
| CalcStackSize | string  | Maximal storlek för beräkningsstacken.                                         | `"1"`         |
| IgnoreError   | boolean | Om `true`, ignoreras beräkningsfel och cellvärdet sätts till `#N/A`.          | `false`       |
| Recursive     | boolean | Aktiverar rekursiv beräkning av beroende celler.                               | `false`       |
| Precision     | string  | Antal decimaler för numeriska resultat.                                        | `"15"`        |
| UseThreading  | boolean | Aktiverar flertrådad beräkning.                                                | `false`       |


### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                   |
|-----|-----------------------------|---------------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                               |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.             |
| 500 | Internal Server Error       | Oväntat serverfel.                                            |

## Hur man använder PostCellCalculate API med SDK:er

### PostCellCalculate API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man anropar Cloud API:et med cURL. **Först måste du erhålla en JWT-token** genom att autentisera mot `/connect/token`-endpoint och ersätta `<jwt token>` med tokenvärdet.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
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

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektsuppgifter. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
---