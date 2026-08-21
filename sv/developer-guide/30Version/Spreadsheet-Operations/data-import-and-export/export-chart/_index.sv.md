---
title: "Exportera Excel-diagram"
second_title: "Dokument"
linktitle: "Diagram"
type: docs
url: /sv/export-excel-chart-to-different-formats/
aliases: [  /sv/export/excel-chart-to-different-formats/ ]
description: "Exportera Excel-diagramobjekt till populära format som PNG, JPEG, PDF, SVG, TIFF, EMF, WMF och mer med Aspose.Cells Cloud REST API eller SDK:er. Inkluderar autentisering, ett cURL-exempel och kodexempel för flera språk."
keywords: "Aspose.Cells, exportera diagram, export av Excel-diagram, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, diagramformat, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Exportera Excel-diagram – Dokument"
---

Att exportera diagramobjekt från en Excel-arbetsbok till olika bild- och dokumentformat är ett vanligt krav för rapportering och publicering. Aspose.Cells Cloud tillhandahåller en enkel REST-slutpunkt som konverterar diagram direkt till populära format som PNG, JPEG, PDF, SVG, TIFF, EMF, WMF och mer.

Du kan exportera diagram till följande format: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), och [PDF](https://docs.fileformat.com/pdf/).

**Förutsättningar:**  
- Ett giltigt Aspose.Cells Cloud-konto med en aktiv prenumeration.  
- En OAuth 2.0 Bearer-token (JWT) som erhållits via autentiseringsflödet.  
- Arbetsboksfilen som ska laddas upp (högsta tillåtna storlek < 50 MB).  

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Parametrar för begäran

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-kropp | Obligatorisk | Beskrivning                                                                                                                     |
|---------------|-------|-------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| file          | fil   | formData                      | Ja           | Fil som ska laddas upp                                                                                                          |
| objectType    | sträng | fråga                         | Ja           | Typen av objekt som ska exporteras. Använd `chart` för diagramexport. Andra möjliga värden är `worksheet`, `picture`, etc.     |
| format        | sträng | fråga                         | Ja           | Önskat utdataformat. Stödda värden: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.                          |

### **Svar**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP-statuskoder**

| Kod | Beteende                    | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | Payload för stor            | Den uppladdade filen överskrider storleksbegränsningen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PostExport-API:et med SDK:er

### PostExport API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Alla begäranden måste innehålla en giltig OAuth 2.0 Bearer-token i `Authorization`-headern. Exemplet nedan visar hur man anropar API:et med **cURL** och laddar upp en arbetsbok med multipart/form‑data.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}