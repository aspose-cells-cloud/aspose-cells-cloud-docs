---
title: "Horizontale Seitenumbruch hinzufügen"
second_title: "Dokument"
linktitle: "Horizontale Seitenumbruch hinzufügen"
type: docs
url: /page-breaks/add-horizontal-page-break/
aliases: [/insert-horizontal-page-break-inside-worksheet/]
keywords: "horizontale Seitenumbruch, Aspose.Cells Cloud, Excel API, REST, SDK, Arbeitsblatt, cURL"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API einen horizontale Seitenumbruch in ein Excel-Arbeitsblatt einfügen. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Code-Snippets für mehrere Programmiersprachen."
weight: 30
ArticleTitle: "Horizontale Seitenumbruch hinzufügen – Aspose.Cells Cloud API"
---

Die **Add Horizontal Page Break** API fügt einen horizontalen Seitenumbruch in ein Excel-Arbeitsblatt ein.

**Voraussetzungen & Authentifizierung**  
Für alle Aufrufe der Aspose.Cells Cloud API ist ein gültiges JWT-Token erforderlich. Holen Sie sich das Token über den in der Authentifizierungsanleitung beschriebenen OAuth 2.0-Workflow und fügen Sie es in den Anforderungsheader als `Authorization: Bearer <jwt token>` ein. Die Ziel- Arbeitsmappe muss sich in einem Speicherort befinden, auf den die API zugreifen kann (Standard-Speicher oder ein benutzerdefiniertes `storageName`, das Sie angeben).

## PutHorizontalPageBreak API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Ort    | Beschreibung                                                                 |
|---------------|--------|--------|------------------------------------------------------------------------------|
| name          | string | path   | Name der Excel-Datei.                                                       |
| sheetName     | string | path   | Name des Arbeitsblatts, in dem der Seitenumbruch eingefügt wird.           |
| cellname      | string | query  | Zellreferenz (z. B. **A1**), die den Beginn des Seitenumbruchs markiert.   |
| row           | integer| query  | Nullbasierter Zeilenindex für den Seitenumbruch.                           |
| column        | integer| query  | Nullbasierter Spaltenindex für den Seitenumbruch.                          |
| startColumn   | integer| query  | Startspalte eines Bereichs beim Einfügen eines Seitenumbruchs.             |
| endColumn     | integer| query  | Endspalte eines Bereichs beim Einfügen eines Seitenumbruchs.               |
| folder        | string | query  | Ordnerpfad, der die Excel-Datei enthält.                                   |
| storageName   | string | query  | Name des Aspose Cloud-Speichers.                                            |

Die <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Schnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Im folgenden Beispiel wird gezeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Verwenden Sie HTTPS, um eine verschlüsselte Kommunikation sicherzustellen
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
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

Beispiel einer Fehlerantwort, wenn das JWT-Token fehlt oder ungültig ist:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Ungültiges oder fehlendes JWT-Token."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                 |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                         |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größenbeschränkung.     |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                   |

Weitere Details zu verwandten Vorgängen finden Sie auf den API-Seiten für **[Get Horizontal Page Breaks](../get-horizontal-page-breaks/)** und **[Delete Horizontal Page Break](../delete-horizontal-page-break/)**.

## Cloud SDK Family

Die Verwendung eines SDK ist der schnellste Weg zur Entwicklung. Ein SDK abstractisiert Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Bitte prüfen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}