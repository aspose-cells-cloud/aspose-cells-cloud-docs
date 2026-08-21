---
title: "Ottenere il Titolo di un Grafico da un Foglio di Lavoro"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Titolo del grafico"
  - "Excel"
  - "REST API"
  - "Ottenere il titolo del grafico"
  - "cURL"
  - "SDK"
  - "Automazione grafici Excel"
  - "GET chart title"
description: "Scopri come recuperare il titolo di un grafico da un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, autenticazione, codice di esempio in cURL e SDK."
ArticleTitle: "Ottenere il Titolo di un Grafico da un Foglio di Lavoro"
---

Questa API REST consente di recuperare il titolo di un grafico memorizzato in un foglio di lavoro di un file Excel.

**Prerequisiti**: Per chiamare questo endpoint è necessario disporre di un token di accesso valido per Aspose.Cells Cloud OAuth2/JWT con l'ambito `Cells.Read`. Il file di lavoro deve essere già caricato nella posizione di archiviazione specificata.

## API GetWorksheetChartTitle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                   |
| -------------- | ------- | -------- | --------------------------------------------- |
| name           | string  | path     | Nome del file del file di lavoro.             |
| sheetName      | string  | path     | Nome del foglio di lavoro contenente il grafico. |
| chartIndex     | integer | path     | Indice in base zero del grafico.              |
| folder         | string  | query    | Percorso della cartella in cui è memorizzato il file di lavoro. |
| storageName    | string  | query    | Nome del servizio di archiviazione.           |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

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
    "Text": "Vendite Q1",
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

**Campi della risposta**

| Campo               | Descrizione                                   |
| ------------------- | --------------------------------------------- |
| `Title.Text`        | Il testo effettivo visualizzato come titolo del grafico. |
| `Title.Font.Name`   | Famiglia di caratteri utilizzata per il titolo (es. _Arial_). |
| `Title.Font.Size`   | Dimensione del carattere in punti.            |
| `Title.Font.IsBold` | Indica se il testo del titolo è in grassetto. |

**Codici di stato della risposta**

| Codice | Descrizione |
|------|-------------|
| 200 OK | Il titolo del grafico è stato recuperato correttamente. |
| 401 Unauthorized | Autenticazione non riuscita o token mancante/invalido. |
| 404 Not Found | Il file di lavoro, il foglio di lavoro o il grafico specificati non esistono. |
| 500 Internal Server Error | Si è verificato un errore imprevisto nel server. |

**Note**: L'indice del grafico è in base zero; assicurati che il grafico esista. Se il file di lavoro non è stato caricato, caricalo prima utilizzando l'API appropriata.

**Come estrarre il titolo in uno script (utilizzando `jq`)**

```bash
# Supponendo che la risposta JSON sia salvata in response.json
title=$(jq -r '.Title.Text' response.json)
echo "Titolo del grafico: $title"
```

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Esempio C# utilizzando l'SDK di Aspose.Cells Cloud
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
// Esempio Java utilizzando l'SDK di Aspose.Cells Cloud
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
// Esempio PHP utilizzando l'SDK di Aspose.Cells Cloud
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
# Esempio Ruby utilizzando l'SDK di Aspose.Cells Cloud
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
# Esempio Python utilizzando l'SDK di Aspose.Cells Cloud
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
// Esempio Node.js utilizzando l'SDK di Aspose.Cells Cloud
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
// Esempio Android (Java) utilizzando l'SDK di Aspose.Cells Cloud
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
// Esempio Swift utilizzando l'SDK di Aspose.Cells Cloud
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Titolo del grafico: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Esempio Perl utilizzando l'SDK di Aspose.Cells Cloud
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

Puoi anche consultare la documentazione specifica dell'SDK per scenari più avanzati, come l'aggiornamento o l'eliminazione del titolo di un grafico.

**Vedi anche**: [Aggiornare il Titolo del Grafico](/charts/title/put/), [Eliminare il Titolo del Grafico](/charts/title/delete/).
---