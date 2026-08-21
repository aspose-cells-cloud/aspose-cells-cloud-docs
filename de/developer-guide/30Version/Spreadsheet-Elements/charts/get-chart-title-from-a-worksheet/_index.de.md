---
title: "Diagrammtitel aus einem Arbeitsblatt abrufen"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Diagrammtitel"
  - "Excel"
  - "REST API"
  - "Diagrammtitel abrufen"
  - "cURL"
  - "SDK"
  - "Excel-Diagrammautomatisierung"
  - "GET chart title"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API den Titel eines Diagramms aus einem Excel-Arbeitsblatt abrufen. Enthält Endpunkt, Parameter, Authentifizierung sowie Beispiel-cURL- und SDK-Code."
ArticleTitle: "Diagrammtitel aus einem Arbeitsblatt abrufen"
---

Diese REST API ruft den Titel eines Diagramms ab, das in einem Arbeitsblatt einer Excel-Arbeitsmappe gespeichert ist.

**Voraussetzungen**: Um diesen Endpunkt aufzurufen, benötigen Sie ein gültiges Aspose.Cells Cloud OAuth2/JWT-Access-Token mit dem Scope `Cells.Read`. Die Arbeitsmappe muss bereits in den angegebenen Speicherort hochgeladen worden sein.

## GetWorksheetChartTitle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ     | Speicherort | Beschreibung                                     |
| --------------- | ------- | ----------- | ------------------------------------------------ |
| name            | string  | path        | Name der Arbeitsmappen-Datei.                    |
| sheetName       | string  | path        | Name des Arbeitsblatts, das das Diagramm enthält.|
| chartIndex      | integer | path        | Nullbasierter Index des Diagramms.               |
| folder          | string  | query       | Pfad des Ordners, in dem die Arbeitsmappe gespeichert ist. |
| storageName     | string  | query       | Name des Speicherdienstes.                       |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webservices einfach anzusprechen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Umsatz Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Antwortfelder**

| Feld                | Beschreibung                                       |
| ------------------- | -------------------------------------------------- |
| `Title.Text`        | Der tatsächlich als Diagrammtitel angezeigte Text.|
| `Title.Font.Name`   | Für den Titel verwendete Schriftfamilie (z. B. _Arial_). |
| `Title.Font.Size`   | Schriftgröße in Punkten.                           |
| `Title.Font.IsBold` | Gibt an, ob der Titeltext fett formatiert ist.     |

**Antwortstatuscodes**

| Code | Beschreibung |
|------|--------------|
| 200 OK | Der Diagrammtitel wurde erfolgreich abgerufen. |
| 401 Unauthorized | Authentifizierung fehlgeschlagen oder Token fehlt/ungültig. |
| 404 Not Found | Die angegebene Arbeitsmappe, das Arbeitsblatt oder das Diagramm existiert nicht. |
| 500 Internal Server Error | Ein unerwarteter Serverfehler ist aufgetreten. |

**Hinweise**: Der Diagrammindex ist nullbasiert; stellen Sie sicher, dass das Diagramm vorhanden ist. Wenn die Arbeitsmappe noch nicht hochgeladen wurde, laden Sie sie zunächst mithilfe der entsprechenden API hoch.

**So extrahieren Sie den Titel in einem Skript (mit `jq`)**

```bash
# Vorausgesetzt, die JSON-Antwort wurde in response.json gespeichert
title=$(jq -r '.Title.Text' response.json)
echo "Diagrammtitel: $title"
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs erfolgen:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C#-Beispiel mit Aspose.Cells Cloud SDK
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java-Beispiel mit Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP-Beispiel mit Aspose.Cells Cloud SDK
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby-Beispiel mit Aspose.Cells Cloud SDK
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python-Beispiel mit Aspose.Cells Cloud SDK
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js-Beispiel mit Aspose.Cells Cloud SDK
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android-(Java)-Beispiel mit Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift-Beispiel mit Aspose.Cells Cloud SDK
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Diagrammtitel: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl-Beispiel mit Aspose.Cells Cloud SDK
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

Weitere fortgeschrittene Szenarien, wie beispielsweise das Aktualisieren oder Löschen eines Diagrammtitels, finden Sie in der jeweiligen SDK-Dokumentation.

**Siehe auch**: [Diagrammtitel aktualisieren](/charts/title/put/), [Diagrammtitel löschen](/charts/title/delete/).
---