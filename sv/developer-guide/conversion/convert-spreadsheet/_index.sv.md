---
title: Aspose.Cells Cloud Web API - Konvertera ett kalkylblad till en annan filformat
second_title: Documen
ArticleTitle: Convert a Spreadsheet to another format file
linktitle: Konvertera kalkylblad
type: docs
url: /sv/convert-spreadsheet/
keywords: spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local file
description: Konverterar enkelt ett kalkylblad från en lokal hårddisk till olika angivna format med hjälp av Excel API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylbladskonvertering, PDF, CSV, JSON, Markdown, Matcha alla tomma celler i ett Excel-kalkylblad
---
Konvertera en lokal kalkylbladsfil/Excel till en fil i ett annat format med Aspose.Cells Cloud Web API.

|**Utformat**|**Beskrivning**|
|:- |:- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - 2003 Arbetsbok.|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|Filformatet Office Open XML SpreadsheetML.|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel Binär arbetsbok.|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel Makroaktiverad arbetsbok.|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 Mall.|
|[XLTX](https://docs.fileformat.com/spreadsheet/xltx/)|Excel Mall.|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel Makroaktiverad mall.|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|En Excel makroaktiverad tilläggsfil som används för att lägga till nya funktioner i Excel.|
|[CSV-fil](https://docs.fileformat.com/spreadsheet/csv/)|CSV-fil (kommaseparerade värden).|
|[TSV](https://docs.fileformat.com/spreadsheet/tsv/)|TSV-fil (tabbavgränsade värden).|
|[Textmeddelande](https://docs.fileformat.com/word-processing/txt/)|Avgränsad vanlig textfil.|
|[HTML](https://docs.fileformat.com/web/html/)|HTML-formatet.|
|[MHTML](https://docs.fileformat.com/web/mhtml/)|MHTML-filen.|
|[ODS](https://docs.fileformat.com/spreadsheet/ods/)|ODS (OpenDocument-kalkylblad).|
|SpreadsheetML|Excel 2003 XML-fil.|
|[Tal](https://docs.fileformat.com/spreadsheet/numbers/)|Dokumentet skapas av Apples program "Numbers" som ingår i Apples iWork office-svit, en uppsättning program som körs på operativsystemen Mac OS X och iOS.|
|[JSON](https://docs.fileformat.com/web/json/)|JavaScript-objektnotation|
|[DIF](https://docs.fileformat.com/spreadsheet/dif/)|Datautbytesformat.|
|[DBF](https://docs.fileformat.com/database/dbf/)|Filen med filändelsen .dbf är en databasfil som används av ett databashanteringssystem som heter dBASE.|
|[PDF](https://docs.fileformat.com/pdf/)|Adobe Portable Document Format.|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|XML-pappersspecifikationsformat.|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|Skalbart vektorgrafikformat.|
|[TIFF](https://docs.fileformat.com/image/tiff/)|Taggad bildfilformat|
|[PNG](https://docs.fileformat.com/image/png/)|Bärbart nätverksgrafikformat|
|[BMP](https://docs.fileformat.com/image/bmp/)|Bitmappsbildformat|
|[EMF](https://docs.fileformat.com/image/emf/)|Förbättrat metafilformat|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG är en typ av bildformat som sparas med hjälp av metoden för förlustkomprimering.|
|[GIF](https://docs.fileformat.com/image/gif/)|Grafiskt utbytesformat|
|[PRISSÄNKNING](https://docs.fileformat.com/word-processing/md/)|Representerar ett nedskrivningsdokument.|
|[SXC](https://docs.fileformat.com/spreadsheet/sxc/)|Ett XML-baserat format som används av OpenOffice och StarOffice|
|[FODS](https://docs.fileformat.com/spreadsheet/fods/)|Detta är ett Open Document-format som lagras som platt XML.|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|Ett välkänt format för Microsoft Word-dokument som är en kombination av XML- och binära filer.|
|[PPTX](https://docs.fileformat.com/presentation/pptx/)|PPTX-formatet är baserat på det öppna XML-presentationsfilformatet Microsoft PowerPoint.|
|[SqlScript](https://docs.fileformat.com/database/sql/)|Strukturerat frågespråk.|
|[XHTML](https://docs.fileformat.com/web/xhtml/)|XHTML är ett textbaserat filformat med markup i XML, som använder en omformulering av HTML 4.0.|
|[Epub](https://docs.fileformat.com/ebook/epub/)|Filer med filändelsen .epub är ett e-boksfilformat som tillhandahåller ett standardformat för digitala publiceringar för utgivare och konsumenter.|
|[XML](https://docs.fileformat.com/web/xml/)|XML står för Extensible Markup Language som liknar HTML men skiljer sig genom att använda taggar för att definiera objekt.|
|[Ots](https://docs.fileformat.com/spreadsheet/ots/)|Öppna dokumentmallsfilen (OTS).|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW är ett digitalt e-boksfilformat som utvecklats av Amazon för deras Kindle-enheter. AZW3, även känt som Kindle Format 8 (KF8).|

## **Konvertera kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen som ska konverteras.|
|formatera|Sträng|Fråga|(Obligatoriskt) Önskat utdataformat (t.ex. "Xlsx", "Pdf", "Csv").|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där den konverterade arbetsboken ska lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Ange ett lagringsnamn för utdatafilen.|
|teckensnittPlats|Sträng|Fråga|Använd anpassade teckensnitt för kalkylbladet.|
|område|Sträng|Fråga|Ange inställningen för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenordet för att öppna kalkylbladsfilen om den är skyddad.|

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

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Varför ska du använda Konvertera kalkylblad API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man Konvertera kalkylbladet API med SDK:er?

### Konvertera kalkylblad API Specifikation

 De[Konvertera kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan konvertera en kalkylbladsfil till en annan filformat med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{< /tab >}}
{{< /tabs >}}
