---
title: "Aspose.Cells Cloud Web API – Summa och räkna efter färg i Excel"
second_title: "Dokument"
ArticleTitle: "Summa, räkna, medelvärde, max, min värden efter färg i kalkylblad/Excel"
LinkTitle: "Aggregera celler efter färg"
type: docs
url: /aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregera, färg, summa, räkna, medelvärde, min, max"
description: "Aggregera Excel-cellerna efter bakgrundsfärg eller teckensnittsfärg (summa, räkna, medelvärde, min, max) med Aspose.Cells Cloud API. Lär dig endpoint, parametrar, autentisering och SDK-exempel."
weight: 100
---

## Översikt

API:et kan utföra databeräkningar baserat på cellernas **färg**. Det kan summera, räkna antalet, beräkna medelvärde samt hitta det högsta och lägsta värdet i ett Excel-kalkylblad enligt cellernas fyllnings- eller teckensnittsfärg.

| Beräkningsåtgärd | Beskrivning                                                |
| :---------------- | :----------------------------------------------------------- |
| Räkna            | Bestäm antalet celler med samma färg.                       |
| Summa            | Beräkna det totala värdet av celler med samma färg.         |
| Max-värde        | Identifiera det högsta värdet bland celler med samma färg.  |
| Min-värde        | Hitta det lägsta värdet bland celler med samma färg.        |
| Medelvärde       | Beräkna medelvärdet av celler med samma färg.               |

## Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parametername   | Typ    | Plats     | Beskrivning                                                     |
| :-------------- | :----- | :-------- | :-------------------------------------------------------------- |
| Spreadsheet     | Fil    | FormData  | Den Excel-arbetsbok som ska bearbetas.                          |
| Worksheet       | String | Query     | Namn på kalkylbladet som innehåller intervallet.                |
| Range           | String | Query     | A‑1-stil-intervall (t.ex. `A1:B10`).                            |
| Operation       | String | Query     | Beräkningsmetod – `Sum`, `Count`, `Average`, `Min` eller `Max`. |
| ColorPosition   | String | Query     | Bestämmer vilken färg som ska utvärderas – `Background`, `Font`.|
| Region          | String | Query     | Kalkylbladets regionsinställning (t.ex. `us-east-1`).          |
| Password        | String | Query     | Lösenord för att öppna en skyddad arbetsbok (valfritt).         |

#### Enumerationer

- **ColorPosition**

  | Värde      | Betydelse                   |
  | :--------- | :-------------------------- |
  | Background | Använd cellens fyllningsfärg.|
  | Font       | Använd cellens teckensnittsfärg.|

**Exempel på multipart/form‑data-begäran**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Svar

Schemat nedan beskriver svarsobjektet. Ett konkret exempel följer efter schemat.

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Exempel på svar (världsverkliga värden)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse               | Beskrivning                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärddetaljer. |
| 400  | Bad Request           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Unauthorized          | Ogiltig eller saknad JWT-token.                                 |
| 413  | Payload Too Large     | Den uppladdade filen överskrider storleksgränsen.               |
| 500  | Internal Server Error | Oväntat serverfel.                                              |

## Var bör vi använda API:et för att aggregera efter färg?

I ett kalkylblad är ofta data från olika kategorier färgkodad. Detta API gör det möjligt att summera, räkna antalet, beräkna medelvärde eller hitta minsta och högsta värde för varje färggrupp, vilket förenklar färgbaserad dataanalys.

## Varför bör du använda API:et för att aggregera efter färg?

API:et erbjuder ett snabbt och pålitligt sätt att utföra färgbaserade beräkningar utan att skriva egen parseringslogik. Det integrerar sömlöst med Aspose.Cells Cloud SDK:er, vilket gör det möjligt för utvecklare att implementera färgbaserad aggregering med bara några rader kod.

## Hur man använder API:et för att aggregera efter färg med SDK:er

### API-specifikation för aggregering efter färg

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">API-specifikationen för aggregering efter färg</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den döljer de lågnivådetaljer som krävs, så att du kan aggregera beräkningar efter cellfärg med bara en kort kodsnutt.  
Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**Anteckningar:**

- När du arbetar med skyddade arbetsböcker inkluderar du den valfria `Password`-queryparametern; annars misslyckas begäran med ett 401-fel.
- Den maximala begärandestorleken för filen `Spreadsheet` är 100 MB. Om du behöver bearbeta större filer bör du överväga att först ladda upp arbetsboken till Aspose Cloud-lagring och referera till den via `Path`-parametern (inte medföljer här).