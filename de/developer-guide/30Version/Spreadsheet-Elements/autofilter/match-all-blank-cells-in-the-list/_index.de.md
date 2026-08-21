---
title: "Alle leeren Zellen in einem Excel-Arbeitsblatt matchen"
ArticleTitle: "Alle leeren Zellen in einem Excel-Arbeitsblatt matchen – Aspose.Cells Cloud API-Anleitung"
second_title: "Dokument"
linktype: "docs"
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, leere Zellen, AutoFilter, REST API, Excel"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST API verwenden, um alle leeren Zellen in einem Excel-Arbeitsblatt zu filtern und zu matchen. Enthält Endpunkt, Parameter, Authentifizierungsschritte, cURL-Beispiel und SDK-Snippets für C#, Java, Python und mehr."
weight: 100
---

Diese REST API matcht alle **leeren Zellen** in der Filterliste eines Excel-Arbeitsblatts.

**Voraussetzungen:** Vor dem Aufrufen dieses Endpunkts stellen Sie sicher, dass Sie über ein gültiges JWT-Access-Token verfügen, die Arbeitsmappe in den Aspose-Cloud-Speicher hochgeladen wurde und der Speicherordner (falls zutreffend) bekannt ist. Geben Sie die Parameter `folder` und `storageName` an, wenn sich die Datei nicht im standardmäßigen Stammverzeichnis befindet.

## PostWorksheetMatchBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername     | Typ     | Ort    | Beschreibung                                                   |
|-------------------|---------|--------|----------------------------------------------------------------|
| name              | string  | path   | Der Name der Arbeitsmappen-Datei.                             |
| sheetName         | string  | path   | Der Name des Arbeitsblatts, das den Filter enthält.           |
| fieldIndex        | integer | query  | Der nullbasierte Index der Spalte, auf die der Filter angewendet wird. |
| folder            | string  | query  | Der Ordnerpfad im Speicher, in dem sich die Arbeitsmappe befindet. |
| storageName       | string  | query  | Der Name des Aspose-Cloud-Speichers.                           |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; die Antwort enthält Details zum Vorgang.     |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Verwendung der PostWorksheetMatchBlanks API mit SDKs

### PostWorksheetMatchBlanks API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
  -X POST \
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

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK abstrahiert die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projekt Aufgaben zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}