---
title: "Aspose.Cells Cloud Web API – Konvertera kalkylark till annat format – Gratis onlineverktyg"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar ett kalkylark till ett annat format: Steg-för-steg-guide"
linktitle: "Konvertera kalkylark"
type: docs
url: /convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, konvertering av kalkylark, Excel till PDF, Excel API, molnbaserad filkonvertering"
description: "Konvertera ett kalkylarksfil till ett annat format med Aspose.Cells Cloud API."
weight: 100
---

Konvertera ett lokalt kalkylark eller Excel-fil till ett annat format med Aspose.Cells Cloud Web API.

## **Konvertera kalkylark API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärandeparametrar:**

| Parameternamn   | Typ    | Path/Query String/HTTPBody | Beskrivning                                                                                   |
| :-------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------------- |
| Spreadsheet     | Fil    | FormData                   | Ladda upp kalkylarksfilen som ska konverteras.                                                |
| format          | Sträng | Query                      | (Obligatoriskt) Önskat utdataformat (t.ex. "XLSX", "PDF", "CSV").                             |
| outPath         | Sträng | Query                      | (Valfritt) Mappens sökväg där det konverterade arbetsboken ska lagras. Standard är null.     |
| outStorageName  | Sträng | Query                      | Ange ett namn för utdatalagringen.                                                            |
| fontsLocation   | Sträng | Query                      | Använd anpassade teckensnitt för kalkylarket.                                                 |
| region          | Sträng | Query                      | Ange regioninställning för kalkylarket.                                                       |
| password        | Sträng | Query                      | Lösenordet för att öppna kalkylarksfilen om den är skyddad.                                   |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Status vid lyckad åtgärd**

- **200 OK** – Konverteringen lyckades och svarsbodyn innehåller den konverterade filströmmen.
- `Content-Type`-headern återspeglar MIME-typen för det begärda utdataformatet (t.ex. `application/pdf` för PDF).

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filtret applicerades korrekt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | Payload för stor      | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Format

| **Utformat**                                                                                           | **Beskrivning**                                                                                                              |
| :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Excel 95/5.0 - 2003-arbetsbok.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Office Open XML SpreadsheetML-filformatet.                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Excel binär arbetsbok.                                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Excel-makroaktiverad arbetsbok.                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Excel 97 - Excel 2003-mall.                                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Excel-mall.                                                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Excel-makroaktiverad mall.                                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | En Excel-makroaktiverad tilläggfil som används för att lägga till nya funktioner till Excel.                                 |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | CSV-fil (Comma Separated Value).                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | TSV-fil (Tab-separated values).                                                                                               |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | Avgränsad ren-textfil.                                                                                                        |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | HTML-format.                                                                                                                  |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | MHTML-fil.                                                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS (OpenDocument Spreadsheet).                                                                                               |
| SpreadsheetML                                                                                          | Excel 2003 XML-fil.                                                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Dokumentet skapas med Apples "Numbers"-applikation, som är en del av iWork-suiten för macOS och iOS.                         |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript Object Notation.                                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | Data Interchange Format.                                                                                                      |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | En fil med filändelsen .dbf är en databasfil som används av dBASE-databashanteringsystemet.                                 |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe Portable Document Format.                                                                                               |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | XML Paper Specification-formatet.                                                                                            |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | Scalable Vector Graphics-formatet.                                                                                           |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | Tagged Image File Format.                                                                                                     |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | Portable Network Graphics-formatet.                                                                                           |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | Bitmap-bildformat.                                                                                                            |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | Enhanced Metafile-formatet.                                                                                                   |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG är ett bildformat som sparas med förlustkomprimering.                                                                    |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | Graphics Interchange Format.                                                                                                  |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Representerar ett Markdown-dokument.                                                                                          |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | Ett XML-baserat format som används av OpenOffice och StarOffice.                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | Ett Open Document-format lagrat som flat XML.                                                                                 |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Ett välkänt format för Microsoft Word-dokument som kombinerar XML och binära filer.                                          |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | PPTX-formatet är baserat på Microsoft PowerPoint Open XML presentation format.                                               |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | Structured Query Language.                                                                                                    |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML är ett textbaserat filformat med taggar i XML, baserat på en omformulering av HTML 4.0.                                |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | Filer med filändelsen .epub är ett e-boksformat som erbjuder en standard digital publikation för utgivare och konsumenter.   |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML står för Extensible Markup Language; det liknar HTML men använder taggar för att definiera objekt.                       |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Open Document Template Sheet (OTS)-fil.                                                                                      |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW är ett digitalt e-bokfilformat utvecklat av Amazon för Kindle-enheter. AZW3, även känt som Kindle Format 8 (KF8).        |

## Var bör du använda API:et för att konvertera kalkylark?

- **Migrering av äldre system**: Konvertera tusentals äldre XLS-filer till XLSX för moderna system.
- **Standardisering av arkivering**: Normalisera olika kalkylarksformat (XLS, XLSM, ODS, CSV) till ett enda format för arkivering.
- **Överensstämmelse mellan kontorsprogram**: Konvertera Excel-filer till format som är kompatibla med LibreOffice, Google Sheets eller Apple Numbers.
- **Normalisering av datakällor**: Konvertera olika kalkylarksformat till CSV eller JSON för inläsning till databaser.
- **Webbpublicering**: Konvertera finansiella modeller till HTML för visning på webben.

## Varför bör du använda API:et för att konvertera kalkylark?

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kompletteras med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramgenerering minskar detta betydligt utvecklingsarbetet.
- **Kostnadseffektivt**: Du kan konvertera tabelldata utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.
- **Omfattande formatstöd**: Konvertera mellan 20+ kalkylarksformat.
- **Bevara datatrogenhet och formatering.**

## Hur använder du API:et för att konvertera kalkylark med SDK:er?

Följande kodexempel visar hur du använder API:et för att konvertera kalkylark med olika SDK:er.

### API-specifikation för att konvertera kalkylark

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">API-specifikation för att konvertera kalkylark</a> definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljer på låg nivå och låter dig konvertera en kalkylarksfil till ett annat format med kompakt kod. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Konvertera kalkylark",
  "description": "Konvertera en kalkylarksfil till ett annat format med Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Webb",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Konvertera ett kalkylark till det angivna formatet."
    }
  ]
}
</script>

---