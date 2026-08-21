---
title: "Arbeitsblattseite exportieren – Aspose.Cells Cloud API Referenz"
ArticleTitle: "Arbeitsblattseite exportieren – Aspose.Cells Cloud API Referenz"
second_title: "Dokument"
linktype: "Seite"
type: docs
url: /de/worksheets/page-to-different-formats/
aliases: [  /de/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, Exportieren einer Arbeitsblattseite, PDF, PNG, CSV, REST API, JWT-Authentifizierung, Dateiformate"
description: "Erfahren Sie, wie Sie eine bestimmte Arbeitsblattseite mit der Aspose.Cells Cloud REST API in PDF, PNG, CSV und weitere Formate exportieren können. Enthält cURL-Anfragen, eine Parameteranleitung und SDK-Beispiele für mehrere Sprachen."
weight: 240
---

Das Exportieren einer bestimmten Arbeitsblattseite ist nützlich, wenn Sie ein druckfähiges Snapshot eines Berichts, ein Diagrammbild oder einen Daten-Auszug benötigen, ohne die gesamte Arbeitsmappe herunterladen zu müssen. Dieser Endpunkt ermöglicht es Ihnen, eine einzelne Seite im Format abzurufen, das am besten für Ihren weiteren Workflow geeignet ist.

Die [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet)-API ermöglicht die Konvertierung einer bestimmten Seite eines Arbeitsblatts in verschiedene Dateiformate. Unterstützte Formate: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

> **Voraussetzungen** – Sie benötigen ein gültiges JWT-Authentifizierungstoken sowie die Arbeitsmappe, die sich in einem Cloud-Ordner befindet, den Sie mit dem Parameter `folder` angeben.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Antwort** – Der Dienst gibt die angeforderte Seite im gewählten Format zurück. Bei Bildformaten (png, jpeg, gif usw.) enthält der Antworttext die binäre Bilddatei; bei Dokumentformaten (pdf, xls, csv usw.) enthält der Antworttext den Dateiinhalt. Ein erfolgreicher Aufruf gibt HTTP 200 zurück.

*Beispiel einer PNG-Antwort (gekürzter Base64-Auszug):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Parameter**

| Parameter              | Typ     | Beschreibung                                                          | Standardwert |
| ---------------------- | ------- | --------------------------------------------------------------------- | ------------ |
| `format`               | string  | Ausgabedateiformat (z. B. `pdf`, `png`, `csv`).                      | `pdf`        |
| `verticalResolution`   | integer | Vertikale DPI des gerenderten Bildes.                                 | `100`        |
| `horizontalResolution` | integer | Horizontale DPI des gerenderten Bildes.                               | `100`        |
| `pageIndex`            | integer | Nullbasiertes Index der zu exportierenden Arbeitsblattseite (`0` = erste Seite). | `0`          |
| `folder`               | string  | Cloud-Speicherordner, in dem sich die Quell-Arbeitsmappe befindet.   | —            |

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                      |
|------|-----------------------------|-------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.            |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                        |

**Mögliche Fehler**

- **401 Unauthorized** – Ungültiger oder fehlender JWT-Token.
- **404 Not Found** – Die angegebene Arbeitsmappe oder das angegebene Arbeitsblatt existiert nicht.
- **400 Bad Request** – Ungültiger Parameterwert (z. B. nicht unterstütztes `format`).
- **500 Internal Server Error** – Unerwartetes serverseitiges Problem.

## Cloud SDK-Familie

Die Verwendung eines SDK ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre ProjektAufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}