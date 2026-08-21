---
title: "Bereich in einem Arbeitsblatt mit Einfügeoptionen kopieren"
second_title: "Dokument"
linktitle: "Kopieren"
type: docs
url: /de/ranges/copy/
aliases: [  /de/copy-range-in-a-worksheet-with-paste-options/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, Bereich kopieren, Arbeitsblatt, Einfügeoptionen"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um einen Bereich innerhalb eines Excel-Arbeitsblatts mit vollständiger Unterstützung für Einfügeoptionen zu kopieren. Enthält SDK-Beispiele für mehrere Programmiersprachen."
weight: 20
ArticleTitle: "Bereich in einem Arbeitsblatt mit Einfügeoptionen kopieren – Aspose.Cells Cloud API"
---

Diese REST API kopiert einen Bereich in einem Arbeitsblatt einer Excel-Arbeitsmappe. Für verwandte Vorgänge siehe die Dokumentation zu **Bereich abrufen** und **Bereich aktualisieren**.

**Voraussetzungen:** Um diesen Endpunkt nutzen zu können, benötigen Sie ein gültiges OAuth 2.0 / JWT-Token und stellen sicher, dass Ihre API-Version mit der Anfrage-URL übereinstimmt.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **Anfrageparameter**

| Parametername   | Typ    | Ort    | Beschreibung                                                                 |
| ---------------- | ------ | ------ | ---------------------------------------------------------------------------- |
| name             | string | path   | Der Name der Arbeitsmappe.                                                   |
| sheetName        | string | path   | Der Name des Arbeitsblatts.                                                  |
| rangeOperate     | string | body   | Die auszuführende Operation: `copydata`, `copystyle`, `copyto` oder `copyvalue`. |
| folder           | string | query  | Der Ordner, der die Arbeitsmappe enthält.                                    |
| storageName      | string | query  | Der Name des Speicherdienstes.                                               |

**Hinweise:** Das Feld `rangeOperate` bestimmt, was kopiert wird. Verwenden Sie `copydata`, um nur Zellwerte zu kopieren, `copystyle` für Formatierungen, `copyto` für sowohl Daten als auch Formatierung sowie `copyvalue`, um Werte ohne Formeln zu kopieren. Die API unterstützt Bereiche bis zu 1 Million Zellen; größere Bereiche können zu einem Timeout führen.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopyCopy) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Die erfolgreiche Antwort gibt den Status `200 OK` zurück. Im Fehlerfall kann die API Payloads wie die folgenden zurückgeben:

```json
{
  "Code": 400,
  "Message": "Bad Request – ungültige Parameter."
}
```

oder

```json
{
  "Code": 401,
  "Message": "Unauthorized – Authentifizierungstoken fehlt oder ist ungültig."
}
```

Diese Fehlerobjekte enthalten einen HTTP-Statuscode sowie eine beschreibende Nachricht, um Probleme zu diagnostizieren.

{{< /tab >}}

{{< /tabs >}}

Sie können eine Beispieldatei zum Testen des Kopiervorgangs [hier](https://example.com/sample.xlsx) herunterladen.

## Cloud SDK Family

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}
---