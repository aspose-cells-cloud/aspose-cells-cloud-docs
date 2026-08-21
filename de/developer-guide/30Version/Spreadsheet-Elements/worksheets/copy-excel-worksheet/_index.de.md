---
title: "Inhalt und Formate aus einer anderen Arbeitsmappe kopieren."
second_title: "Dokument"
linktitle: "Kopieren"
type: docs
url: /de/worksheets/copy/
aliases: [  /de/copy-excel-worksheet/ ]
keywords: "Aspose Cells API zum Kopieren von Arbeitsblättern, Excel Arbeitsblatt kopieren per REST, Aspose Cloud SDK zum Kopieren, Tabellenkalkulation Arbeitsblatt kopieren"
description: "Erfahren Sie, wie Sie ein Arbeitsblatt und dessen Formatierung in ein neues Blatt innerhalb derselben Arbeitsmappe kopieren können, mithilfe der Aspose.Cells Cloud REST API. Enthält Endpunkte, Parameter, cURL-Beispiele sowie SDK-Beispiele für C#, Java, Python und weitere."
weight: 20
---

Diese REST API kopiert ein Arbeitsblatt und dessen Formatierung in ein neues Blatt innerhalb derselben Arbeitsmappe.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

Die Anfrageparameter sind wie folgt aufgelistet:

| Parametername      | Typ    | Ort    | Beschreibung                                                               |
| ------------------ | ------ | ------ | -------------------------------------------------------------------------- |
| `name`             | string | path   | Der Name der Arbeitsmappendatei.                                           |
| `sheetName`        | string | path   | Der Name des Zielarbeitsblatts (des neuen Blatts).                         |
| `sourceSheet`      | string | query  | Der Name des zu kopierenden Arbeitsblatts.                                 |
| `options`          | object | body   | JSON-Objekt mit Kopieroptionen (z. B. Spaltenbreite, Formeln).            |
| `sourceWorkbook`   | string | query  | Der Name der Quellarbeitsmappe, falls sie sich von der aktuellen unterscheidet. |
| `sourceFolder`     | string | query  | Der Ordnerpfad, in dem sich die Quellarbeitsmappe befindet.               |
| `folder`           | string | query  | Der Ordnerpfad, in dem die Zielarbeitsmappe gespeichert werden soll.      |
| `storageName`      | string | query  | Der Name des zu verwendenden Speicherdienstes.                            |

### Anfrage- und Antwortbeispiele

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Fehlerbehandlung

Die API gibt standardmäßige HTTP-Statuscodes zusammen mit einem JSON-Fehlerbody zurück. Typische Antworten sind:

| HTTP-Code | Beschreibung                                                   | Beispiel für JSON-Fehlerbody                                  |
| --------- | -------------------------------------------------------------- | ------------------------------------------------------------- |
| 400       | Ungültige Anfrage – fehlende oder ungültige Parameter.        | `{ "Code": 400, "Message": "Ungültige Anforderungsparameter." }` |
| 401       | Nicht autorisiert – fehlender oder ungültiger Token.          | `{ "Code": 401, "Message": "Authentifizierung fehlgeschlagen." }` |
| 404       | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Ordner existiert nicht. | `{ "Code": 404, "Message": "Ressource nicht gefunden." }`     |
| 500       | Interner Serverfehler – unerwarteter Zustand.                 | `{ "Code": 500, "Message": "Ein unerwarteter Fehler ist aufgetreten." }` |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}