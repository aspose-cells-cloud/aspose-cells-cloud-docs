---
title: "Konvertieren einer Excel-Datei in verschiedene Formate"
ArticleTitle: "Konvertieren einer Excel-Datei in verschiedene Formate"
second_title: "Dokument"
linktitle: "Excel konvertieren"
type: docs
url: /de/convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, Excel-Konvertierung, Dateiformatkonvertierung, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Konvertieren Sie Excel-Arbeitsmappen in verschiedene Formate wie CSV, PDF, HTML, JSON, Markdown und weitere mithilfe der Aspose.Cells Cloud REST API."
weight: 10
---

Bevor Sie diesen Endpunkt aufrufen, stellen Sie sicher, dass Sie ein gültiges JWT-Token besitzen und sich die Quelldatei in einem unterstützten Speicherort befindet (z. B. Aspose Cloud Storage). Geben Sie das Token im `Authorization`-Header an und geben Sie ggf. den Abfrageparameter `storageName` an.

Diese REST API konvertiert eine Excel-Datei in verschiedene Ausgabeformate.

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

Die Anfrage ist ein HTTP **PUT** mit multipart-Inhalt (siehe [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Der erste Teil des multipart-Körpers enthält die **Daten-Datei**, der zweite Teil enthält die **Speicheroptionen**.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Abfrageparameter

| Parametername           | Typ    | Beschreibung                                                                                                                |
| ----------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | Ziel-Dateiformat (z. B. CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG usw.).         |
| `password`              | string | Passwort, das zum Öffnen der Quell-Excel-Datei erforderlich ist.                                                           |
| `outPath`               | string | Vollständiger Pfad (einschließlich Dateiname und -erweiterung) für eine einzelne Ausgabedatei bzw. ein Ordnerpfad, wenn mehrere Dateien generiert werden. |
| `storageName`           | string | Name des Speichers, in dem sich die Quelldatei befindet.                                                                   |
| `checkExcelRestriction` | bool   | Wenn **true**, werden Excel-Beschränkungen vor dem Ändern von Zellen oder zugehörigen Objekten überprüft.                 |
| `streamFormat`          | string | Format des Eingabedatenstroms.                                                                                             |
| `region`                | string | Auf die Arbeitsmappe angewendete regionale Einstellungen.                                                                  |
| `pageWideFitOnPerSheet` | bool   | Passt die Seitenbreite an, sodass jedes Arbeitsblatt bei der Konvertierung in PDF vollständig passt.                      |
| `pageTallFitOnPerSheet` | bool   | Passt die Seitenhöhe an, sodass jedes Arbeitsblatt bei der Konvertierung in PDF vollständig passt.                        |
| `sheetName`             | string | Name des Arbeitsblatts, das konvertiert werden soll.                                                                      |
| `pageIndex`             | string | Index der zu konvertierenden Seite (erfordert `sheetName`).                                                                |
| `onePagePerSheet`       | bool   | Wenn **true**, wird eine PDF-Seite pro Arbeitsblatt generiert.                                                            |
| `AutoRowsFit`           | bool   | Passt automatisch alle Zeilen in der Arbeitsmappe an.                                                                     |
| `AutoColumnsFit`        | bool   | Passt automatisch die Spaltenbreiten in der Arbeitsmappe an.                                                              |

### Parameter im Anforderungstext

| Parametername | Typ       | Beschreibung                                                    |
| ------------- | --------- | --------------------------------------------------------------- |
| `datafile`    | data file | Die Excel-Datei, die im ersten Teil des multipart-Körpers übergeben wird. |
| `SaveOptions` | object    | Speicheroptionen, die im zweiten Teil des multipart-Körpers übergeben werden. |

### **Antwort**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; die Antwort enthält Details zum Vorgang.     |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).    |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                      |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Verwendung der PutConvertWorkBook API mit SDKs

### PutConvertWorkBook API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) definiert eine öffentlich zugängliche Schnittstelle, die direkte REST-Interaktionen aus einem Webbrowser ermöglicht.

### cURL-Beispiel

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs beschleunigt die Entwicklung, da niedrigstufige Details automatisch behandelt werden, sodass Sie sich auf die Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---