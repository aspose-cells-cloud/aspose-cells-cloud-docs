---
title: Import
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API unterstützt das Importieren von Daten in Excel-Dateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 31
---
Das Importieren von Daten in eine Excel-Datei ist ein komplexer Vorgang. Viele Faktoren tragen zur Komplexität bei und sollten daher während des Exportprozesses berücksichtigt werden. Die Möglichkeit, verschiedene Formate und Datentypen in präziser professioneller Qualität in die Datei zu importieren, ist ein Top-Feature von Aspose.Cells Cloud.

## RSET-APIs

Die folgenden APIs zum Importieren von Daten in eine Excel-Datei oder mehrere Excel-Dateien werden bereitgestellt:

|API|Beschreibung|
|:- |:- |
|[POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importieren Sie Daten in Excel-Dateien, ohne Speicher zu verwenden.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importieren Sie Daten in die Datei Excel mit Speichernutzung.|

## Anforderungsparameter
 
### Ohne Speicher zu verwenden

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Datei| Datei| Formulardaten| Datei zum Hochladen|
| ImportOption| Importoptionen| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

### Mit der Verwendung von Speicher

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg||
| Ordner| Schnur| Anfrage||
| Speichername| Schnur| Anfrage| Speichername.|
| Daten importieren|| Körper||


### Parameter der Importdatenoption

**Die wichtigen Parameter sind in der folgenden Tabelle beschrieben**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>BatchData</td><td>Aufführen<CellValue></td> <td>Chargendaten</td> </tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Numerische Daten konvertieren</td><td>Schnur</td> <td>wahr falsch.</td> </tr>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>Trennzeichenfolge</td><td> Schnur</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>CustomParser</td><td>Aufführen<CustomParserConfig></td><td></td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>CSV-Daten</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>IstVertikal</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Daten</td><td> Zeichenkette[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>Bild</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>Daten</td><td> Ganze Zahl[,]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>Daten</td><td> Doppelt[,]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>Daten</td><td> Zeichenkette[,]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>IstVertikal</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Daten</td><td> Ganze Zahl[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>GanzzahlArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>IstVertikal</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Daten</td><td> Doppelt[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>DoubleArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>ObereLinkeReihe</td><td>int</td> <td></td> </tr>
    <tr> <td>UpperLeftColumn</td><td>int</td><td></td></tr>
    <tr> <td>LowerRightRow</td><td>int</td> <td></td> </tr>
    <tr> <td>LowerRightColumn</td><td>int</td><td></td></tr>
    <tr><td>Dateinamen</td><td>Schnur</td><td></td></tr>
    <tr><td>Daten</td><td> Schnur</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Schnur</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Schnur</td><td>wahr falsch.</td></tr>
    <tr><td>Datentyp importieren</td><td> Schnur</td><td>StringArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>Zeilenindex</td><td>int</td> <td></td> </tr>
    <tr><td>Spaltenindex</td><td>int</td><td></td></tr>
    <tr><td>Typ</td><td>Schnur</td><td>Datentyp</td></tr>
    <tr><td>Wert</td><td> Schnur</td> <td></td></tr>
    <tr><td>Stil</td><td> Stil (Objekt)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>Schnur</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Dateipfad</td><td>Schnur</td><td> Dateiposition</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## So rufen Sie RSET-APIs auf

Die folgenden Artikel erklären jede API wie man sie anruft im Detail und enthalten cURL und SDK Beispiele für jede API:

- [So importieren Sie Daten in Excel-Dateien, ohne Speicher zu verwenden.](/cells/de/import/without-using-storage)
- [So importieren Sie Daten in Excel-Dateien mit Speichernutzung.](/cells/de/import/with-using-storage)
- [So importieren Sie Chargendaten in das Arbeitsblatt Excel](/cells/de/import/batch-data/)
- [So importieren Sie CSV-Daten in das Arbeitsblatt Excel](/cells/de/import/csv-data/)
- [So importieren Sie ein Bild in das Arbeitsblatt Excel](/cells/de/import/picture/)
- [So importieren Sie ein Integer-Array in das Arbeitsblatt Excel](/cells/de/import/integer-array/)
- [So importieren Sie Double Array in das Arbeitsblatt Excel](/cells/de/import/double-array/)
- [So importieren Sie ein String-Array in das Arbeitsblatt Excel](/cells/de/import/string-array/)
- [So importieren Sie ein zweidimensionales Integer-Array in das Arbeitsblatt Excel](/cells/de/import/2dimension-integer-array/)
- [So importieren Sie ein zweidimensionales Doppelarray in das Arbeitsblatt Excel](/cells/de/import/2dimension-double-array/)
- [So importieren Sie ein zweidimensionales String-Array in das Arbeitsblatt Excel](/cells/de/import/2dimension-string-array/)
