---
title: "Hämta diagramrubrik från ett kalkylblad"
type: docs
url: /sv/charts/title/get/
aliases: [  /sv/get-chart-title-from-a-worksheet/ ]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Diagramrubrik"
  - "Excel"
  - "REST API"
  - "Hämta diagramrubrik"
  - "cURL"
  - "SDK"
  - "Automatisering av Excel-diagram"
  - "GET diagramrubrik"
description: "Lär dig hur du hämtar en diagramrubrik från ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Innehåller endpoint, parametrar, autentisering, exempel på cURL- och SDK-kod."
ArticleTitle: "Hämta diagramrubrik från ett kalkylblad"
---

Denna REST API hämtar rubriken för ett diagram som är lagrat i ett kalkylblad i en Excel-arbetsbok.

**Förutsättningar**: För att anropa denna endpoint måste du ha en giltig Aspose.Cells Cloud OAuth2/JWT-åtkomsttoken med scope `Cells.Read`. Arbetsboken måste redan vara uppladdad till den angivna lagringsplatsen.

## GetWorksheetChartTitle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameternamn | Typ    | Plats  | Beskrivning                                   |
| ------------- | ------ | ------ | --------------------------------------------- |
| name          | string | path   | Namn på arbetsboksfilen.                      |
| sheetName     | string | path   | Namn på kalkylbladet som innehåller diagrammet. |
| chartIndex    | integer | path  | Nollbaserat index för diagrammet.             |
| folder        | string | query  | Mappväg där arbetsboken är lagrad.            |
| storageName   | string | query  | Namn på lagringstjänsten.                     |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

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
    "Text": "Försäljning Q1",
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

**Svarsfält**

| Fält                | Beskrivning                                   |
| ------------------- | --------------------------------------------- |
| `Title.Text`        | Den faktiska texten som visas som diagramrubrik. |
| `Title.Font.Name`   | Teckensnittsfamilj som används för rubriken (t.ex. _Arial_). |
| `Title.Font.Size`   | Teckenstorlek i punkter.                      |
| `Title.Font.IsBold` | Anger om diagramrubrikens text är fetstild.   |

**Svarsstatuskoder**

| Kod | Beskrivning |
|-----|-------------|
| 200 OK | Diagramrubriken hämtades framgångsrikt. |
| 401 Obehörig | Autentisering misslyckades eller token saknas/är ogiltig. |
| 404 Ej hittad | Den angivna arbetsboken, kalkylbladet eller diagrammet finns inte. |
| 500 Internt serverfel | Ett oväntat serverfel inträffade. |

**Anteckningar**: Diagramindexet är nollbaserat; se till att diagrammet finns. Om arbetsboken inte har laddats upp, ladda upp den först med lämpligt API.

**Hur man extraherar rubriken i ett skript (med `jq`)**

```bash
# Anta att JSON-svaret är sparat i response.json
title=$(jq -r '.Title.Text' response.json)
echo "Diagramrubrik: $title"
```

## Cloud SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektoppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C#-exempel med Aspose.Cells Cloud SDK
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
// Java-exempel med Aspose.Cells Cloud SDK
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
// PHP-exempel med Aspose.Cells Cloud SDK
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
# Ruby-exempel med Aspose.Cells Cloud SDK
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
# Python-exempel med Aspose.Cells Cloud SDK
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
// Node.js-exempel med Aspose.Cells Cloud SDK
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
// Android (Java)-exempel med Aspose.Cells Cloud SDK
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
// Swift-exempel med Aspose.Cells Cloud SDK
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Diagramrubrik: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl-exempel med Aspose.Cells Cloud SDK
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

Du kan också läsa den individuella SDK-dokumentationen för avancerade scenarier, till exempel uppdatering eller borttagning av en diagramrubrik.

**Se även**: [Uppdatera diagramrubrik](/charts/title/put/), [Ta bort diagramrubrik](/charts/title/delete/).