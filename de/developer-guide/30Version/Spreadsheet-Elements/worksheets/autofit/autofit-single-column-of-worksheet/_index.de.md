---
title: "Spalte in Excel automatisch anpassen mit der Aspose.Cells Cloud API – Schnellanleitung"
second_title: "Dokument"
linktitle: "Spalte"
type: docs
url: /de/worksheets/autofit/column/
aliases: [  /de/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, Spalte automatisch anpassen, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Erfahren Sie, wie Sie die Breite einer einzelnen Spalte (oder eines zusammenhängenden Spaltenbereichs) in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API automatisch anpassen können. Enthält cURL-Beispiele, SDK-Beispiele (C#, Java, Python usw.) sowie vollständige Anforderungs- und Antwortdetails."
weight: 10
---

Diese REST API passt die Breite einer einzelnen Spalte oder eines zusammenhängenden Spaltenbereichs in einem Excel-Arbeitsblatt automatisch an.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### Anforderungsparameter

| Parametername      | Typ    | Ort   | Beschreibung                                                                                                    |
| ------------------ | ------ | ----- | --------------------------------------------------------------------------------------------------------------- |
| name               | string | path  | Der Name der Excel-Datei.                                                                                       |
| sheetName          | string | path  | Der Name des Arbeitsblatts.                                                                                     |
| firstColumn        | integer | query | Nullbasierter Index der ersten Spalte, deren Breite automatisch angepasst werden soll.                        |
| lastColumn         | integer | query | Nullbasierter Index der letzten Spalte, deren Breite automatisch angepasst werden soll.                       |
| autoFitterOptions  | object | body  | Optionen zur Steuerung des automatischen Anpassungsverhaltens (siehe [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow           | integer | query | Nullbasierter Index der ersten Zeile, die bei der Breitenberechnung berücksichtigt wird.                      |
| lastRow            | integer | query | Nullbasierter Index der letzten Zeile, die bei der Breitenberechnung berücksichtigt wird.                     |
| folder             | string | query | Der Ordner im Speicher, in dem sich die Datei befindet.                                                        |
| storageName        | string | query | Der Name des Speicherdienstes.                                                                                  |

### Fehlerantworten

| HTTP-Status | Bedeutung                                 | Beispiel-JSON-Body                                         |
| ----------- | ----------------------------------------- | ---------------------------------------------------------- |
| 400         | Ungültige Parameter                       | `{"Code":400,"Message":"Ungültiger Parameter 'firstColumn'."}` |
| 401         | Nicht autorisiert – fehlendes oder ungültiges JWT-Token | `{"Code":401,"Message":"Autorisierung fehlgeschlagen."}`    |
| 404         | Datei oder Arbeitsblatt nicht gefunden    | `{"Code":404,"Message":"Arbeitsblatt 'Sheet1' nicht gefunden."}` |
| 500         | Interner Serverfehler                     | `{"Code":500,"Message":"Ein unerwarteter Fehler ist aufgetreten."}` |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das Befehlszeilentool **cURL** verwenden, um Aspose.Cells Cloud-Dienste aufzurufen. Das folgende Beispiel zeigt, wie der „autofit-column“-Endpunkt aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
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

Die Verwendung eines SDKs ist der schnellste Weg, die API in Ihre Anwendung zu integrieren. SDKs übernehmen die Details der niedrigen Ebene, sodass Sie sich auf die Geschäftslogik konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um die vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie der „autofit-column“-Endpunkt mit verschiedenen SDKs aufgerufen wird:

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