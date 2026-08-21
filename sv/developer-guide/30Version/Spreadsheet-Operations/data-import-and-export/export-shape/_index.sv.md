---
title: "Exportera former"
second_title: "Dokument"
linktitle: "Form"
type: docs
url: /sv/export-excel-shape-to-different-formats/
aliases: [  /sv/export/excel-shape-to-different-formats/ ]
keywords: "Exportera former, Aspose.Cells Cloud, Export av Excel-former, Bildformat, REST API, SDK"
description: "Lär dig hur du exporterar Excel-former till olika bildformat (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) med Aspose.Cells Cloud REST API och SDK:er."
weight: 20
ArticleTitle: "Exportera former – Aspose.Cells Cloud"
---

Att exportera former från Excel möjliggör återanvändning av diagraminnehåll över plattformar och program. **Förutsättningar:** ett giltigt JWT-åtkomsttoken och källexcelfilen som ska laddas upp.

Du kan exportera former till följande format: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## PostExport API

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Parametrar för begäran

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-brödtext | Krävs | Beskrivning |
|---------------|--------|----------------------------------|-------|-------------|
| file          | fil    | formData                         | Ja    | Fil som ska laddas upp |
| objectType    | sträng | fråga                            | Ja    | Objekttypen som ska exporteras. För diagramexport använd `chart`. Giltiga värden inkluderar `shape`, `worksheet`, `picture`, etc. |
| format        | sträng | fråga                            | Ja    | Önskat utdataformat. Stödda värden: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **Exempel på begäran**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Svar

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... ytterligare filobjekt ...
  ]
}
```

*Typiska Base64-kodade filinnehåll varierar från några hundra byte till flera megabyte beroende på bildens dimensioner och format.*

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning |
|-----|-----------------------|-------------|
| 200 | OK                    | Formerna exporterades framgångsrikt; svaret innehåller fillistan. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar. |
| 401 | Oauktorisering        | Ogiltigt eller saknat åtkomsttoken. |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel     | Oväntat serverfel. |


## Hur du använder PostExport API med SDK:er

### PostExport API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar Cloud API med cURL.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla mot Aspose.Cells Cloud. En SDK abstraher bort detaljer på lägre nivå och låter dig fokusera på affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}
---