---
title: "Lägg till en färgfilter i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Lägg till färgfilter"
type: docs
url: /sv/autofilter/add-color-filter/
aliases: [  /sv/filter-a-list-using-a-color-filter/ , /sv/autofilter/add-a-color-filter/ ]
keywords: "Excel, färgfilter, Aspose.Cells Cloud, REST API, autofilter, JWT-autentisering"
description: "Lär dig hur du tillämpar ett färgfilter på ett Excel-arbetsblad med Aspose.Cells Cloud API. Innehåller endpoint, parametrar, cURL-exempel, felhantering och SDK-exempel."
weight: 65
ArticleTitle: "Lägg till ett färgfilter i ett Excel-arbetsblad med Aspose.Cells Cloud API"
---

Lär dig hur du lägger till ett färgfilter i ett Excel-arbetsblad med Aspose.Cells Cloud API. Denna guide täcker nödvändiga endpoints, parametrar, autentiseringskrav, exempel på cURL-förfrågan, SDK-exempel och svarshanteringslogik.

Denna REST API lägger till ett **färgfilter** i ett Excel-arbetsblad.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud APIs är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Förfrågningsparametrar:


| Parameternamn  | Typ     | Plats   | Beskrivning                                                                 |
|----------------|---------|---------|-----------------------------------------------------------------------------|
| name           | string  | path    | Namnet på Excel-filen.                                                      |
| sheetName      | string  | path    | Namnet på arbetsbladet som innehåller data som ska filtreras.              |
| range          | string  | query   | Cellomfång till vilken filtret tillämpas (t.ex. `A1:B10`).                 |
| fieldIndex     | integer | query   | Nollbaserat index för kolumnen som färgfiltret tillämpas på.               |
| colorFilter    | object  | body    | JSON-objekt som definierar för- och bakgrundsfärger som ska filtreras.     |
| matchBlanks    | boolean | query   | Om rader med tomma celler ska ingå i filterresultaten.                     |
| refresh        | boolean | query   | Om `true`, uppdateras arbetsbladet efter att filtret tillämpats.           |
| folder         | string  | query   | Mappen i lagringen där Excel-filen finns.                                  |
| storageName    | string  | query   | Namnet på lagringstjänsten (t.ex. Aspose Cloud Storage).                   |

**`colorFilter` JSON-schema**

| Egenskap          | Typ    | Beskrivning                                                                    | Obligatorisk |
|-------------------|--------|--------------------------------------------------------------------------------|--------------|
| Pattern           | string | Filtermönster (t.ex. `"Solid"`).                                              | Ja           |
| ForegroundColor   | object | Definierar förgrundsfärgen. Innehåller underegenskaper såsom `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` och `Type`. | Nej |
| BackgroundColor   | object | Definierar bakgrundsfärgen. Samma underegenskaper som `ForegroundColor`.      | Nej |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel. |
## Hur man använder PutWorksheetColorFilter API med SDK:er

### PutWorksheetColorFilter API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även:** [Lägg till ett anpassat filter](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [Lägg till ett datumfilter](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [Ta bort ett autofilter](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).