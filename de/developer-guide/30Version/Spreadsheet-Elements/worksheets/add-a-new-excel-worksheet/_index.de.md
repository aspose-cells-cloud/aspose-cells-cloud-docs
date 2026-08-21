---
title: "Fügen Sie ein Excel-Arbeitsblatt hinzu"
ArticleTitle: "Fügen Sie ein Excel-Arbeitsblatt hinzu – Aspose.Cells Cloud API-Anleitung"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /worksheets/add/
aliases: [/add-a-new-excel-worksheet/]
keywords: "Excel-Arbeitsblatt hinzufügen, Aspose.Cells Cloud, REST-API, PUT worksheet, Excel-Arbeitsmappe, API-Anfrage"
description: "Schritt-für-Schritt-Anleitung zum Hinzufügen eines neuen Arbeitsblatts zu einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API, einschließlich Anforderungsdetails, einem cURL-Beispiel und SDK-Code-Snippets für mehrere Sprachen."
weight: 20
---

Diese REST API fügt ein neues Arbeitsblatt zu einer vorhandenen Arbeitsmappe hinzu.

**Voraussetzungen**: Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges Aspose Cloud Authentifizierungstoken, die Ziel-Arbeitsmappe muss in den Aspose Cloud-Speicher hochgeladen sein, und Sie müssen den Namen des Speichers kennen (sofern Sie einen benutzerdefinierten Speicher verwenden).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Anforderungsparameter**

| Parametername   | Typ    | Speicherort | Beschreibung                                                |
|-----------------|--------|-------------|-------------------------------------------------------------|
| name            | string | path        | Name der Arbeitsmappendatei.                                |
| sheetName       | string | path        | Name des neu zu erstellenden Arbeitsblatts.                 |
| position        | integer | query      | Nullbasierte Position, an der das Blatt eingefügt wird.     |
| sheettype       | string | query       | Typ des neuen Blatts (z. B. **Chart**, **Dialog**).        |
| folder          | string | query       | Ordner, der die Arbeitsmappe enthält.                       |
| storageName     | string | query       | Name des Aspose Cloud-Speichers.                            |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**Mögliche Antwort-Statuscodes**

| Statuscode | Beschreibung                                               |
|------------|------------------------------------------------------------|
| 200        | Arbeitsblatt erfolgreich hinzugefügt.                     |
| 400        | Ungültige Anforderung – ungültige Parameter.              |
| 401        | Nicht autorisiert – Authentifizierungstoken fehlt/ungültig. |
| 404        | Nicht gefunden – Arbeitsmappe oder Ordner existiert nicht. |
| 500        | Interner Serverfehler – unerwarteter Zustand.             |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstractiert die niederleveligen Details und ermöglicht es Ihnen, sich auf Ihr Projekt zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---