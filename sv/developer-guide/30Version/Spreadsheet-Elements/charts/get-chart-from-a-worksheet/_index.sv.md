---
title: "Hämta diagram från ett kalkylblad"
type: docs
url: /sv/charts/get/
aliases: [/sv/get-chart-from-a-worksheet/]
weight: 10
keywords: "Aspose.Cells Cloud, hämta diagram, kalkylblad, REST API, Excel, diagram-API, diagramhämtning, Excel-diagram"
description: "Hämta diagraminformation, inklusive metadata och exportformat, från ett kalkylblad med Aspose.Cells Cloud REST API."
ArticleTitle: "Hämta diagram från ett kalkylblad – Aspose.Cells Cloud API"
---

Detta REST API hämtar diagraminformation.

**Förutsättningar** – För att anropa denna slutpunkt måste du ha ett giltigt Aspose.Cells Cloud-konto, en aktiv lagringsplats och ett JWT-åtkomsttoken. Hämta token enligt instruktionerna i autentiseringshandboken innan du gör några API-förfrågningar.

## GetWorksheetChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Förfrågningsparameter

| Parameternamn   | Typ     | Plats  | Beskrivning                                  |
| --------------- | ------- | ------ | -------------------------------------------- |
| name            | string  | path   | Namn på Excel-filen.                         |
| sheetName       | string  | path   | Namn på kalkylbladet som innehåller diagrammet. |
| chartNumber     | integer | path   | Nollbaserat index för det diagram som ska hämtas. |
| format          | string  | query  | Önskat exportformat (t.ex. png, jpeg).       |
| folder          | string  | query  | Mapp sökväg där dokumentet lagras.           |
| storageName     | string  | query  | Namn på lagringstjänsten.                    |


### **Svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Diagram 1",
    "Type": "Stapel",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token.                    |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.  |
| 500 | Internt serverfel           | Oväntat serverfel.                                 |

## Hur du använder GetWorksheetChart API med SDK:er

### GetWorksheetChart API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Diagram 1",
    "Type": "Stapel",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}