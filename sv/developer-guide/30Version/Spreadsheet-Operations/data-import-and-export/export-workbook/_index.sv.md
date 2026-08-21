---
title: "Exportera arbetsbok"
second_title: "Dokument"
linktitle: "Arbetsbok"
type: docs
url: /export-excel-to-different-formats/
aliases: [/export/excel-to-different-formats/]
keywords: "Aspose.Cells Cloud, Excel-export, konvertering av arbetsbok, PDF, CSV, JSON, bildformat, Spreadsheet API, XLSX, ODS, PNG"
description: "Ett steg-för-steg-guide för hur man exporterar Excel-arbetsböcker till flera format — inklusive PDF, CSV, JSON och diverse bildtyper — med Aspose.Cells Cloud REST API och SDK:er."
weight: 20
---

Du kan exportera arbetsböcker till något av följande format: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begäraparametrar

| Parameter Name | Typ    | Path/Query String/HTTP Body | Obligatorisk | Beskrivning                                               |
|----------------|--------|-----------------------------|--------------|-----------------------------------------------------------|
| file           | fil    | formData                    | Ja           | Fil som ska laddas upp                                    |
| objectType     | sträng | query                       | Ja           | Objekttypen som ska exporteras. För diagramexport använd `chart`. Andra möjliga värden är `worksheet`, `picture`, etc. |
| format         | sträng | query                       | Ja           | Önskat utdataformat. Stödda värden: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |


### **Svar**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                      |
|-----|-----------------------|--------------------------------------------------|
| 200 | OK                    | Objekt exporterades framgångsrikt; svaret innehåller fillistan. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar.              |
| 401 | Oauktoriserad         | Ogiltig eller saknad åtkomsttoken.              |
| 413 | Payload för stor      | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel     | Oväntat serverfel.                               |


## Hur man använder PostExport API med SDK:er

### PostExport API-specifikation


[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man anropar Cloud API:et med cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK påskyndar utvecklingen eftersom den hanterar detaljer på lägre nivå, så att du kan fokusera på affärslogiken. En komplett lista över Aspose.Cells Cloud SDK:er finns i [GitHub-lagret](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänsten med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}