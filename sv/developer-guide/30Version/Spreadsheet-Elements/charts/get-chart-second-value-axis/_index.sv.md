---
title: "Hämta andrahandsvärdeaxel för diagram"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, diagram andrahandsvärdeaxel, Excel, REST API, moln, API, Excel-diagramaxel
description: Hämtar andrahandsvärdeaxeln för ett angivet diagram i ett Excel-ark med hjälp av Aspose.Cells Cloud REST API.
ArticleTitle: "Hämta andrahandsvärdeaxel för diagram – Aspose.Cells Cloud API"
---

Denna REST API hämtar andrahandsvärdeaxeln för ett diagram.

## GetChartSecondValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameternamn  | Typ     | Plats   | Beskrivning                                      |
| -------------- | ------- | ------- | ------------------------------------------------ |
| name           | string  | path    | Namnet på Excel-filen.                           |
| sheetName      | string  | path    | Namnet på det kalkylblad som innehåller diagrammet. |
| chartIndex     | integer | path    | Det nollbaserade indexet för diagrammet.        |
| folder         | string  | query   | Mappen där filen är lagrad.                      |
| storageName    | string  | query   | Namnet på Aspose Cloud-lagringen.                |

**Förutsättningar**: En giltig JWT-åtkomsttoken som erhållits via Aspose Cloud OAuth2-flödet måste lämnas i `Authorization`-huvudet för varje begäran.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör en anrop till moln-API:et med cURL. Alla Aspose Cloud-slutpunkter kräver HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Andrahandsvärdeaxel"
  }
}
```

**Svarsfält**

- **Code** – HTTP-statuskod för åtgärden (t.ex. `200` för framgång).  
- **Status** – Textuell beskrivning av statusen (`"OK"` för framgång).  
- **Axis** – Objekt som innehåller information om andrahandsvärdeaxeln:  
  - **AxisId** – Identifikator för axeln.  
  - **IsVisible** – Booleskt värde som anger om axeln visas.  
  - **MinimumScale** – Minsta värde som visas på axeln.  
  - **MaximumScale** – Största värde som visas på axeln.  
  - **MajorUnit** – Intervall mellan stora tick-märken.  
  - **MinorUnit** – Intervall mellan mindre tick-märken.  
  - **Title** – Titeltext för axeln.

**Felsvar** (icke-200)

- `400 Bad Request` – Ogiltiga parametrar eller felaktig begäran.  
- `401 Unauthorized` – Saknad eller ogiltig JWT-token.  
- `404 Not Found` – Angiven fil, kalkylblad eller diagram finns inte.  
- `500 Internal Server Error` – Oväntat serverfel.

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-lagret</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
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