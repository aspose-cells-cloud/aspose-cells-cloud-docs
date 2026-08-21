---
title: "Mehrere Spalten in einem Excel-Arbeitsblatt automatisch anpassen"
second_title: "Dokument"
linktitle: "Spalten"
type: docs
url: /de/worksheets/autofit/columns/
aliases: [  /de/autofit-multiple-columns-of-worksheet/ ]
keywords: "Aspose.Cells, Spalten automatisch anpassen, Excel-API, Cloud-Tabellenkalkulation, REST"
description: "Erfahren Sie, wie Sie mehrere Spalten in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) automatisch anpassen. Enthält Endpunkt, Parameter, cURL-Beispiel, Fehlerbehandlung und SDK-Code-Snippets für C#, Java, Python und weitere."
weight: 20
---

Diese REST API passt **mehrere Spalten** in einem Excel-Arbeitsblatt automatisch an.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **Anforderungsparameter**

| Parametername         | Typ     | Ort    | Beschreibung                                                                                                                                     |
| --------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| name                  | string  | path   | Der Dateiname.                                                                                                                                   |
| sheetName             | string  | path   | Der Arbeitsblattname.                                                                                                                            |
| firstColumn           | integer | query  | Der Index der Startspalte.                                                                                                                       |
| lastColumn            | integer | query  | Der Index der Endspalte.                                                                                                                         |
| autoFitterOptions\*   | object  | body   | AutoFit-Optionen (siehe [AutoFit-Optionen](/cells/auto-fitter-options/)). Enthält `AutoFitMergedCells`, `IgnoreHidden` und `OnlyAuto`.         |
| firstRow              | integer | query  | Der Index der Startzeile für die automatische Anpassung (**optional**).                                                                         |
| lastRow               | integer | query  | Der Index der Endzeile für die automatische Anpassung (**optional**).                                                                           |
| folder                | string  | query  | Ordnerpfad im Speicher (**optional**).                                                                                                           |
| storageName           | string  | query  | Name des Speichers (**optional**).                                                                                                               |

\*Der Parametername ist als Link zur zugehörigen Dokumentation dargestellt.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie mithilfe von cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}