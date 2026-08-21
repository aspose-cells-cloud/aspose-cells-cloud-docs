---
title: "Alle Dokumenteigenschaften entfernen"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /de/document-properties/clear/
aliases: [  /de/remove-all-document-properties/ ]
keywords: "Aspose.Cells, Dokumenteigenschaften löschen, Excel-Eigenschaften löschen, REST API, Cloud-SDK, Tabellenkalkulation, API-Referenz"
description: "Schritt-für-Schritt-Anleitung zum Entfernen aller benutzerdefinierten und Zurücksetzen aller integrierten Eigenschaften einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API."
weight: 58
---

Diese REST API löscht alle benutzerdefinierten Dokumenteigenschaften und setzt die integrierten Eigenschaften zurück.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung              |
| --------------- | ------ | ------ | ------------------------- |
| name            | string | path   | Der Dokumentname.         |
| folder          | string | query  | Der Dokumentordner.       |
| storageName     | string | query  | Der Speichername.         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperties) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperties.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperties.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperties.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperties.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperties.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperties.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperties.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperties.go" >}}
{{< /tab >}}

{{< /tabs >}}