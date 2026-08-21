---
title: "Bereich einer Arbeitsmappe in PNG, PDF, CSV exportieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Bereich"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, Bereich einer Arbeitsmappe exportieren, PNG, PDF, CSV, Excel-Konvertierung, REST API, SDK"
description: "Erfahren Sie, wie Sie einen bestimmten Zellbereich aus einer Excel-Arbeitsmappe in PNG, PDF, CSV und über 20 weitere Formate mithilfe der Aspose.Cells Cloud REST API oder SDKs (C#, Java, Python, …) exportieren können."
weight: 230
ArticleTitle: "Bereich einer Arbeitsmappe mit Aspose.Cells Cloud API in PNG, PDF, CSV exportieren – vollständige Anleitung"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API ermöglicht die Konvertierung eines festgelegten Bereichs einer Arbeitsmappe in verschiedene Dateiformate. Unterstützte Formate: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Diese Anleitung zeigt, wie Sie einen **bestimmten Zellbereich** aus einer Excel-Arbeitsmappe in PNG, PDF, CSV und weitere über 20 Formate mithilfe der Aspose.Cells Cloud API exportieren können. Für verwandte Vorgänge wie den Export einer gesamten Arbeitsmappe oder die Konvertierung einer Arbeitsmappe siehe die Seiten **[Gesamte Arbeitsmappe exportieren](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** und **[Arbeitsmappe in PDF konvertieren](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**.

## REST API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Anforderungsparameter

| Parameter                | Typ    | Erforderlich | Beschreibung                                      |
|--------------------------|--------|--------------|---------------------------------------------------|
| `name`                   | string | Ja           | Dateiname der Arbeitsmappe.                       |
| `sheetName`              | string | Ja           | Name der Zielarbeitsmappe.                        |
| `format`                 | string | Ja           | Gewünschtes Ausgabeformat (png, pdf, csv, …).    |
| `area`                   | string | Nein         | Zellbereich für den Export (z. B. `B3:K8`).      |
| `verticalResolution`     | int    | Nein         | Vertikale DPI für Rasterformate.                  |
| `horizontalResolution`   | int    | Nein         | Horizontale DPI für Rasterformate.               |
| `folder`                 | string | Nein         | Cloud-Speicherordner, der die Datei enthält.     |
| `storage`                | string | Nein         | Name des Speicherdienstes.                        |

### Erfolgreiche Antwort

* **200 OK** – Gibt die angeforderte Datei im Binärformat (PNG, PDF, CSV, usw.) zurück.

### Fehlerantworten

| Statuscode | Beschreibung                                           |
|------------|--------------------------------------------------------|
| 400        | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401        | Nicht autorisiert – Authentifizierungstoken fehlt oder ist ungültig. |
| 404        | Nicht gefunden – angegebene Arbeitsmappe oder Arbeitsmappe existiert nicht. |
| 500        | Interner Serverfehler – unerwarteter Zustand auf dem Server. |

**Beispiel für eine Fehlerantwort**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "Der Parameter 'area' ist ungültig. Erwartetes Format: B3:K8."
  }
}
```

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Konvertiertes Bild (binäres PNG)

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstractiert die Details der niedrigen Ebene und ermöglicht es Ihnen, sich auf Ihre Projektlogik zu konzentrieren. Weitere Informationen zu den verfügbaren Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}