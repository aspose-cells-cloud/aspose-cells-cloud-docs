---
title: "Gruppierung von Zeilen in einem Excel-Arbeitsblatt aufheben"
second_title: "Dokument"
linktitle: "Gruppierung aufheben"
type: docs
url: /rows/ungroup/
aliases: [/ungroup-rows-in-excel-worksheet/]
keywords: "Zeilengruppierung aufheben, Excel, Aspose.Cells Cloud, REST API, SDK, Tabellenkalkulation"
description: "Erfahren Sie, wie Sie die Gruppierung von Zeilen in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API und SDKs für verschiedene Programmiersprachen aufheben."
weight: 70
---

Diese REST API hebt die Gruppierung von Zeilen in einem Excel-Arbeitsblatt auf.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **Anfrageparameter**

| Parametername   | Typ     | Ort    | Beschreibung                                                  |
| --------------- | ------- | ------ | ------------------------------------------------------------- |
| name            | string  | path   | Der Name der Arbeitsmappe.                                    |
| sheetName       | string  | path   | Der Name des Arbeitsblatts.                                   |
| firstIndex      | integer | query  | Der nullbasierte Index der ersten Zeile, deren Gruppierung aufgehoben werden soll. |
| lastIndex       | integer | query  | Der nullbasierte Index der letzten Zeile, deren Gruppierung aufgehoben werden soll. |
| isAll           | boolean | query  | Falls **true**, wird die Gruppierung für alle Zeilen im angegebenen Bereich aufgehoben. |
| folder          | string  | query  | Der Ordner, der die Arbeitsmappe enthält.                     |
| storageName     | string  | query  | Der Name des Speichers, in dem sich die Arbeitsmappe befindet. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
 -X POST \
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

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf unterster Ebene und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}