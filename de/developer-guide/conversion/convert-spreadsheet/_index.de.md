---
title: Aspose.Cells Cloud Web API - Konvertieren Sie eine Tabelle in eine Datei mit einem anderen Format
second_title: Documen
ArticleTitle: Convert a Spreadsheet to another format file
linktitle: Tabellenkalkulation konvertieren
type: docs
url: /de/convert-spreadsheet/
keywords: spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local file
description: Konvertiert mühelos eine Tabelle von einem lokalen Laufwerk in verschiedene angegebene Formate mithilfe der Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulationskonvertierung, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen
---
Konvertieren Sie eine lokale Tabellenkalkulations-/Excel-Datei mit dem Aspose.Cells Cloud Web API in eine Datei mit einem anderen Format.

|**Ausgabeformat**|**Beschreibung**|
|:- |:- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - 2003 Arbeitsbuch.|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|Das Office Open XML SpreadsheetML-Dateiformat.|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel Binäres Arbeitsbuch.|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel Arbeitsmappe mit Makros.|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 Vorlage.|
|[XLTX](https://docs.fileformat.com/spreadsheet/xltx/)|Excel Vorlage.|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel Makrofähige Vorlage.|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|Eine Excel Makro-fähige Add-In-Datei, die verwendet wird, um Excel neue Funktionen hinzuzufügen.|
|[CSV](https://docs.fileformat.com/spreadsheet/csv/)|CSV-Datei (Comma Separated Value).|
|[TSV](https://docs.fileformat.com/spreadsheet/tsv/)|TSV-Datei (Tab-getrennte Werte).|
|[TXT](https://docs.fileformat.com/word-processing/txt/)|Durch Trennzeichen getrennte reine Textdatei.|
|[HTML](https://docs.fileformat.com/web/html/)|HTML-Format.|
|[MHTML](https://docs.fileformat.com/web/mhtml/)|MHTML-Datei.|
|[ODS](https://docs.fileformat.com/spreadsheet/ods/)|ODS (OpenDocument-Tabellenkalkulation).|
|SpreadsheetML|Excel 2003 XML-Datei.|
|[Zahlen](https://docs.fileformat.com/spreadsheet/numbers/)|Das Dokument wird von der Anwendung „Numbers“ von Apple erstellt, die Teil der iWork office-Suite von Apple ist, einer Reihe von Anwendungen, die auf den Betriebssystemen Mac OS X und iOS laufen.|
|[JSON](https://docs.fileformat.com/web/json/)|JavaScript-Objektnotation|
|[DIF](https://docs.fileformat.com/spreadsheet/dif/)|Datenaustauschformat.|
|[DBF](https://docs.fileformat.com/database/dbf/)|Die Datei mit der Erweiterung .dbf ist eine Datenbankdatei, die von einer Datenbankverwaltungssystemanwendung namens dBASE verwendet wird.|
|[PDF](https://docs.fileformat.com/pdf/)|Adobe Portable Document Format.|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|XML-Papierspezifikationsformat.|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|Skalierbares Vektorgrafikformat.|
|[TIFF](https://docs.fileformat.com/image/tiff/)|Markiertes Bilddateiformat|
|[PNG](https://docs.fileformat.com/image/png/)|Portable Network Graphics Format|
|[BMP](https://docs.fileformat.com/image/bmp/)|Bitmap-Bildformat|
|[EMF](https://docs.fileformat.com/image/emf/)|Erweitertes Metadateiformat|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG ist ein Bildformat, das mit der Methode der verlustbehafteten Komprimierung gespeichert wird.|
|[GIF](https://docs.fileformat.com/image/gif/)|Grafisches Austauschformat|
|[MARKDOWN](https://docs.fileformat.com/word-processing/md/)|Stellt ein Markdown-Dokument dar.|
|[SXC](https://docs.fileformat.com/spreadsheet/sxc/)|Ein XML-basiertes Format, das von OpenOffice und StarOffice verwendet wird|
|[Lebensmittel](https://docs.fileformat.com/spreadsheet/fods/)|Dies ist ein Open Document-Format, das als flaches XML gespeichert wird.|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|Ein bekanntes Format für Microsoft Word-Dokumente, das eine Kombination aus XML- und Binärdateien ist.|
|[PPTX](https://docs.fileformat.com/presentation/pptx/)|Das PPTX-Format basiert auf dem offenen XML-Präsentationsdateiformat Microsoft PowerPoint.|
|[SQLScript](https://docs.fileformat.com/database/sql/)|Strukturierte Abfragesprache.|
|[XHtml](https://docs.fileformat.com/web/xhtml/)|XHTML ist ein textbasiertes Dateiformat mit Markup im XML, das eine Neuformulierung von HTML 4.0 verwendet.|
|[Epub](https://docs.fileformat.com/ebook/epub/)|Dateien mit der Erweiterung .epub sind ein E-Book-Dateiformat, das Verlegern und Verbrauchern ein standardisiertes digitales Veröffentlichungsformat bietet.|
|[XML](https://docs.fileformat.com/web/xml/)|XML steht für Extensible Markup Language, die HTML ähnelt, sich aber in der Verwendung von Tags zum Definieren von Objekten unterscheidet.|
|[Ots](https://docs.fileformat.com/spreadsheet/ots/)|Öffnen Sie die OTS-Datei (Document Template Sheet).|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW ist ein von Amazon für seine Kindle-Geräte entwickeltes Dateiformat für digitale E-Books. AZW3, auch bekannt als Kindle Format 8 (KF8).|

## **Tabellenkalkulation konvertieren API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Kalkulationstabelle|Datei|FormData|Laden Sie die zu konvertierende Tabellenkalkulationsdatei hoch.|
|Format|Zeichenfolge|Abfrage|(Erforderlich) Das gewünschte Ausgabeformat (z. B. „Xlsx“, „Pdf“, „Csv“).|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad, in dem die konvertierte Arbeitsmappe gespeichert wird. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Geben Sie einen Speichernamen für die Ausgabedatei an.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Verwenden Sie benutzerdefinierte Schriftarten für die Tabelle.|
|Region|Zeichenfolge|Abfrage|Geben Sie die Einstellung für den Tabellenbereich an.|
|Passwort|Zeichenfolge|Abfrage|Das Kennwort zum Öffnen der Tabellenkalkulationsdatei, falls diese geschützt ist.|

### **Antwort**

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

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Warum sollten Sie die Convert-Tabelle API verwenden?

- Kein Cloud-Speicher erforderlich, wodurch die Belastung der Cloud-Ressourcen reduziert wird.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## Wie verwende ich die Konvertierungstabelle API mit SDKs?

### Konvertieren Sie die Tabellenkalkulation API Spezifikation

 Der[Konvertieren Sie die Tabellenkalkulation API Spezifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, eine Tabellenkalkulationsdatei mit einem kurzen Code in eine Datei in einem anderen Format zu konvertieren.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

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
