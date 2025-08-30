---
title: Importieren Sie Daten in Excel-Dateien und exportieren Sie Daten aus Excel-Dateien
second_title: Aspose.Cells Cloud Documen
linktitle: Importieren und Exportieren von Daten
type: docs
url: /de/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: Erstellen Sie neue Dokumente oder Berichte, die Diagramme, Tabellen und andere Datenvisualisierungselemente enthalten können
weight: 25
kwords: Excel Datenimport vs. direkter Datenbankzugriff; Batch-Datenimport vs. zeilenweises Schreiben von Daten; automatisierter Datenexport vs. manuelle Datenextraktion.
---
Aspose.Cells Cloud API unterstützt den Import von Daten aus einer Vielzahl von Datenquellen und kann Daten aus Excel, Diagrammen und Tabellen in verschiedene Formate exportieren, darunter Excel, CSV, PDF, HTML, PNG usw. Dies macht die Datenverwaltung und -freigabe einfach und effizient.

## So importieren Sie Daten aus verschiedenen Datenquellen

Der Import von Daten in eine Excel-Datei ist ein komplexer Prozess. Viele Faktoren tragen zur Komplexität bei und sollten daher beim Export berücksichtigt werden. Die Möglichkeit, verschiedene Formate und Datentypen in präziser, professioneller Qualität in die Datei zu importieren, ist ein herausragendes Merkmal von Aspose.Cells Cloud.

### Informationen zu Daten-APIs importieren

Die folgenden APIs zum Importieren von Daten in eine Excel-Datei oder mehrere Excel-Dateien werden bereitgestellt:

|API|Beschreibung|
|:- |:- |
|[POST /Zellen/Import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Importieren Sie Daten in Excel-Dateien, ohne Speicher zu verwenden.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Importieren Sie Daten mithilfe des Speichers in die Datei Excel.|

### Anforderungsparameter

#### Ohne Speichernutzung

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Datei| Datei| formData| Hochzuladende Datei|
| ImportOption| Importoptionen| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

#### Mit der Verwendung von Speicher

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg||
| Ordner| Schnur| Abfrage||
| Speichername| Schnur| Abfrage| Speichername.|
| Importdaten|| Körper||

#### Parameter für die Option „Daten importieren“

**Die wichtigen Parameter sind in der folgenden Tabelle beschrieben**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parameter</th><th scope="col">Typ</th> <th scope="col">Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr> <td>Batchdaten</td><td>Liste<CellValue></td> <td>Batchdaten</td> </tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>TwoDimensionStringBatchDataArray</td></tr>
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
    <tr> <td>NumerischeDaten konvertieren</td><td>Zeichenfolge</td> <td>wahr/falsch.</td> </tr>
    <tr> <td>Erste Reihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Erste Spalte</td><td>int</td><td></td></tr>
    <tr><td>Trennzeichenfolge</td><td> Zeichenfolge</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>Benutzerdefinierte Parser</td><td>Liste<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>CSV-Daten</td></tr>
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
    <tr><td>IsVertical</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>Daten</td><td> Zeichenfolge[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>Bild</td></tr>
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
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>TwoDimensionIntArray</td></tr>
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
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>Zweidimensionales Doppelarray</td></tr>
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
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>Zweidimensionales String-Array</td></tr>
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
    <tr><td>IsVertical</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>Daten</td><td> Ganze Zahl[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>IntegerArray</td></tr>
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
    <tr><td>IsVertical</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>Daten</td><td> Doppelt[]</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>DoppelArray</td></tr>
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
    <tr> <td>Obere linke Spalte</td><td>int</td><td></td></tr>
    <tr> <td>UntereRechteReihe</td><td>int</td> <td></td> </tr>
    <tr> <td>Untere Rechte Spalte</td><td>int</td><td></td></tr>
    <tr><td>Dateiname</td><td>Zeichenfolge</td><td></td></tr>
    <tr><td>Daten</td><td> Zeichenfolge</td> <td></td></tr>
    <tr> <td>ZielArbeitsblatt</td><td> Zeichenfolge</td><td> Name des Zielarbeitsblatts.</td></tr>
    <tr><td>IsInsert</td><td>Zeichenfolge</td><td>wahr/falsch.</td></tr>
    <tr><td>ImportDataType</td><td> Zeichenfolge</td><td>Zeichenfolgen-Array</td></tr>
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
    <tr><td>Spaltenindex</td><td>int</td><td></td></tr>
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

## So exportieren Sie Excel-Objekte in verschiedene Dateiformate

 Wenn Sie ursprünglich eine Excel-Datei in einem bestimmten Format erstellt haben, wie[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , Und[CSV](https://docs.fileformat.com/spreadsheet/csv/) kann es manchmal sinnvoll sein, die Excel-Datei in ein anderes Format zu konvertieren, um die speziellen Funktionen der Datei nutzen zu können. Beispielsweise möchten Sie eine Excel-Datei exportieren nach[PDF](https://docs.fileformat.com/pdf/)um Ihre Inhalte vor unbefugten Änderungen zu schützen und das gleichzeitige Lesen und Teilen zu erleichtern.

Der Export von Excel-Objekten ist ein komplexer Prozess. Viele Faktoren tragen zur Komplexität bei und sollten daher beim Export berücksichtigt werden. Die Möglichkeit, Excel-Objekte in eine Datei in präziser, professioneller Qualität zu exportieren, ist ein Top-Feature von Aspose.Cells Cloud.

 Es funktioniert perfekt für Arbeitsmappen, Diagramme, Formen und Bilder, die aus Excel-Dateien exportiert werden. Sie können folgende Formate exportieren:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) . Die Nur-Export-Formate:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [ZAHLEN](https://docs.fileformat.com/spreadsheet/numbers/), [Lebensmittel](https://docs.fileformat.com/spreadsheet/fods/).

Bei der Anfrage handelt es sich um eine HTTP-Anfrage mit mehrteiligem Inhalt (siehe[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die Datendatei und der zweite enthält Speicheroptionen.

Die REST API `export`-Arbeitsmappe und interne Objekte in Dateien mit unterschiedlichem Format.

### Export API Informationen

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Datei| Datei| formData| Hochzuladende Datei|
| Objekttyp| Schnur| Abfrage| Objekttyp (Arbeitsmappe/Arbeitsblatt/Diagramm/Form/Bild/Listenobjekt/Oleobjekt)|
| Format| Schnur| Abfrage|[Dateiformat](/cells/de/supported-file-formats/)  |

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an Cloud API tätigen.

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

## So rufen Sie Import- und Export-APIs auf

Die folgenden Artikel erklären detailliert, wie jeder API aufgerufen wird, und enthalten cURL und SDK-Beispiele für jeden API:

- [So importieren Sie Daten in Excel-Dateien, ohne Speicher zu verwenden.](/cells/de/import/without-using-storage)
- [So importieren Sie Daten mithilfe von Speicher in Excel-Dateien.](/cells/de/import/with-using-storage)
- [So importieren Sie Batchdaten in das Arbeitsblatt Excel](/cells/de/import-batch-data-into-excel-worksheet/)
- [So importieren Sie CSV-Daten in das Arbeitsblatt Excel](/cells/de/import-csv-data-into-excel-worksheet/)
- [So importieren Sie ein Bild in das Arbeitsblatt Excel](/cells/de/import-picture-into-excel-worksheet/)
- [So importieren Sie ein Integer-Array in das Arbeitsblatt Excel](/cells/de/import-integer-array-into-excel-worksheet/)
- [So importieren Sie ein Double Array in das Arbeitsblatt Excel](/cells/de/import-double-array-into-excel-worksheet/)
- [So importieren Sie ein String-Array in das Arbeitsblatt Excel](/cells/de/import-string-array-into-excel-worksheet/)
- [So importieren Sie ein 2-dimensionales Integer-Array in das Arbeitsblatt Excel](/cells/de/import-a-2D-integer-array-into-excel-worksheet/)
- [So importieren Sie ein zweidimensionales Doppelarray in das Arbeitsblatt Excel](/cells/de/import-a-2D-double-array-into-excel-worksheet/)
- [So importieren Sie ein 2-dimensionales Zeichenfolgenarray in das Arbeitsblatt Excel](/cells/de/import-a-2D-string-array-into-excel-worksheet/)
- [Exportieren Sie das Diagramm Excel in ein anderes Dateiformat](/cells/de/export-excel-chart-to-different-formats/)
- [Exportieren Sie das Listenobjekt Excel in ein anderes Dateiformat](/cells/de/export-excel-listobject-to-different-formats/)
- [Exportieren Sie Excel OLE-Objekt in ein anderes Dateiformat](/cells/de/export-excel-ole-object/)
- [Exportieren Sie das Bild Excel in ein anderes Dateiformat](/cells/de/export-excel-picture-to-different-formats/)
- [Exportieren Sie die Form Excel in ein anderes Dateiformat](/cells/de/export-excel-shape-to-different-formats/)
- [Exportieren Sie die Arbeitsmappe Excel in ein anderes Dateiformat](/cells/de/export-excel-to-different-formats/)
- [Exportieren Sie das Arbeitsblatt Excel in ein anderes Dateiformat](/cells/de/export-excel-worksheet-to-different-formats//)
