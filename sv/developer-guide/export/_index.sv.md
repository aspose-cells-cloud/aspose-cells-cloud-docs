---
title: Exportera arbetsbok och interna objekt till olika former
second_title: Aspose.Cells Cloud Documen
linktitle: Expor
type: docs
url: /sv/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API stöder export av Excel-filer och interna objekt till olika formatfiler. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 31
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Exportera arbetsbok och interna objekt till olika format
---
 Om du ursprungligen har skapat en Excel-fil i ett visst format, t.ex[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , och[CSV](https://docs.fileformat.com/spreadsheet/csv/) kan du ibland tycka att det är användbart att konvertera excel-filen till ett annat format så att du kan dra fördel av specialfunktioner som den tillhandahåller. Du kanske till exempel vill exportera en excel-fil till[PDF](https://docs.fileformat.com/pdf/) för att skydda ditt innehåll från alla obehöriga ändringar och göra det enkelt att läsa och dela samtidigt.

 Excel objektexport är en komplex process. Många faktorer bidrar till komplexiteten och bör därför beaktas under exportprocessen. Möjligheten att exportera Excel-objekt till en filformat med exakt professionell kvalitet är en toppfunktion i Aspose.Cells Cloud.

 Det fungerar perfekt för arbetsbok, diagram, form och bild som exporteras från Excel-fil. Du kan exportera format:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [Text](https://docs.fileformat.com/word-processing/txt/) . Formaten endast för export:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [TAL](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Begäran är en HTTP-begäran med innehåll i flera delar (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av innehållet med flera delar innehåller datafilen och den andra innehåller sparaalternativ.

REST API `export` arbetsbok och interna objekt till olika format fil.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| fil| fil| formData| Fil att ladda upp|
| objectType| sträng| fråga| objekttyp (arbetsbok/kalkylblad/diagram/form/bild/listobjekt/oleobjekt)|
| formatera| sträng| fråga|[Filformat](/cells/sv/supported-file-formats/)  |
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj


 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export.php" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


Följande artiklar förklarar varje API i detalj och innehåller cURL och SDK-exempel på varje API:


1. [Exportera Excel diagram till annat filformat](/cells/sv/export/excel-chart-to-different-formats/)
2. [Exportera Excel listobjekt till annat filformat](/cells/sv/export/excel-listobject-to-different-formats/)
3. [Exportera Excel ole-object till annat filformat](/cells/sv/export/excel-ole-object/)
4. [Exportera Excel bild till annat filformat](/cells/sv/export/excel-picture-to-different-formats/)
5. [Exportera Excel form till annat filformat](/cells/sv/export/excel-shape-to-different-formats/)
6. [Exportera Excel arbetsbok till annat filformat](/cells/sv/export/excel-to-different-formats/)
7. [Exportera Excel kalkylblad till annat filformat](/cells/sv/export/excel-worksheet-to-different-formats//)
