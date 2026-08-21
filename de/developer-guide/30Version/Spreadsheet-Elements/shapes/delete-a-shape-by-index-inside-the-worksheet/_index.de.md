---
title: "Löschen einer Formularformular nach Index auf einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /de/shapes/delete/
aliases: [  /delete-a-shape-by-index-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, Formular löschen, Formularindex, Excel-Arbeitsblatt, REST-API, SDK"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um eine Formularformular nach ihrem Index auf einem Excel-Arbeitsblatt zu löschen. Die API ist über mehrere SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) verfügbar und unterstützt verschiedene Speicheroptionen."
weight: 50
---

Diese REST-API löscht eine Formularformular auf einem Excel-Arbeitsblatt.

## REST-API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### **Anforderungsparameter**

| Parametername   | Typ     | Ort    | Beschreibung                                      |
| --------------- | ------- | ------ | ------------------------------------------------- |
| name            | string  | path   | Name der Arbeitsmappen-Datei.                     |
| sheetName       | string  | path   | Name des Arbeitsblatts.                           |
| shapeindex      | integer | path   | Index der Formularformular innerhalb der Shapes. |
| folder          | string  | query  | Ordner, in dem die Arbeitsmappe gespeichert ist.  |
| storageName     | string  | query  | Name des Speichers.                               |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShape) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt über einen Webbrowser durchzuführen.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/1" \
-X DELETE \
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

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können.Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}