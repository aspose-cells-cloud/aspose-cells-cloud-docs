---
title: "Ein Excel-Arbeitsbuch in mehrere Dateien aufteilen"
ArticleTitle: "Wie man ein Excel-Arbeitsbuch mit der Aspose.Cells Cloud API in mehrere Dateien aufteilt"
second_title: "Dokument"
linktitle: "Eine Excel-Datei aufteilen"
type: docs
url: /split-multi-excel-files/
aliases: [/split/multi-files/]
keywords: "Excel, Aspose.Cells Cloud, REST API, Arbeitsbuch aufteilen, mehrere Dateien, JPEG, PNG, PDF, CSV, JSON"
description: "Die Aspose.Cells Cloud REST API ermöglicht das Aufteilen eines Excel-Arbeitsbuchs in mehrere Dateien in verschiedenen Formaten. Diese Dokumentation enthält Anforderungsparameter, ein cURL-Beispiel und SDK-Codebeispiele für die Sprachen C#, Java, PHP, Ruby, Node.js, Python, Perl und Go."
weight: 130
---

Diese REST API teilt ein Excel-**Arbeitsbuch** in mehrere Dateien in verschiedenen Formaten auf.

> **Voraussetzungen** – Um diese API nutzen zu können, müssen Sie ein gültiges JWT-Token besitzen, sicherstellen, dass Sie eine unterstützte SDK-Version verwenden, und überprüfen, ob sich Ihr Arbeitsbuch in einem unterstützten Speicherort befindet. Die API erzwingt außerdem Dateigrößenbeschränkungen, die in den Plattformrichtlinien dokumentiert sind.

## PostWorkbookSplit API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername        | Typ     | Ort       | Beschreibung                                                                                     | Erforderlich |
| -------------------- | ------- | --------- | ------------------------------------------------------------------------------------------------ | ------------ |
| files[]              | Datei   | formData  | Eine oder mehrere Excel-Arbeitsbücher, die **aufgeteilt** werden sollen. Verwenden Sie `file1`, `file2`, … in der Anfrage. | Ja           |
| format               | Zeichenkette | Query   | Gewünschtes Ausgabeformat für die aufgeteilten Dateien.                                         | Nein         |
| from                 | Ganzzahl | Query    | Startindex des Arbeitsblatts.                                                                    | Nein         |
| to                   | Ganzzahl | Query    | Endindex des Arbeitsblatts.                                                                      | Nein         |
| horizontalResolution | Ganzzahl | Query    | Horizontale Bildauflösung.                                                                       | Nein         |
| verticalResolution   | Ganzzahl | Query    | Vertikale Bildauflösung.                                                                         | Nein         |
| outFolder            | Zeichenkette | Query  | Ausgabeordner für die aufgeteilten Dateien.                                                      | Nein         |
| splitNameRule        | Zeichenkette | Query  | Namensregel, die auf die aufgeteilten Dateien angewendet wird.                                  | Nein         |
| folder               | Zeichenkette | Query  | Ordner, der das ursprüngliche Arbeitsbuch enthält.                                               | Nein         |
| storageName          | Zeichenkette | Query  | Name des zu verwendenden Speichers.                                                              | Nein         |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[Dateiname 1]",
        "Filesize" : [Dateigröße],
        "FileContent" : "[Base64-Zeichenkette]"
      },
      {
        "Filename" : "[Dateiname 2]",
        "Filesize" : [Dateigröße],
        "FileContent" : "[Base64-Zeichenkette]"
      },
      {
        "Filename" : "[Dateiname 3]",
        "Filesize" : [Dateigröße],
        "FileContent" : "[Base64-Zeichenkette]"
      }
    ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größeinschränkung.                 |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Verwendung der PostWorkbookSplit API mit SDKs

### PostWorkbookSplit API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---