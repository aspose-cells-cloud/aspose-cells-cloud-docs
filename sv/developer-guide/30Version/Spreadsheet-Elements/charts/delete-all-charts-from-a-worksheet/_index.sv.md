---
title: "Ta bort alla diagram från ett kalkylblad"
type: docs
url: /charts/clear/
aliases: [/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, moln, ta bort, alla diagram, kalkylblad, REST API, DELETE, SDK"
description: "Lär dig hur du tar bort alla diagram från ett kalkylblad med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, cURL-exempel, SDK-kodavsnitt, autentiseringssteg och felhantering."
ArticleTitle: "Ta bort alla diagram från ett kalkylblad med Aspose.Cells Cloud API"
---

Denna REST API tar bort alla diagram från det angivna kalkylbladet.

**Bakgrund** – Att ta bort alla diagram från ett kalkylblad är användbart när du behöver återställa kalkylbladets visuella layout, ersätta föråldrade visualiseringar eller förbereda en arbetsbok för återanvändning utan att behålla tidigare diagramdata.

Innan du anropar API:et, se till att följande förutsättningar är uppfyllda:

- Ett giltigt JWT-token är tillgängligt för autentisering.  
- Arbetsboksfilen finns på den angivna lagringsplatsen och i den angivna mappen.  
- Du använder API-version **v3.0**.

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

### Begäransparametrar

| Parameter_name | Typ    | Plats  | Beskrivning                              |
| -------------- | ------ | ------ | ---------------------------------------- |
| name           | string | path   | Namn på arbetsboksfilen.                 |
| sheetName      | string | path   | Namn på kalkylbladet.                    |
| folder         | string | query  | Mapp där arbetsboken är lagrad.          |
| storageName    | string | query  | Namn på lagringen.                       |

**Begäranshuvuden**

| Header        | Beskrivning                     |
|---------------|---------------------------------|
| Authorization | Bearer `<jwt token>`            |
| Accept        | `application/json`              |
| Content-Type  | `application/json` (inget brödtext) |

**Begäransbrödtext**

DELETE-operationen kräver **inte** en begäransbrödtext.

**Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod  | Betydelse                   | Beskrivning                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Oautentiserad               | Ogiltigt eller saknat JWT-token. |
| 413  | För stor nyttolast          | Uppladdad fil överskrider storleksgränsen. |
| 500  | Internt serverfel           | Oväntat serverfel. |

*Exempel på felaktiga svar*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Ogiltig parameter: 'sheetName' krävs."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Autentisering misslyckades. Ogiltigt JWT-token."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "Begärans nyttolast överskrider den högsta tillåtna storleken."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "Ett oväntat fel uppstod på servern."
}
```

## Hur du använder DeleteWorksheetClearCharts API med SDK:er

### DeleteWorksheetClearCharts API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
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

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen när du behöver **ta bort alla diagram** från ett kalkylblad. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---