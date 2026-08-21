---
title: "Alle Formen in einem Excel-Arbeitsblatt löschen"
ArticleTitle: "Alle Formen in einem Excel-Arbeitsblatt löschen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /de/shapes/clear/
aliases: [  /delete-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, Alle Formen löschen, Excel-Arbeitsblatt, REST API, SDK, cURL, .NET, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift"
description: "Löschen Sie alle Formen aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Der Vorgang ist über cURL und eine breite Palette an SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift) verfügbar."
weight: 40
---

Diese REST API löscht alle Formen in einem Excel-Arbeitsblatt.

**Voraussetzungen:** Ein gültiges JWT-Access-Token ist erforderlich. Es kann über den Aspose Cloud OAuth2-Flow abgerufen und im `Authorization`-Header wie im folgenden Beispiel gezeigt verwendet werden.

## DeleteWorksheetShapes API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ    | Ort    | Beschreibung                                  |
| --------------- | ------ | ------ | --------------------------------------------- |
| name            | string | path   | Der Name der Excel-Datei.                     |
| sheetName       | string | path   | Der Name des Arbeitsblatts.                   |
| folder          | string | query  | Der Ordner, der das Dokument enthält.         |
| storageName     | string | query  | Der Speichername, in dem sich das Dokument befindet. |

Die <a href="https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShapes" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
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

Die Verwendung eines SDK ist die beste Möglichkeit, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}