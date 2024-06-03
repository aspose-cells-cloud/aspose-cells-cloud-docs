---
title: Impor
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API stödjer import av data till Excel filer. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 31
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Import
---
Att importera data till en Excel-fil är en komplex process. Många faktorer bidrar till komplexiteten och bör därför beaktas under exportprocessen. Möjligheten att importera typer av format och typer av data till filen med en exakt professionell kvalitet är en toppfunktion i Aspose.Cells Cloud.

## RSET API:er

Följande API:er för att importera data till en Excel-fil eller flera Excel-filer tillhandahålls:

|API|Beskrivning|
|:- |:- |
|[POST /celler/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importera data till Excel-filer utan att använda lagringsutrymme.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importera data till filen Excel med hjälp av lagring.|

## Begär parametrar
 
### Utan att använda förvaring

| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| fil| fil| formData| Fil att ladda upp|
| Importalternativ| Importalternativ| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

### Med användning av förvaring

| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg||
| mapp| sträng| fråga||
| lagringsnamn| sträng| fråga| lagringsnamn.|
| importera data|| kropp||


### Importera dataalternativparameter

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
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>KonverteraNumericData</td><td>Sträng</td> <td>sant falskt.</td> </tr>
    <tr> <td>Första raden</td><td>int</td> <td></td> </tr>
    <tr> <td>Första kolumnen</td><td>int</td><td></td></tr>
    <tr><td>SeparatorString</td><td> Sträng</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>CustomParsers</td><td>Lista<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>CSVData</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
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
    <tr><td>IsVertikal</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>Data</td><td> Sträng[]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>Bild</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
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
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
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
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
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
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
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
    <tr><td>IsVertikal</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>Data</td><td> Heltal[]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>IntegerArray</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
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
    <tr><td>IsVertikal</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>Data</td><td> Dubbel[]</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>DoubleArray</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr> <td>UpperLeftRow</td><td>int</td> <td></td> </tr>
    <tr> <td>Övre vänstra kolumnen</td><td>int</td><td></td></tr>
    <tr> <td>Nedre högerrad</td><td>int</td> <td></td> </tr>
    <tr> <td>Nedre högerkolumn</td><td>int</td><td></td></tr>
    <tr><td>Filnamn</td><td>Sträng</td><td></td></tr>
    <tr><td>Data</td><td> Sträng</td> <td></td></tr>
    <tr> <td>Destinationsarbetsblad</td><td> Sträng</td><td> Namn på målarbetsblad.</td></tr>
    <tr><td>IsInsert</td><td>Sträng</td><td>sant falskt.</td></tr>
    <tr><td>ImportDataType</td><td> Sträng</td><td>StringArray</td></tr>
    <tr> <td>Källa</td><td> FileSource</td><td>Indikerar datafilens position när BatchData-parametern är null.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td> <td></td> </tr>
    <tr><td>columnIndex</td><td>int</td><td></td></tr>
    <tr><td>typ</td><td>Sträng</td><td>data typ</td></tr>
    <tr><td>värde</td><td> Sträng</td> <td></td></tr>
    <tr><td>stil</td><td> Stil(objekt)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beskrivning</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>Sträng</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Sökväg</td><td>Sträng</td><td> fil position</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Hur man anropar RSET API:er

Följande artiklar förklarar varje API hur man ringer i detalj och innehåller cURL och SDK-exempel på varje API:

- [Hur man importerar data till Excel-filer utan att använda lagring.](/cells/sv/import/without-using-storage)
- [Hur man importerar data till Excel-filer med hjälp av lagring.](/cells/sv/import/with-using-storage)
- [Hur man importerar batchdata till Excel arbetsblad](/cells/sv/import/batch-data/)
- [Hur man importerar CSV-data till Excel arbetsblad](/cells/sv/import/csv-data/)
- [Hur man importerar bild till Excel arbetsblad](/cells/sv/import/picture/)
- [Så här importerar du Integer Array till Excel kalkylblad](/cells/sv/import/integer-array/)
- [Hur man importerar Double Array till Excel kalkylblad](/cells/sv/import/double-array/)
- [Hur man importerar String Array till Excel kalkylblad](/cells/sv/import/string-array/)
- [Så här importerar du 2 Dimension Integer Array till Excel kalkylblad](/cells/sv/import/2dimension-integer-array/)
- [Hur man importerar 2 Dimension Double Array till Excel kalkylblad](/cells/sv/import/2dimension-double-array/)
- [Hur man importerar 2 Dimension String Array till Excel kalkylblad](/cells/sv/import/2dimension-string-array/)
