---
title: "Hämta värdeaxel för diagram"
type: docs
url: /charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Diagramvärdeaxel, REST API, Excel, molntjänst, hämta diagramvärdeaxel
description: "Aspose.Cells Cloud REST API – Hämta värdeaxeln för ett diagram i ett Excel-ark."
ArticleTitle: "Hämta värdeaxel för diagram - Aspose.Cells Cloud REST API"
---

Denna REST API hämtar värdeaxeln för ett diagram. Den ingår i **Aspose.Cells Cloud REST API** och fungerar med Excel-ark som lagras i molnet.

För relaterade åtgärder, se slutpunkten **[Hämta kategoriaxel för diagram](/charts/category-axis/get/)**.

## GetChartValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameternamn | Typ    | Plats  | Beskrivning                                             |
| ------------- | ------ | ------ | ------------------------------------------------------- |
| name          | string | path   | Namnet på Excel-filen (inklusive filtillägg).          |
| sheetName     | string | path   | Namnet på arbetsbladet som innehåller diagrammet.       |
| chartIndex    | integer | path  | Det nollbaserade indexet för diagrammet inom arbetsbladet. |
| folder        | string | query  | Mappen i molnlagringen där filen finns.                 |
| storageName   | string | query  | Namnet på lagringstjänsten (t.ex. Aspose Cloud).        |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör en anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
 -X GET \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Värden",
    "Format": {
      "NumberFormat": "General",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Möjliga HTTP-statuskoder**

| Kod | Beskrivning                                         |
|-----|-----------------------------------------------------|
| 200 | Lyckades – information om värdeaxeln returneras.   |
| 400 | Felaktig begäran – obligatoriska parametrar saknas eller är ogiltiga. |
| 401 | Auktorisering misslyckades – autentiseringstoken saknas eller är ogiltig. |
| 404 | Hittades inte – den angivna arbetsboken, arbetsbladet eller diagrammet finns inte. |
| 500 | Internt serverfel – ett oväntat fel inträffade på servern. |

Svaret innehåller ett detaljerat `ValueAxis`-objekt med egenskaper såsom `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` och `Format`. I en fullständig implementering kan ytterligare formateringsdetaljer tillhandahållas.

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}