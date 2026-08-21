---
title: "Spalten in einem Excel-Arbeitsblatt einblenden"
ArticleTitle: "Spalten in einem Excel-Arbeitsblatt einblenden – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /de/columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, Cloud API, Spalten einblenden, Excel, REST, SDK"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST API verwenden, um Spalten in einem Excel-Arbeitsblatt einzublenden. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Codebeispiele für mehrere Programmiersprachen."
weight: 50
---

Diese REST API blendet Spalten in einem Arbeitsblatt wieder ein.

**Voraussetzungen** – Alle Aspose.Cells Cloud-Endpunkte erfordern HTTPS und einen gültigen OAuth 2.0-Zugriffstoken. Stellen Sie sicher, dass Sie einen Zugriffstoken erhalten haben und diesen im `Authorization`-Header Ihrer Anfragen angeben.

## PostUnhideWorksheetColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ     | Ort    | Beschreibung                                     |
| --------------- | ------- | ------ | ------------------------------------------------ |
| name            | string  | path   | Der Name der Arbeitsmappe.                       |
| sheetName       | string  | path   | Der Name des Arbeitsblatts.                      |
| startColumn     | integer | query  | Der Index der ersten zu verarbeitenden Spalte.   |
| totalColumns    | integer | query  | Die Anzahl der zu verarbeitenden Spalten.        |
| width           | number  | query  | Gewünschte Spaltenbreite (Standard = 50,0).      |
| folder          | string  | query  | Der Ordner, der das Dokument enthält.            |
| storageName     | string  | query  | Der Name des Speicherdienstes.                   |

Die <a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Anfragen an die Cloud API mit cURL gestellt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**Typische HTTP-Statuscodes**

| Code | Beschreibung                                 |
|------|----------------------------------------------|
| 200  | OK – Spalten wurden erfolgreich eingeblendet.|
| 400  | Bad Request – Ungültige Parameter.          |
| 401  | Unauthorized – Fehlender oder ungültiger Token. |
| 404  | Not Found – Arbeitsmappe oder Arbeitsblatt nicht gefunden. |
| 500  | Internal Server Error – Unerwarteter Fehler. |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}