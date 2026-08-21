---
title: "Elimina collegamento ipertestuale del foglio di lavoro"
type: docs
url: /it/hyperlinks/delete/
description: "Elimina un collegamento ipertestuale del foglio di lavoro per indice tramite l'API di Aspose.Cells Cloud. Scopri i parametri richiesti, l'autenticazione e consulta esempi di codice per C#, Java, Python e altro ancora."
keywords: "Aspose.Cells, Cloud, elimina collegamento ipertestuale, API Excel, REST, collegamento ipertestuale foglio di lavoro"
ArticleTitle: "Elimina collegamento ipertestuale del foglio di lavoro – Documentazione API Aspose.Cells Cloud"
weight: 40
---

Questa REST API elimina un collegamento ipertestuale del foglio di lavoro tramite il suo indice in un foglio di lavoro Excel.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/it/total/getting-started/rest-api-overview/authenticating-api-requests/).

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Parametri della richiesta

| Nome parametro      | Tipo    | Posizione | Obbligatorio | Descrizione                                                     |
| ------------------- | ------- | --------- | ------------ | --------------------------------------------------------------- |
| **name**            | string  | path      | ✅           | Nome del documento Excel.                                       |
| **sheetName**       | string  | path      | ✅           | Nome del foglio di lavoro.                                      |
| **hyperlinkIndex**  | integer | path      | ✅           | Indice in base zero del collegamento ipertestuale da eliminare. |
| **folder**          | string  | query     | ❌           | Cartella contenente il documento (impostazione predefinita: root). |
| **storageName**     | string  | query     | ❌           | Nome del servizio di archiviazione (se omesso, viene usato l'archiviazione predefinita). |

#### Risposte

| Codice di stato               | Descrizione                                              | Corpo di esempio                                  |
| ----------------------------- | -------------------------------------------------------- | ------------------------------------------------- |
| **200 OK**                    | Collegamento ipertestuale eliminato con successo.        | `{"Code":200,"Status":"OK"}`                      |
| **400 Bad Request**           | Parametri mancanti o non validi.                         | `{"Code":400,"Message":"hyperlinkIndex non valido."}` |
| **401 Unauthorized**          | Token di autenticazione mancante o non valido.           | `{"Code":401,"Message":"Token di accesso non valido."}` |
| **404 Not Found**             | Il file, il foglio di lavoro o l'indice del collegamento ipertestuale non esiste. | `{"Code":404,"Message":"Risorsa non trovata."}`     |
| **500 Internal Server Error** | Errore imprevisto del server.                            | `{"Code":500,"Message":"Errore interno del server."}`  |

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
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

## Famiglia di SDK per il cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK. Sono forniti frammenti inline per garantire l'affidabilità; per riferimento viene mantenuto un link al Gist originale.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Origine: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Origine: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Origine: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
// Origine: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Origine: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Collegamento ipertestuale eliminato"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
// Origine: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Collegamento ipertestuale eliminato')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
// Origine: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Origine: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Collegamento ipertestuale eliminato")
    }
}
```

{{< /tab >}}

{{< /tabs >}}