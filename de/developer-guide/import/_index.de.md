---
title: Importieren
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API unterstützt das Importieren von Daten in Excel Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 31
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Importieren
---
Das Importieren von Daten in eine Excel-Datei ist ein komplexer Vorgang. Viele Faktoren tragen zur Komplexität bei und sollten daher beim Exportvorgang berücksichtigt werden. Die Möglichkeit, alle Arten von Formaten und Datentypen in präziser, professioneller Qualität in die Datei zu importieren, ist ein Top-Feature von Aspose.Cells Cloud.

## RSET-APIs

Die folgenden APIs zum Importieren von Daten in eine Excel-Datei oder mehrere Excel-Dateien werden bereitgestellt:

|API|Beschreibung|
|:- |:- |
|[POST /Zellen/Import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importieren Sie Daten in Excel-Dateien, ohne Speicher zu verwenden.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importieren Sie Daten mithilfe des Speichers in die Datei Excel.|

## Anforderungsparameter
 
### Ohne Speichernutzung

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Datei| Datei| Formulardaten| Hochzuladende Datei|
| ImportOption| Importoptionen| HTTPBody| IntArray/DoubleArray/StringArray/ZweidimensionalIntArray/ZweidimensionalDoubleArray/ZweidimensionalStringArray/BatchData/CSVData/Bild|

### Mit der Nutzung von Speicher

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg||
| Ordner| Schnur| Abfrage||
| Speichername| Schnur| Abfrage| Speichername.|
| Daten importieren|| Körper||


### Datenimportoptionsparameter

**Die wichtigen Parameter werden in der folgenden Tabelle beschrieben**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Stapeldaten</td><td>Aufführen<CellValue></td> <td>Batchdaten</td> </tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>Zweidimensionales String-BatchDataArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>NumerischeDatenKonvertieren</td><td>Zeichenfolge</td> <td>wahr falsch.</td> </tr>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>Trennzeichen</td><td> Zeichenfolge</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>BenutzerdefinierteParser</td><td>Aufführen<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>CSVDaten</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
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
    <tr><td>IstVertikal</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>Daten</td><td> Zeichenfolge[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>Bild</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
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
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
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
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>Zweidimensionales Doppelarray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
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
    <tr><td>Daten</td><td> Zeichenfolge[,]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>Zweidimensionales String-Array</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
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
    <tr><td>IstVertikal</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>Daten</td><td> Ganze Zahl[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>IntegerArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
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
    <tr><td>IstVertikal</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>Daten</td><td> Doppelt[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>DoppelArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Obere Linke Zeile</td><td>int</td> <td></td> </tr>
    <tr> <td>Obere Linke Spalte</td><td>int</td><td></td></tr>
    <tr> <td>UntereRechteReihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Untere Rechte Spalte</td><td>int</td><td></td></tr>
    <tr><td>Dateiname</td><td>Zeichenfolge</td><td></td></tr>
    <tr><td>Daten</td><td> Zeichenfolge</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IstEinfügen</td><td>Zeichenfolge</td><td>wahr falsch.</td></tr>
    <tr><td>ImportierenDatentyp</td><td> Zeichenfolge</td><td>ZeichenfolgeArray</td></tr>
    <tr> <td>Quelle</td><td> Dateiquelle</td><td>Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.</td></tr>
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
    <tr><td>SpaltenIndex</td><td>int</td><td></td></tr>
    <tr><td>Typ</td><td>Zeichenfolge</td><td>Datentyp</td></tr>
    <tr><td>Wert</td><td> Zeichenfolge</td> <td></td></tr>
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
    <tr><td>Dateiquellentyp</td><td>Zeichenfolge</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Dateipfad</td><td>Zeichenfolge</td><td> Dateiposition</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## So rufen Sie RSET-APIs auf

Die folgenden Artikel erläutern detailliert, wie API aufgerufen wird, und enthalten cURL und SDK-Beispiele für jeweils API:

- [So importieren Sie Daten in Excel-Dateien, ohne Speicher zu verwenden.](/cells/de/import/without-using-storage)
- [So importieren Sie Daten mithilfe des Speichers in Excel-Dateien.](/cells/de/import/with-using-storage)
- [So importieren Sie Batch-Daten in das Arbeitsblatt Excel](/cells/de/import/batch-data/)
- [So importieren Sie CSV-Daten in das Arbeitsblatt Excel](/cells/de/import/csv-data/)
- [So importieren Sie ein Bild in das Arbeitsblatt Excel](/cells/de/import/picture/)
- [So importieren Sie ein Integer-Array in das Arbeitsblatt Excel](/cells/de/import/integer-array/)
- [So importieren Sie ein Double Array in das Arbeitsblatt Excel](/cells/de/import/double-array/)
- [So importieren Sie ein String-Array in das Arbeitsblatt Excel](/cells/de/import/string-array/)
- [So importieren Sie ein zweidimensionales Integer-Array in das Arbeitsblatt Excel](/cells/de/import/2dimension-integer-array/)
- [So importieren Sie ein zweidimensionales Doppelarray in das Arbeitsblatt Excel](/cells/de/import/2dimension-double-array/)
- [So importieren Sie ein zweidimensionales Zeichenfolgenarray in das Arbeitsblatt Excel](/cells/de/import/2dimension-string-array/)
