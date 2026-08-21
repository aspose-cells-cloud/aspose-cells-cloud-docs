---
title: "Hinzufügen eines Filters in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Filter hinzufügen"
type: docs
url: /de/autofilter/add-filter/
aliases: [  /de/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, Cloud, Excel, AutoFilter, Filter hinzufügen, REST API, SDK"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API einen Auto-Filter für eine Spalte in einem Excel-Arbeitsblatt hinzufügen. Enthält cURL-Beispiele, SDK-Beispiele und eine Parameteranleitung."
weight: 60
ArticleTitle: "Hinzufügen eines Filters in einem Excel-Arbeitsblatt mit Aspose.Cells Cloud"
---

**Voraussetzungen:** Bevor Sie diese API aufrufen, müssen Sie ein gültiges JWT-Token erhalten, sicherstellen, dass die Zielarbeitsmappe im angegebenen Speicher hochgeladen wurde, und über die erforderlichen Zugriffsrechte für die Datei verfügen. Für die Befehlszeilenbeispiele wird eine aktuelle Version von cURL (7.68 oder höher) empfohlen.

Diese REST API fügt einen Filter für eine bestimmte Spalte in einem Excel-Arbeitsblatt hinzu.

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ     | Lage     | Beschreibung |
|-----------------|---------|----------|-------------|
| name            | string  | Path     | Der Name der Arbeitsmappe. |
| sheetName       | string  | Path     | Der Name des Arbeitsblatts. |
| range           | string  | Query    | Der Zellbereich, der den Filter enthält (z. B. `A1:B1`). |
| fieldIndex      | integer | Query    | Der nullbasierte Index der Spalte, für die der Filter angewendet wird. |
| criteria        | string  | Query    | Die Filterkriterien (z. B. ein Wert oder ein Ausdruck). |
| matchBlanks     | boolean | Query    | Auf `true` setzen, um leere Zellen in den Filter einzubeziehen; andernfalls `false`. |
| refresh         | boolean | Query    | Auf `true` setzen, um den Filter nach dem Anwenden zu aktualisieren; andernfalls `false`. |
| folder          | string  | Query    | Der Ordner, in dem die ursprüngliche Arbeitsmappe gespeichert ist. |
| storageName     | string  | Query    | Der Name des Speicherdiensts. |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## Verwendung der PutWorksheetFilter API mit SDKs

### PutWorksheetFilter API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
-X PUT \
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

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}