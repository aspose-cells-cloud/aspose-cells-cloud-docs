---
title: "Löschen einer bestimmten Dokumenteigenschaft"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /de/document-properties/delete/
aliases: [  /de/remove-a-particular-document-property/ ]
keywords: "Aspose.Cells, Dokumenteigenschaft löschen, Excel-Metadaten-API, REST, Cloud-SDK, cURL-Beispiel"
description: "Löschen einer bestimmten Dokumenteigenschaft aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API v3.0. Beinhaltet cURL- und SDK-Beispiele für C#, Java, Python und weitere."
weight: 50
---

Diese REST API löscht eine Dokumenteigenschaft aus einer Arbeitsmappe.

## REST-API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Anforderungsparameter

| Parametername   | Typ    | Ort     | Erforderlich | Beschreibung                                           |
| --------------- | ------ | ------- | ------------ | ------------------------------------------------------ |
| name            | string | path    | Ja           | Der Name der Excel-Arbeitsmappe.                       |
| propertyName    | string | path    | Ja           | Der Name der zu löschenden Dokumenteigenschaft.       |
| folder          | string | query   | Nein         | Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist. |
| storageName     | string | query   | Nein         | Der Name des Speicherdienstes.                         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
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

### Fehlerantworten

| HTTP-Status | Beschreibung                                                       | Beispiel-JSON                                                    |
| ----------- | ------------------------------------------------------------------ | ---------------------------------------------------------------- |
| 400         | Ungültige Anforderung – fehlende erforderliche Parameter oder ungültige Werte. | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401         | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.         | `{"Code":401,"Message":"Invalid access token."}`               |
| 404         | Nicht gefunden – die Arbeitsmappe oder die angegebene Eigenschaft existiert nicht. | `{"Code":404,"Message":"Document property not found."}`       |
| 500         | Interner Serverfehler – ein unerwarteter Zustand ist auf dem Server aufgetreten. | `{"Code":500,"Message":"An unexpected error has occurred."}`  |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}