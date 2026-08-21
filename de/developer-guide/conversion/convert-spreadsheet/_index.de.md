---
title: "Aspose.Cells Cloud Web-API – Konvertieren einer Tabellendatei in ein anderes Format – Kostenloses Online-Tool"
second_title: "Dokument"
ArticleTitle: "So konvertieren Sie eine Tabellendatei in ein anderes Format: Schritt-für-Schritt-Anleitung"
linktitle: "Tabellendatei konvertieren"
type: docs
url: /de/convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, Tabellendateikonvertierung, Excel zu PDF, Excel-API, Cloud-Dateikonvertierung"
description: "Konvertieren Sie eine Tabellendatei mit der Aspose.Cells Cloud API in ein anderes Format."
weight: 100
---

Konvertieren Sie eine lokale Tabellendatei/-Excel-Datei mit der Aspose.Cells Cloud Web-API in ein anderes Format.

## **Konvertieren einer Tabellendatei per API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername     | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                     |
| :---------------- | :----- | :--------------------------------- | :----------------------------------------------------------------------------------------------- |
| Spreadsheet       | Datei  | FormData                           | Laden Sie die zu konvertierende Tabellendatei hoch.                                             |
| format            | String | Abfrage                            | (Erforderlich) Das gewünschte Ausgabeformat (z. B. „XLSX“, „PDF“, „CSV“).                       |
| outPath           | String | Abfrage                            | (Optional) Der Ordnerpfad, in dem die konvertierte Arbeitsmappe gespeichert wird. Standard ist null. |
| outStorageName    | String | Abfrage                            | Geben Sie einen Speichernamen für die Ausgabedatei an.                                          |
| fontsLocation     | String | Abfrage                            | Verwenden Sie benutzerdefinierte Schriftarten für die Tabellendatei.                            |
| region            | String | Abfrage                            | Geben Sie die Regionseinstellung für die Tabellendatei an.                                      |
| password          | String | Abfrage                            | Das Passwort zum Öffnen der schützten Tabellendatei.                                             |

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

**Erfolgsstatus**

- **200 OK** – Die Konvertierung war erfolgreich; der Antworttext enthält den konvertierten Dateistream.
- Der `Content-Type`-Header spiegelt den MIME-Typ des angeforderten Ausgabeformats wider (z. B. `application/pdf` für PDF).

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                    |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.    |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Format

| **Ausgabeformat**                                                                                      | **Beschreibung**                                                                                                             |
| :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Excel 95/5.0 – 2003-Arbeitsmappe.                                                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Das Office Open XML SpreadsheetML-Dateiformat.                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Excel-Binäre Arbeitsmappe.                                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Excel-Arbeitsmappe mit Makrounterstützung.                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Excel 97 – Excel 2003-Vorlage.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Excel-Vorlage.                                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Excel-Vorlage mit Makrounterstützung.                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | Eine Excel-Makroaktivierte-Add-In-Datei, die verwendet wird, um neue Funktionen zu Excel hinzuzufügen.                      |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | CSV-Datei (Comma Separated Value).                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | TSV-Datei (Tab-separated values).                                                                                             |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | Delimitierte Textdatei.                                                                                                       |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | HTML-Format.                                                                                                                  |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | MHTML-Datei.                                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS (OpenDocument Spreadsheet).                                                                                               |
| SpreadsheetML                                                                                          | Excel 2003 XML-Datei.                                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Das Dokument wird mit Apples „Numbers“-Anwendung erstellt, Teil der iWork-Suite für macOS und iOS.                           |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript Object Notation.                                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | Data Interchange Format.                                                                                                      |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | Die Datei mit der Endung .dbf ist eine Datenbankdatei des dBASE-Datenbankverwaltungssystems.                                 |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe Portable Document Format.                                                                                               |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | XML Paper Specification-Format.                                                                                               |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | Scalable Vector Graphics-Format.                                                                                              |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | Tagged Image File Format.                                                                                                     |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | Portable Network Graphics-Format.                                                                                             |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | Bitmap-Bildformat.                                                                                                            |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | Enhanced Metafile-Format.                                                                                                     |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG ist ein Bildformat, das mit verlustbehafteter Komprimierung gespeichert wird.                                           |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | Graphics Interchange Format.                                                                                                  |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Stellt ein Markdown-Dokument dar.                                                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | Ein XML-basiertes Format, das von OpenOffice und StarOffice verwendet wird.                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | Dies ist ein Open Document-Format, das als flache XML-Datei gespeichert wird.                                                |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Ein weit verbreitetes Format für Microsoft Word-Dokumente, das XML- und Binärdateien kombiniert.                             |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | Das PPTX-Format basiert auf dem Microsoft PowerPoint Open XML Presentation-Dateiformat.                                      |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | Structured Query Language.                                                                                                    |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML ist ein textbasiertes Dateiformat mit Markup in XML, basierend auf einer Neufassung von HTML 4.0.                      |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | Dateien mit der Endung .epub sind ein E-Book-Format, das einen standardisierten digitalen Veröffentlichungsstandard darstellt. |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML steht für Extensible Markup Language; es ähnelt HTML, verwendet aber Tags zur Definition von Objekten.                   |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Open Document Template Sheet (OTS)-Datei.                                                                                    |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW ist ein von Amazon für Kindle-Geräte entwickeltes digitales E-Book-Format. AZW3 ist auch als Kindle Format 8 (KF8) bekannt. |

## Wofür sollten Sie die Konvertieren einer Tabellendatei-API verwenden?

- **Migration veralteter Systeme**: Konvertieren Sie Tausende veralteter XLS-Dateien in XLSX für moderne Systeme.
- **Standardisierung der Archivierung**: Normalisieren Sie verschiedene Tabellendateiformate (XLS, XLSM, ODS, CSV) in ein einheitliches Format für die Archivierung.
- **Interoperabilität mit Office-Suiten**: Konvertieren Sie Excel-Dateien in Formate, die mit LibreOffice, Google Sheets oder Apple Numbers kompatibel sind.
- **Datenquellen-Standardisierung**: Konvertieren Sie verschiedene Tabellendateiformate in CSV oder JSON für die Datenbankverarbeitung.
- **Web-Publizierung**: Konvertieren Sie Finanzmodelle in HTML zur Webanzeige.

## Warum sollten Sie die Konvertieren einer Tabellendatei-API verwenden?

- **Entwicklerfreundlich**: Aspose.Cells Cloud bietet SDK-Bibliotheken in mehreren Sprachen, die eine schnelle Entwicklung ermöglichen, und wird mit umfassender Dokumentation geliefert. Im Vergleich zum Aufbau eigener Diagramm-Render-Lösungen reduziert dies den Entwicklungsaufwand erheblich.
- **Kosteneffizient**: Sie können Tabellendaten konvertieren, ohne die Arbeitsmappe zuvor hochzuladen, wodurch Speicherplatz eingespart und Kosten reduziert werden.
- **Umfassende Formatunterstützung**: Konvertieren Sie zwischen über 20 Tabellendateiformaten.
- **Erhalt der Datenintegrität und -formatierung.**

## Wie verwenden Sie die Konvertieren einer Tabellendatei-API mit SDKs?

Die folgenden Codebeispiele zeigen, wie Sie die Konvertieren einer Tabellendatei-API mit verschiedenen SDKs verwenden.

### API-Spezifikation für die Konvertierung einer Tabellendatei

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">API-Spezifikation für die Konvertierung einer Tabellendatei</a> definiert eine öffentlich zugängliche Programmierschnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist die schnellste Möglichkeit zur Entwicklung, da sie niedrigere Detailstufen abstrahiert und es Ihnen ermöglicht, eine Tabellendatei mit kurzen Codezeilen in ein anderes Format zu konvertieren. Sehen Sie sich das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

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
  "name": "Convert Spreadsheet",
  "description": "Konvertieren Sie eine Tabellendatei mit Aspose.Cells Cloud in ein anderes Format.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Konvertieren Sie eine Tabellendatei in das angegebene Format."
    }
  ]
}
</script>

---