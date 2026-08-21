---
title: "Daten in Excel-Dateien importieren und Daten aus Excel-Dateien exportieren"
second_title: "Dokument"
linktitle: "Datenimport und -export"
type: docs
url: /de/data-import-and-export/
keywords: "Aspose.Cells Cloud, Daten importieren, Excel exportieren, API, CSV, JSON, Bild, Array"
description: "Erfahren Sie, wie Sie Daten aus CSV, JSON, Arrays und Bildern in Excel-Dateien importieren sowie Arbeitsmappen, Diagramme und Formen in PDF, PNG und weitere Formate mit der Aspose.Cells Cloud API (v3.0) exportieren können."
weight: 25
---

Die Aspose.Cells Cloud API unterstützt den Import von Daten aus einer Vielzahl von Quellen und kann Excel-Arbeitsmappen, Diagramme und andere Objekte in verschiedene Formate exportieren, darunter **XLSX**, **CSV**, **PDF**, **HTML**, **PNG** und mehr. Dies macht das Datenmanagement und die Datenteilung einfach und effizient.

**API-Version:** **v3.0** – Letzte Aktualisierung: **2024‑03‑15**

### Schnellstartanleitung

1. **Payload vorbereiten** – Erstellen Sie einen JSON-Body, der die Import- oder Exportoptionen beschreibt (z. B. `ImportCSVDataOption`, `ExportOptions`).
2. **Anfrage senden** – Verwenden Sie `curl`, Postman oder ein SDK, um den entsprechenden Endpunkt aufzurufen (`POST /cells/import` oder `POST /cells/export`).
3. **Antwort verarbeiten** – Bei Erfolg erhalten Sie die verarbeitete Datei (binär oder Base64). Bei einem Fehler prüfen Sie den HTTP-Statuscode sowie die im JSON-Body zurückgegebene Fehlermeldung.

#### Voraussetzungen

- Ein aktives Aspose Cloud-Konto und ein gültiges JWT-Token.
- Die Zielarbeitsmappe muss im angegebenen Speicherort vorhanden sein (für speicherbasierte APIs).
- Richtiges `Content-Type`-Header („multipart/form-data“ für Datei-Uploads, „application/json“ für JSON-Body).

## Daten aus verschiedenen Datenquellen importieren

Das Importieren von Daten in eine Excel-Datei erfordert verschiedene Überlegungen, die während des Vorgangs berücksichtigt werden müssen. Die Fähigkeit, viele Formate und Arten von Daten mit professioneller Qualität zu importieren, ist eine der wichtigsten Funktionen von Aspose.Cells Cloud.

### API-Informationen zum Datenimport

Folgende APIs stehen zum Importieren von Daten in eine oder mehrere Excel-Dateien zur Verfügung:

| API                                                                                                | Beschreibung                                                           |
| :------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | Daten in Excel-Dateien importieren, ohne Speicher zu verwenden.       |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Daten in eine Excel-Datei importieren, die in der Cloud gespeichert ist. |

### Anforderungsparameter

#### Ohne Verwendung von Speicher

| Parametername | Typ    | Position | Beschreibung                              |
| :------------ | :----- | :------- | :---------------------------------------- |
| file          | Datei  | formData | Hochzuladende Datei                       |
| ImportOption  | ImportOptions | body | Gibt das Importformat an (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### Mit Verwendung von Speicher

| Parametername | Typ          | Position | Beschreibung                  |
| :------------ | :----------- | :------- | :---------------------------- |
| name          | string       | path     | Name der Excel-Datei          |
| folder        | string       | query    | Ordnerpfad im Speicher        |
| storageName   | string       | query    | Name des Speichers            |
| importData    | ImportOptions | body     | Nutzdaten für den Datenimport |

#### Parameter für die Importoption

**Die wichtigsten Parameter sind in den folgenden Tabellen beschrieben:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>Zu importierende Stapeldaten</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>Gibt an, ob numerische Daten konvertiert werden sollen (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>Index der ersten Zeile</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index der ersten Spalte</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>Spaltentrennzeichen</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Benutzerdefinierte Parserkonfigurationen</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index der ersten Zeile</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index der ersten Spalte</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Gibt an, ob das Bild vertikal platziert wird (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>Bilddaten (Base64-Zeichenfolgen)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index der ersten Zeile</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index der ersten Spalte</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>Zweidimensionales ganzzahliges Array</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index der ersten Zeile</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index der ersten Spalte</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>Zweidimensionales Double-Array</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index der ersten Zeile</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index der ersten Spalte</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>Zweidimensionales String-Array</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index der ersten Zeile</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index der ersten Spalte</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Gibt an, ob das Array vertikal ist (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>Eindimensionales ganzzahliges Array</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index der ersten Zeile</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index der ersten Spalte</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Gibt an, ob das Array vertikal ist (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>Eindimensionales Double-Array</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Index der oberen linken Zeile</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Index der oberen linken Spalte</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>Index der unteren rechten Zeile</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Index der unteren rechten Spalte</td></tr>
    <tr><td>Filename</td><td>string</td><td>Name der Quelldatei</td></tr>
    <tr><td>Data</td><td>string</td><td>Zu importierende Zeichenfolgendaten</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Name des Zielblatts</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Gibt an, ob Daten eingefügt werden sollen (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Speicherort der Datendatei, wenn BatchData null ist</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Zeilenindex der Zelle</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Spaltenindex der Zelle</td></tr>
    <tr><td>type</td><td>string</td><td>Datentyp des Zellwerts</td></tr>
    <tr><td>value</td><td>string</td><td>Zellwert</td></tr>
    <tr><td>style</td><td>Style (Objekt)</td><td>Zellstildefinition</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Typ</th><th>Beschreibung</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem oder RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>Pfad zur Quelldatei</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Excel-Objekte in verschiedene Dateiformate exportieren

Wenn Sie eine Excel-Datei ursprünglich in einem Format wie **XLS**, **XLSX**, **XLSB** oder **CSV** erstellt haben, möchten Sie diese möglicherweise in ein anderes Format konvertieren, um bestimmte Funktionen zu nutzen. Beispielsweise schützt der Export in **PDF** den Inhalt vor unbefugten Änderungen und macht ihn gleichzeitig einfach lesbar und teilbar.

Beim Exportieren von Excel-Objekten sind verschiedene Faktoren zu berücksichtigen. Aspose.Cells Cloud bietet qualitativ hochwertigen Export von Arbeitsmappen, Diagrammen, Formen und Bildern in eine Vielzahl von Formaten:

_Nur-Export-Formate_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
_Sowohl Import als auch Export_: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

Die Anfrage nutzt mehrteiligen Inhalt gemäß [RFC 2046] und [RFC 1341]. Der erste Teil enthält die Datendatei; der zweite Teil enthält die Speicheroptionen.

### API-Informationen zum Export

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### Anforderungsparameter

| Parametername | Typ    | Position | Beschreibung                                                                                  |
| :------------ | :----- | :------- | :-------------------------------------------------------------------------------------------- |
| file          | Datei  | formData | Hochzuladende Datei                                                                           |
| objectType    | string | query    | Objekttyp (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format        | string | query    | Gewünschtes Ausgabedateiformat (siehe [Unterstützte Dateiformate](/cells/supported-file-formats/)) |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle, mit der Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

Sie können das cURL-Befehlszeilentool verwenden, um die API aufzurufen. Das folgende Beispiel zeigt eine Anfrage und ihre JSON-Antwort.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### Häufige HTTP-Statuscodes

| Status | Bedeutung                                                    | Empfohlene Aktion                           |
| ------ | ------------------------------------------------------------ | ------------------------------------------- |
| 200    | Erfolg – die Datei wurde exportiert                          | Zurückgegebene Datei(en) verarbeiten        |
| 400    | Ungültige Anforderung – fehlende oder ungültige Parameter  | Anforderungsnutzlast und Abfragezeichenfolgen prüfen |
| 401    | Nicht autorisiert – ungültiges oder abgelaufenes JWT-Token | Token aktualisieren und erneut versuchen    |
| 404    | Nicht gefunden – die angegebene Arbeitsmappe oder das angegebene Blatt existiert nicht | Dateinamen und Speicherpfad überprüfen      |
| 500    | Interner Serverfehler – unerwarteter Zustand auf dem Server | Aspose-Support mit der Anforderungs-ID kontaktieren |

## Import- und Export-APIs aufrufen

Die folgenden Artikel erläutern jede API im Detail und enthalten cURL- und SDK-Beispiele:

- [Daten in Excel-Dateien importieren, ohne Speicher zu verwenden.](/cells/import/without-using-storage)
- [Daten in Excel-Dateien importieren, mit Speicher.](/cells/import/with-using-storage)
- [Stapeldaten in Excel-Blatt importieren](/cells/import-batch-data-into-excel-worksheet/)
- [CSV-Daten in Excel-Blatt importieren](/cells/import-CSV-data-into-excel-worksheet/)
- [Bild in Excel-Blatt importieren](/cells/import-picture-into-excel-worksheet/)
- [Ganzzahl-Array in Excel-Blatt importieren](/cells/import-integer-array-into-excel-worksheet/)
- [Double-Array in Excel-Blatt importieren](/cells/import-double-array-into-excel-worksheet/)
- [String-Array in Excel-Blatt importieren](/cells/import-string-array-into-excel-worksheet/)
- [2-dimensionales Ganzzahl-Array in Excel-Blatt importieren](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [2-dimensionales Double-Array in Excel-Blatt importieren](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [2-dimensionales String-Array in Excel-Blatt importieren](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Excel-Diagramm in anderes Dateiformat exportieren](/cells/export-excel-chart-to-different-formats/)
- [Excel-Listenobjekt in anderes Dateiformat exportieren](/cells/export-excel-listobject-to-different-formats/)
- [Excel-OLE-Objekt in anderes Dateiformat exportieren](/cells/export-excel-ole-object/)
- [Excel-Bild in anderes Dateiformat exportieren](/cells/export-excel-picture-to-different-formats/)
- [Excel-Form in anderes Dateiformat exportieren](/cells/export-excel-shape-to-different-formats/)
- [Excel-Arbeitsmappe in anderes Dateiformat exportieren](/cells/export-excel-to-different-formats/)
- [Excel-Blatt in anderes Dateiformat exportieren](/cells/export-excel-worksheet-to-different-formats/)

---