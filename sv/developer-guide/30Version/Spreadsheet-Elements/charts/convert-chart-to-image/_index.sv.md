---
title: "Konvertera Excel-diagram till bild – Aspose.Cells Cloud REST API"
type: docs
url: /sv/charts/to-image/
aliases: [  /sv/convert-charts-to-image/ ]
weight: 50
keywords: "Aspose.Cells Cloud, diagram till bild, Excel-diagramkonvertering, REST API, bildformat, PNG, JPEG, BMP, TIFF, GIF"
description: "Lär dig hur du konverterar Excel-diagramobjekt till PNG-, JPEG-, BMP-, TIFF- eller GIF-bilder med Aspose.Cells Cloud REST API. Innehåller slutpunktsinformation, parametrar, cURL-exempel, SDK-utdrag, svarsexempel och felhantering."
ArticleTitle: "Konvertera Excel-diagram till bild – Aspose.Cells Cloud REST API"
---

Denna REST API visar hur man konverterar ett **Excel-diagram** till en bild med **Aspose.Cells Cloud**.

## PutWorksheetAddChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

Stödda bildformat inkluderar `png`, `jpeg`, `bmp`, `tiff` och `gif`.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn  | Typ     | Plats  | Beskrivning                     |
| -------------- | ------- | ------ | ------------------------------- |
| name           | string  | path   | Dokumentnamn.                   |
| sheetName      | string  | path   | Arbeidsbladsnamn.               |
| chartNumber    | integer | path   | Diagramnumret.                  |
| format         | string  | query  | Det exporterade filformatet.    |
| folder         | string  | query  | Dokumentmappen.                 |
| storageName    | string  | query  | Lagringsnamn.                   |

### **Svar**

Slutpunkten returnerar bildfilen i det begärda formatet som en binär ström (t.ex. `byte[]`). Svarsheadern `Content-Type` matchar det valda bildformatet, t.ex. `image/png`, `image/jpeg`, etc.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                            |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. ej stött filtyp). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PutWorksheetAddChart API med SDK:er

### PutWorksheetAddChart API-specificering

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">OpenAPI-specificeringen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

Exempel kommer snart.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}