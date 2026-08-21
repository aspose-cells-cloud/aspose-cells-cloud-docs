---
title: "Hämta fyllningsformat för diagramområde – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /sv/charts/chart-area/fill-format/get/
aliases: [  /sv/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Diagramområde"
  - "Fyllningsformat"
  - "REST API"
  - "Excel"
description: "Hämta fyllningsformatet (färg, mönster, gradient) för ett diagramområde i ett Excel-ark via Aspose.Cells Cloud API. Inkluderar cURL-exempel, SDK-kodfragment, autentiseringssteg och svarsdetaljer."
ArticleTitle: "Hämta fyllningsformat för diagramområde – Aspose.Cells Cloud API v3.0"
---

Denna REST API hämtar fyllningsformatinformationen för ett **diagramområde**.

**Förutsättningar**  
För att anropa denna slutpunkt krävs en giltig OAuth/JWT-åtkomsttoken. Skaffa token med Aspose.Cells Clouds autentiseringsflöde och inkludera den i `Authorization`-headern som `Bearer <jwt token>`. Om du använder ett av SDK:erna, se till att SDK:n är konfigurerad med dina `client_id` och `client_secret` innan du anropar metoden.

## GetChartAreaFillFormat API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärningsparametrar

| ParameterName   | Typ    | Plats  | Beskrivning                         |
| --------------- | ------ | ------ | ----------------------------------- |
| name            | string | path   | Arbetsbokens namn.                  |
| sheetName       | string | path   |Arkets namn.                         |
| chartIndex      | integer| path   | Index för diagrammet.               |
| folder          | string | query  | Mapp som innehåller arbetsboken.    |
| storageName     | string | query  | Namn på lagringsplatsen.            |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att komma åt Aspose.Cells-webbtjänster. Exempel nedan visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Anteckningar**  
- En lyckad anrop returnerar HTTP 200 med detaljerad fyllningsformatinformation.  
- HTTP 401 anger ett autentiseringsfel (ogiltig eller saknad token).  
- HTTP 404 returneras när den angivna arbetsboken, arket eller diagramindexet inte finns.  
- HTTP 500 indikerar ett serverfel; försök igen eller kontakta support om problemet kvarstår.

| Kod | Betydelse                                           |
|-----|-----------------------------------------------------|
| 200 | Lyckades – fyllningsformatet returnerades           |
| 401 | Auktorisering misslyckades – ogiltig eller saknad token |
| 404 | Hittades inte – arbetsbok, ark eller diagram hittades inte |
| 500 | Internt serverfel                                   |

Se även slutpunkterna **Get Chart Area Border** (Hämta diagramområdets kant) och **Get Chart Title** (Hämta diagramtitel) för relaterade åtgärder.

{{< /tab >}}

{{< /tabs >}}

## Molntjänstfamilj för SDK

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förvaret</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}
---