---
title: "Uppdatera diagrammets andra värdeaxel"
ArticleTitle: "Uppdatera diagrammets andra värdeaxel – Aspose.Cells Cloud REST API"
type: docs
url: /charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, Second Value Axis, Excel, REST, Cloud SDK"
description: "Uppdaterar den andra värdeaxeln i ett diagram i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller exempel på förfrågningar, svarskoder och förutsättningar."
---

Denna REST API uppdaterar den andra värdeaxeln i ett diagram.

**Förutsättningar:**  
- En giltig JWT-åtkomsttoken (se [Autentiseringsguide](https://docs.aspose.cloud/cells/authentication/)).  
- Den mål-Excel-fil som ska användas måste finnas lagrad i Aspose Cloud-lagring (ange `folder` och valfritt `storageName`).  
- API-version v3.0 används; se till att bas-URL är `https://api.aspose.cloud/v3.0`.

## PostChartSecondValueAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Förfrågningsparametrar

| Parameternamn  | Typ     | Plats   | Beskrivning                                      |
| -------------- | ------- | ------- | ------------------------------------------------ |
| name           | string  | path    | Namn på Excel-filen.                             |
| sheetName      | string  | path    | Namn på det ark som innehåller diagrammet.       |
| chartIndex     | integer | path    | Nollbaserat index för diagrammet som ska ändras. |
| axis           | object  | body    | Inställningar för den andra värdeaxeln.          |
| folder         | string  | query   | Mappväg i lagringen där filen finns.             |
| storageName    | string  | query   | Namn på lagringstjänsten.                        |

**Exempel på förfrågningsbody (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Sekundär axel"
  }
}
```

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token.                            |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksbegränsningen.    |
| 500 | Internt serverfel           | Oväntat serverfel.                                         |

**Se även:**  
- [Hämta diagrammets andra värdeaxel](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [Uppdatera diagrammets värdeaxel](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Cloud SDK Family

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljerna på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C#-exempel för att uppdatera den andra värdeaxeln
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java-exempel för att uppdatera den andra värdeaxeln
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// PHP-exempel för att uppdatera den andra värdeaxeln
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby-exempel för att uppdatera den andra värdeaxeln
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python-exempel för att uppdatera den andra värdeaxeln
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
// Android-exempel (Java) – samma som Java-kodblocket ovan
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift-exempel för att uppdatera den andra värdeaxeln
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl-exempel för att uppdatera den andra värdeaxeln
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go-exempel för att uppdatera den andra värdeaxeln
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}
---