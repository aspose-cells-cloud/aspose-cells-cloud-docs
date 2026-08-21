---
title: "Aggiorna Asse Valore Secondario del Grafico"
ArticleTitle: "Aggiorna Asse Valore Secondario del Grafico – Aspose.Cells Cloud REST API"
type: docs
url: /it/charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, API per i grafici, Asse valore secondario, Excel, REST, SDK cloud"
description: "Aggiorna l'asse valore secondario di un grafico in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi di richiesta, codici di risposta e prerequisiti."
---

Questa API REST aggiorna l'asse valore secondario di un grafico.

**Prerequisiti:**  
- Un token di accesso JWT valido (vedi la [guida all'autenticazione](https://docs.aspose.cloud/cells/authentication/)).  
- Il file Excel di destinazione deve essere archiviato nell'archivio cloud di Aspose (fornire `folder` e facoltativamente `storageName`).  
- Viene utilizzata la versione API v3.0; assicurati che l'URL di base sia `https://api.aspose.cloud/v3.0`.

## API PostChartSecondValueAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                         |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name           | string  | path     | Nome del file Excel.                                |
| sheetName      | string  | path     | Nome del foglio di calcolo contenente il grafico.   |
| chartIndex     | integer | path     | Indice in base zero del grafico da modificare.      |
| axis           | object  | body     | Impostazioni per l'asse valore secondario.          |
| folder         | string  | query    | Percorso della cartella nell'archivio dove è situato il file. |
| storageName    | string  | query    | Nome del servizio di archiviazione.                 |

**Esempio di corpo della richiesta (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Asse secondario"
  }
}
```

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

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

**Codici di stato HTTP**

| Codice | significato                   | Descrizione                                        |
|--------|-------------------------------|----------------------------------------------------|
| 200    | OK                            | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida          | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato               | Token JWT non valido o mancante. |
| 413    | Payload troppo grande         | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server     | Errore imprevisto del server. |

**Vedi anche:**  
- [Ottieni Asse Valore Secondario del Grafico](https://docs.aspose.cloud/cells/it/charts/second-value-axis/get/)  
- [Aggiorna Asse Valore del Grafico](https://docs.aspose.cloud/cells/it/charts/value-axis/update/)

## Famiglia di SDK cloud

L'utilizzo di un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Esempio in C# per aggiornare l'asse valore secondario
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Esempio in Java per aggiornare l'asse valore secondario
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Esempio in PHP per aggiornare l'asse valore secondario
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Esempio in Ruby per aggiornare l'asse valore secondario
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Esempio in Python per aggiornare l'asse valore secondario
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
// Esempio in Android (Java) – identico al frammento Java riportato sopra
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Esempio in Swift per aggiornare l'asse valore secondario
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Esempio in Perl per aggiornare l'asse valore secondario
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Esempio in Go per aggiornare l'asse valore secondario
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}