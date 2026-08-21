---
title: "Uppdatera diagrammets andra kategoriaxel"
type: docs
url: /charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, Diagram, Andra kategoriaxel, REST API, Uppdatera diagram, Excel, moln-API"
description: "Lär dig hur du uppdaterar den andra kategoriaxeln i ett diagram i ett Excel-arbetsblad med Aspose.Cells Cloud REST API."
ArticleTitle: "Uppdatera diagrammets andra kategoriaxel – Aspose.Cells Cloud API"
---

Detta REST API uppdaterar den andra kategoriaxeln i ett diagram.

## PostChartSecondCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameternamn | Typ    | Plats  | Beskrivning                                           |
| ------------- | ------ | ------ | ----------------------------------------------------- |
| name          | string | path   | Namnet på Excel-filen.                               |
| sheetName     | string | path   | Namnet på arbetsbladet som innehåller diagrammet.    |
| chartIndex    | integer | path  | Det nollbaserade indexet för det diagram som ska uppdateras. |
| axis          | object | body   | Objektet för den andra kategoriaxeln med de nya inställningarna. |
| folder        | string | query  | Sökvägen till mappen där filen lagras.               |
| storageName   | string | query  | Namnet på lagringstjänsten.                          |

**Autentisering** – API:et kräver en giltig OAuth 2.0-åtkomsttoken. Generera en JWT-token genom att följa [Autentiseringsguiden](https://docs.aspose.cloud/cells/authentication/). Inkludera token i `Authorization`-headern enligt exemplet med cURL nedan.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* axis-inställningar, t.ex. "Title": "Ny axelrubrik", "IsVisible": true */
        }
      }'
```

*Ersätt `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}` och `{storageName}` med dina faktiska värden. Begärandetexten måste innehålla `axis`-objektet med önskade inställningar.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Lyckat svar (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "Ny axelrubrik",
      "IsVisible": true,
      /* ytterligare axelegenskaper */
    }
  }
}
```

**Felaktiga svar**  

| Statuskod | Beskrivning                                     |
|-----------|-------------------------------------------------|
| 400       | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401       | Oauktoriserad – ogiltig eller saknad JWT-token. |
| 404       | Ej hittad – den angivna filen, arbetsbladet eller diagrammet finns inte. |
| 500       | Internt serverfel – oväntat tillstånd på servern. |

```json
{
  "Code": 400,
  "Message": "Ogiltig begäransnyttolast."
}
```

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

SDK:er förenklar utvecklingen genom att hantera detaljer på låg nivå och låta dig fokusera på din affärslogik. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C#-exempelplats -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java-exempelplats -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP-exempelplats -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby-exempelplats -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python-exempelplats -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android-exempelplats -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift-exempelplats -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl-exempelplats -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go-exempelplats -->

{{< /tab >}}

{{< /tabs >}}

**Anteckningar och bästa praxis**

* Parametern `chartIndex` är nollbaserad; det första diagrammet i ett arbetsblad har index 0.  
* API:et stöder både arbetsboksformaten `.xlsx` och `.xls`.  
* Inkludera endast de egenskaper du behöver i `axis`-objektet; ej angivna egenskaper behåller sina nuvarande värden.  
* Följ riktlinjerna för hastighetsbegränsning (normalt 100 begäranden per minut per konto) för att undvika throttling.