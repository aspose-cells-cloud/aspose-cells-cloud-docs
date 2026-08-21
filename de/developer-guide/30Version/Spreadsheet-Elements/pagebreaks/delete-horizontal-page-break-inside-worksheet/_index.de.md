---
title: "Horizontale Seitenumbrüche löschen"
ArticleTitle: "Aspose.Cells Cloud – Horizontale Seitenumbrüche löschen (REST API)"
second_title: "Dokument"
linktype: "docs"
url: /de/page-breaks/delete-horizontal-page-break/
aliases: [  /delete-horizontal-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, Horizontale Seitenumbrüche löschen, Excel-Arbeitsblatt, REST API, SDK"
description: "Löschen Sie einen horizontalen Seitenumbruch aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. SDKs verfügbar für C#, Java, PHP, Ruby, Node.js, Python, Perl, Go."
weight: 50
---

Diese REST API löscht einen **horizontalen** Seitenumbruch.

**Voraussetzungen**: Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges Aspose Cloud JWT-Access-Token. Erhalten Sie es gemäß der [Authentifizierungsanleitung](https://docs.aspose.cloud/cells/authentication/).

## DeleteHorizontalPageBreak API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*Alle API-Aufrufe müssen über **HTTPS** erfolgen.*

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ     | Ort    | Beschreibung                                                         |
|-----------------|---------|--------|----------------------------------------------------------------------|
| `name`          | string  | path   | Der Name der Excel-Datei (Arbeitsmappe).                            |
| `sheetName`     | string  | path   | Der Name des Arbeitsblatts, das den Seitenumbruch enthält.          |
| `index`         | integer | path   | Nullbasierter Index des zu löschenden horizontalen Seitenumbruchs.  |
| `folder`        | string  | query  | Optionaler Ordnerpfad im Speicher, in dem sich die Datei befindet. |
| `storageName`   | string  | query  | Optionaler Name des Speicherdienstes.                               |

### Fehlerantworten

| HTTP-Code | Beschreibung                                                                 |
|-----------|------------------------------------------------------------------------------|
| 401       | Nicht autorisiert – fehlender oder ungültiger Token.                        |
| 404       | Nicht gefunden – die angegebene Datei, das Arbeitsblatt oder der Index des Seitenumbruchs existiert nicht. |
| 400       | Ungültige Anforderung – fehlerhafte Syntax oder ungültige Parameter.        |
| 500       | Interner Serverfehler – unerwarteter Zustand aufgetreten.                   |

**Siehe auch:**  
- [Horizontalen Seitenumbruch hinzufügen](/page-breaks/add-horizontal-page-break/)  
- [Horizontale Seitenumbrüche abrufen](/page-breaks/get-horizontal-page-breaks/)  
- [Vertikalen Seitenumbruch löschen](/page-breaks/delete-vertical-page-break/)

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webdienste einfach anzusprechen. Das folgende Beispiel zeigt, wie der Aufruf mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
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

**Antwortschema**

| Feld    | Typ     | Beschreibung                                      |
|---------|---------|---------------------------------------------------|
| Code    | integer | HTTP-Statuscode (z. B. 200).                      |
| Status  | string  | Textuelle Statusmeldung (z. B. "OK").             |
| Message | string  | Optional zusätzliche Informationen bei Fehlern.   |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d).*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f).*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152).*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca).*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0).*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1).*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca).*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*Falls das Beispiel nicht geladen wird, sehen Sie es auf dem [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

{{< /tab >}}

{{< /tabs >}}