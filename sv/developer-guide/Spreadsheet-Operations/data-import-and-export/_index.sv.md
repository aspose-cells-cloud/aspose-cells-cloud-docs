---
title: Importera data till Excel-filer och exportera data från Excel-filer
second_title: Aspose.Cells Cloud Documen
linktitle: Importera och exportera data
type: docs
url: /sv/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: Generera nya dokument eller rapporter som kan innehålla diagram, tabeller och andra element för datavisualisering
weight: 25
kwords: Excel dataimport kontra direkt databasåtkomst; batchdataimport kontra rad-för-rad-dataskrivning; automatiserad dataexport kontra manuell dataextrahering.
---
Aspose.Cells Cloud API stöder import av data från en mängd olika datakällor och kan exportera data från Excel, diagram och diagram till olika format, inklusive Excel, CSV, PDF, HTML, PNG, etc. Detta gör datahantering och delning enkel och effektiv.

## Hur man importerar data från olika datakällor

Att importera data till en Excel-fil är en komplex process. Många faktorer bidrar till komplexiteten och bör därför beaktas under exportprocessen. Möjligheten att importera olika format och datatyper till filen med en exakt professionell kvalitet är en av de viktigaste funktionerna i Aspose.Cells Cloud.

### Importera information om data-API:er

Följande API:er för att importera data till en Excel-fil eller flera Excel-filer tillhandahålls:

|API|Beskrivning|
|:- |:- |
|[POST /celler/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importera data till Excel-filer utan att använda lagringsutrymme.|
|[POST /celler/{namn}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importera data till filen Excel med hjälp av lagring.|

### Begäranparametrar

#### Utan att använda lagringsutrymme

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| fil| fil| formulärData| Fil att ladda upp|
| Importalternativ| Importalternativ| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

#### Med användning av lagring

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg||
| mapp| sträng| fråga||
| lagringsnamn| sträng| fråga| lagringsnamn.|
| importeraData|| kropp||

#### Importera dataalternativparameter

**De viktiga parametrarna beskrivs i följande tabell**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>BatchData</td><td>Lista<CellValue></td> <td>batchdata</td> </tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>Tvådimensionell strängBatchDataArray</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>KonverteraNumeriskData</td><td>Sträng</td> <td>sant/falskt.</td> </tr>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>Separatorsträng</td><td> Sträng</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>AnpassadeParsers</td><td>Lista<CustomParserConfig></td><td></td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>CSV-data</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>ÄrVertikal</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Data</td><td> Sträng[]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>Bild</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>Data</td><td> Heltal[,]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>Tvådimensionell int-array</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>Data</td><td> Dubbel[,]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>Tvådimensionell dubbelmatris</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>Data</td><td> Sträng[,]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>Tvådimensionell strängmatris</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>ÄrVertikal</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Data</td><td> Heltal[]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>Heltalsmatris</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>ÄrVertikal</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Data</td><td> Dubbel[]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>Dubbelmatris</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>Övre vänsterrad</td><td>int</td> <td></td> </tr>
    <tr> <td>Övre vänsterkolumn</td><td>int</td><td></td></tr>
    <tr> <td>Nedre högerrad</td><td>int</td> <td></td> </tr>
    <tr> <td>Nedre högerkolumn</td><td>int</td><td></td></tr>
    <tr><td>Filnamn</td><td>Sträng</td><td></td></tr>
    <tr><td>Data</td><td> Sträng</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>ÄrInfoga</td><td>Sträng</td><td>sant/falskt.</td></tr>
    <tr><td>Importera datatyp</td><td> Sträng</td><td>StringArray</td></tr>
    <tr> <td>Källa</td><td> Filkälla</td><td>Anger datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr><td>radindex</td><td>int</td> <td></td> </tr>
    <tr><td>kolumnindex</td><td>int</td><td></td></tr>
    <tr><td>typ</td><td>Sträng</td><td>datatyp</td></tr>
    <tr><td>värde</td><td> Sträng</td> <td></td></tr>
    <tr><td>stil</td><td> Stil (objekt)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr><td>Filkällatyp</td><td>Sträng</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Filsökväg</td><td>Sträng</td><td> filposition</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Hur man exporterar Excel-objekt till olika filformat

 Om du ursprungligen skapade en Excel-fil i ett visst format, som[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) och[CSV-fil](https://docs.fileformat.com/spreadsheet/csv/) kan det ibland vara bra att konvertera Excel-filen till ett annat format så att du kan dra nytta av specialfunktioner som den erbjuder. Du kanske till exempel vill exportera en Excel-fil till[PDF](https://docs.fileformat.com/pdf/) för att skydda ditt innehåll från obehöriga ändringar och göra det enkelt att läsa och dela samtidigt.

Export av Excel-objekt är en komplex process. Många faktorer bidrar till komplexiteten och bör därför beaktas under exportprocessen. Möjligheten att exportera Excel-objekt till en enda filformat med exakt professionell kvalitet är en av de viktigaste funktionerna i Aspose.Cells Cloud.

 Det fungerar perfekt för arbetsböcker, diagram, former och bilder som exporteras från Excel-filer. Du kan exportera formaten:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV-fil](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [Textmeddelande](https://docs.fileformat.com/word-processing/txt/) . Formaten som endast är avsedda för export:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [TAL](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Begäran är en HTTP-begäran med flerdelat innehåll (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)Den första delen av flerdelat innehåll innehåller datafilen och den andra innehåller alternativ för att spara.

REST API `export`-arbetsboken och interna objekt till en fil i olika format.

### Exportera API Information

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| fil| fil| formulärData| Fil att ladda upp|
| objekttyp| sträng| fråga| objekttyp (arbetsbok/kalkylblad/diagram/form/bild/listobjekt/oleobjekt)|
| formatera| sträng| fråga|[Filformat](/cells/sv/supported-file-formats/)  |

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

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

## Hur man anropar import- och export-API:er

Följande artiklar förklarar i detalj hur man anropar varje API och innehåller cURL och SDK-exempel för varje API:

- [Hur man importerar data till Excel-filer utan att använda lagringsutrymme.](/cells/sv/import/without-using-storage)
- [Hur man importerar data till Excel-filer med hjälp av lagring.](/cells/sv/import/with-using-storage)
- [Hur man importerar batchdata till Excel-arbetsbladet](/cells/sv/import-batch-data-into-excel-worksheet/)
- [Hur man importerar CSV-data till Excel-arbetsbladet](/cells/sv/import-csv-data-into-excel-worksheet/)
- [Hur man importerar en bild till ett Excel-arbetsblad](/cells/sv/import-picture-into-excel-worksheet/)
- [Hur man importerar en heltalsmatris till ett Excel-arbetsblad](/cells/sv/import-integer-array-into-excel-worksheet/)
- [Hur man importerar en dubbel array till ett Excel-arbetsblad](/cells/sv/import-double-array-into-excel-worksheet/)
- [Hur man importerar en strängmatris till ett Excel-arbetsblad](/cells/sv/import-string-array-into-excel-worksheet/)
- [Hur man importerar en 2-dimensionell heltalsmatris till ett Excel-arbetsblad](/cells/sv/import-a-2D-integer-array-into-excel-worksheet/)
- [Hur man importerar en 2-dimensionell dubbelmatris till arbetsbladet Excel](/cells/sv/import-a-2D-double-array-into-excel-worksheet/)
- [Hur man importerar en 2-dimensionell strängmatris till arbetsbladet Excel](/cells/sv/import-a-2D-string-array-into-excel-worksheet/)
- [Exportera Excel-diagrammet till ett annat filformat](/cells/sv/export-excel-chart-to-different-formats/)
- [Exportera Excel list-objekt till ett annat filformat](/cells/sv/export-excel-listobject-to-different-formats/)
- [Exportera Excel ole-objekt till ett annat filformat](/cells/sv/export-excel-ole-object/)
- [Exportera Excel-bilden till ett annat filformat](/cells/sv/export-excel-picture-to-different-formats/)
- [Exportera Excel-formen till ett annat filformat](/cells/sv/export-excel-shape-to-different-formats/)
- [Exportera arbetsboken Excel till ett annat filformat](/cells/sv/export-excel-to-different-formats/)
- [Exportera Excel-arbetsbladet till ett annat filformat](/cells/sv/export-excel-worksheet-to-different-formats//)
