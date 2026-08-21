---
title: "Aktualisieren der zweiten Wertachse eines Diagramms"
ArticleTitle: "Aktualisieren der zweiten Wertachse eines Diagramms – Aspose.Cells Cloud REST API"
type: docs
url: /de/charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, Zweite Wertachse, Excel, REST, Cloud SDK"
description: "Aktualisiert die zweite Wertachse eines Diagramms in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API. Enthält Beispielanforderungen, Antwortcodes und Voraussetzungen."
---

Diese REST API aktualisiert die zweite Wertachse eines Diagramms.

**Voraussetzungen:**  
- Ein gültiges JWT-Access-Token (siehe [Authentifizierungsanleitung](https://docs.aspose.cloud/cells/authentication/)).  
- Die Ziel-Excel-Datei muss im Aspose-Cloud-Speicher gespeichert sein (geben Sie `folder` und optional `storageName` an).  
- API-Version v3.0 wird verwendet; stellen Sie sicher, dass die Basis-URL `https://api.aspose.cloud/v3.0` lautet.

## PostChartSecondValueAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ     | Speicherort | Beschreibung                                        |
| --------------- | ------- | ----------- | --------------------------------------------------- |
| name            | string  | path        | Name der Excel-Datei.                              |
| sheetName       | string  | path        | Name des Arbeitsblatts, das das Diagramm enthält.  |
| chartIndex      | integer | path        | Nullbasierten Index des zu ändernden Diagramms.    |
| axis            | object  | body        | Einstellungen für die zweite Wertachse.            |
| folder          | string  | query       | Ordnerpfad im Speicher, in dem sich die Datei befindet. |
| storageName     | string  | query       | Name des Speicherdienstes.                         |

**Beispielanforderungstext (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Sekundäre Achse"
  }
}
```

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                              |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                     |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.   |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                               |

**Siehe auch:**  
- [Abrufen der zweiten Wertachse eines Diagramms](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [Aktualisieren der Diagrammwertachse](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Cloud SDK Family

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um die Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C#-Beispiel zum Aktualisieren der zweiten Wertachse
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java-Beispiel zum Aktualisieren der zweiten Wertachse
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// PHP-Beispiel zum Aktualisieren der zweiten Wertachse
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby-Beispiel zum Aktualisieren der zweiten Wertachse
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python-Beispiel zum Aktualisieren der zweiten Wertachse
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android-(Java)-Beispiel – identisch mit dem obigen Java-Snippet
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift-Beispiel zum Aktualisieren der zweiten Wertachse
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl-Beispiel zum Aktualisieren der zweiten Wertachse
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go-Beispiel zum Aktualisieren der zweiten Wertachse
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}