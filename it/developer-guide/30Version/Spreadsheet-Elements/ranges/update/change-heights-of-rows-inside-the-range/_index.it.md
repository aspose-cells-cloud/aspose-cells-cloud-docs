---
title: "Imposta l'altezza delle righe per un intervallo in Excel – Aspose.Cells Cloud API (v3.0)"
description: "Modifica l'altezza delle righe all'interno di un intervallo specifico di un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, esempio cURL, risposte di esempio e frammenti di SDK per più linguaggi."
keywords: "Aspose.Cells, altezza riga, intervallo, Excel, API REST, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Imposta l'altezza delle righe per un intervallo in Excel

Questa operazione aggiorna l'altezza delle righe di un intervallo specificato su un foglio di calcolo memorizzato nell'archivio cloud di Aspose.

## Prerequisiti / Autenticazione

È necessario ottenere un token di accesso JWT dal servizio OAuth di Aspose Cloud con l'ambito **Cells.ReadWrite**.

Includere il token nell'intestazione `Authorization` di ogni richiesta:

```http
Authorization: Bearer <jwt token>
```

Se non si dispone di un token, seguire la **guida all'autenticazione di Aspose Cloud** per richiederne uno.

## Richiesta HTTP

| Metodo | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### Parametri del percorso

| Nome | Tipo | Descrizione |
|------|------|-------------|
| `name` | `string` | **Obbligatorio.** Il nome del file Excel memorizzato nel cloud. |
| `sheetName` | `string` | **Obbligatorio.** Il foglio di calcolo contenente l'intervallo di destinazione. |

### Parametri di query

| Nome | Tipo | Obbligatorio | Descrizione |
|------|------|--------------|-------------|
| `value` | `number` | **Sì** | Altezza desiderata della riga (in punti) da applicare all'intervallo. |
| `folder` | `string` | No | Percorso della cartella nell'archivio in cui si trova il file. |
| `storageName` | `string` | No | Nome del servizio di archiviazione (se sono configurati più archivi). |

### Corpo della richiesta (JSON)

Il corpo deve contenere un oggetto **Range** che definisce quali righe sono interessate.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Schema JSON per Range

| Proprietà | Tipo | Obbligatorio | Descrizione |
|-----------|------|--------------|-------------|
| `FirstRow` | integer | **Sì** | Indice in base zero della prima riga nell'intervallo. |
| `RowCount` | integer | **Sì** | Numero di righe alle quali verrà applicata l'altezza. |
| `FirstColumn` | integer | No | Indice in base zero della prima colonna (opzionale per l'operazione di altezza riga). |
| `ColumnCount` | integer | No | Numero di colonne interessate dall'intervallo (opzionale). |

Solo le proprietà elencate sopra vengono utilizzate per l'operazione di altezza riga; eventuali campi aggiuntivi vengono ignorati.

## Esempio di richiesta

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### Risposta di esempio (Successo)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

Tutte le risposte contengono un `Code` numerico e un `Status` leggibile (o `Message` in caso di errore). Quando si verifica un errore, potrebbero essere forniti ulteriori dettagli nell'oggetto `ErrorDetails`.

## Esempi di SDK

I frammenti seguenti mostrano come chiamare **Set Row Height for a Range** utilizzando gli SDK ufficiali di Aspose.Cells Cloud.

| Linguaggio | Esempio |
|------------|---------|
| **C#** | <details><summary>Mostra codice</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>Mostra codice</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>Mostra codice</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>Mostra codice</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Altezza riga impostata'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Mostra codice</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>Mostra codice</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>Mostra codice</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>Mostra codice</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **Nota:** Tutti gli SDK aggiungono automaticamente l'intestazione obbligatoria `Authorization: Bearer` quando il token di accesso è configurato.

## Vedi anche

- **Specifiche OpenAPI** – Contratto dettagliato per questa operazione: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Repository degli SDK di Aspose.Cells Cloud** – Codice sorgente e binding aggiuntivi per altri linguaggi: <https://github.com/aspose-cells-cloud>
- **Guida all'autenticazione** – Come ottenere un token JWT: <https://docs.aspose.cloud/cells/authentication/>

---