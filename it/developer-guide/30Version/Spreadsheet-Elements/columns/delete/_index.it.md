---
---
title: "Elimina una colonna da un foglio di Excel usando l'API Aspose.Cells Cloud"
description: "Scopri come eliminare una o più colonne da un foglio di Excel tramite l'API REST Aspose.Cells Cloud. Include autenticazione, sintassi delle richieste, parametri, risposte, gestione degli errori ed esempi di SDK."
keywords: ["Aspose.Cells", "Elimina colonna", "Excel API", "REST", "Cloud", "Foglio di calcolo", "Colonne"]
date: 2026-07-30
api_version: "v3.0"
---

# Elimina una colonna da un foglio di Excel

**Endpoint**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

L'operazione rimuove una singola colonna o un intervallo di colonne da un foglio di calcolo. I riferimenti alle celle (inclusi formule) possono essere aggiornati automaticamente dopo l'eliminazione.

---

## Indice
1. [Prerequisiti](#prerequisiti)  
2. [Autenticazione](#autenticazione)  
3. [URL della richiesta e metodo HTTP](#url-della-richiesta-e-metodo-http)  
4. [Parametri](#parametri)  
   - [Parametri di percorso](#parametri-di-percorso)  
   - [Parametri di query](#parametri-di-query)  
5. [Esempio cURL](#esempio-curl)  
6. [Risposte](#risposte)  
7. [Codici di errore](#codici-di-errore)  
8. [Esempi di SDK](#esempi-di-sdk)  
9. [Note aggiuntive](#note-aggiuntive)  

---

## Prerequisiti
- Un **token di accesso JWT** valido ottenuto tramite il flusso di autenticazione di Aspose Cloud.  
- Il workbook (`{name}`) deve essere già caricato nell'archivio Aspose Cloud (o accessibile tramite i parametri di query `folder`/`storageName`).  

---

## Autenticazione
Tutte le richieste a Aspose.Cells Cloud richiedono l'autenticazione tramite **token Bearer**.

```http
Authorization: Bearer <access_token>
```

Consultare la [guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) per ulteriori dettagli su come ottenere un token JWT.

---

## URL della richiesta e metodo HTTP
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – nome del file del workbook (es. `test.xlsx`).  
- **`{sheetName}`** – nome del foglio di calcolo (es. `Sheet1`).  
- **`{columnIndex}`** – indice in base zero della prima colonna da eliminare.

---

## Parametri

| Nome            | Posizione | Tipo    | Obbligatorio | Descrizione |
|-----------------|-----------|---------|--------------|-------------|
| **name**        | path      | stringa | ✅ Sì        | Nome del file del workbook. |
| **sheetName**   | path      | stringa | ✅ Sì        | Nome del foglio di calcolo. |
| **columnIndex** | path      | intero  | ✅ Sì        | Indice in base zero della prima colonna da eliminare. |
| **startColumn** | query     | intero  | ❌ No        | Indice in base zero da cui inizia l'eliminazione. Se omesso, assume il valore di `columnIndex`. |
| **totalColumns**| query     | intero  | ❌ No        | Numero di colonne da eliminare. Se omesso, viene eliminata solo la colonna identificata da `columnIndex`. |
| **updateReference** | query | booleano | ❌ No     | Se `true`, aggiorna i riferimenti alle celle (inclusi formule) in tutto il workbook dopo l'eliminazione. |
| **folder**      | query     | stringa | ❌ No        | Percorso della cartella contenente il workbook. |
| **storageName** | query     | stringa | ❌ No        | Nome del servizio di archiviazione Aspose Cloud. |

> **Nota** – Il parametro `columns` indicato nella specifica dell'API di basso livello è stato sostituito dai più espressivi parametri di query `startColumn` e `totalColumns`. Entrambi gli approcci sono accettati per compatibilità all'indietro.

---

## Esempio cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Spiegazione
- Elimina la colonna **B** (`columnIndex = 1`) da `Sheet1` di `test.xlsx`.  
- `startColumn=1` e `totalColumns=1` specificano l'eliminazione di una singola colonna.  
- `updateReference=true` garantisce che formule e altri riferimenti vengano aggiornati automaticamente.

---

## Risposte

| Codice HTTP | Descrizione | Esempio |
|-------------|-------------|---------|
| **200** | Esito positivo – le colonne sono state eliminate. | `{ "Code": 200, "Status": "OK" }` |
| **400** | Richiesta non valida – parametri mancanti o non validi. | `{ "Code": 400, "Message": "Valore totalColumns non valido." }` |
| **401** | Non autorizzato – token JWT mancante o non valido. | `{ "Code": 401, "Message": "Autenticazione non riuscita." }` |
| **404** | Non trovato – il workbook o il foglio di calcolo non esiste. | `{ "Code": 404, "Message": "Foglio 'Sheet1' non trovato." }` |
| **500** | Errore interno del server – condizione imprevista sul server. | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

Il corpo della risposta segue il modello generico **`CellsCloudResponse`**.

---

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto sul server. |
---

## Esempi di SDK

Di seguito sono riportati frammenti di codice pronti all'uso per gli SDK più diffusi. Sostituire i valori segnaposto (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>`, ecc.) con i propri dati.

| Lingua | Esempio |
|--------|---------|
| **C#** | <details><summary>Mostra codice</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>Mostra codice</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Mostra codice</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Eccezione durante la chiamata a CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>Mostra codice</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Mostra codice</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Errore:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Mostra codice</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Eccezione: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>Mostra codice</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Eccezione durante la chiamata a CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Mostra codice</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*Tutti gli SDK aggiungono automaticamente l'header `Authorization` richiesto quando `access_token` è configurato.*

---

## Note aggiuntive

### Header di sicurezza (consigliato per produzione)
Durante la generazione della pagina di documentazione, includere i seguenti header HTTP nella risposta per migliorare la sicurezza:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Suggerimenti per le prestazioni
- Caricare gli script di analisi di terze parti (`gtag.js`, `containerize.js`) con l'attributo `async` o posticiparne l'esecuzione fino al completamento del rendering della pagina.  
- Minificare eventuali bundle JavaScript/CSS personalizzati.  
- Pre-caricare icone SVG piccole che bloccano il rendering:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### Miglioramenti SEO (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Elimina una colonna da un foglio di Excel usando l'API Aspose.Cells Cloud",
  "description": "Scopri come eliminare una o più colonne da un foglio di Excel tramite l'API REST Aspose.Cells Cloud.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Elimina colonna", "Excel", "REST API"]
}
```

Inserire il frammento all'interno di un blocco `<script type="application/ld+json">` nell'header HTML.

### Accessibilità
- Tutte le immagini decorative utilizzano `alt=""` o sono nascoste con `aria-hidden="true"`.  
- L'immagine Open Graph include ora un attributo `alt` nel meta tag per completezza.  

---

## Vedi anche
- [Specifica OpenAPI per DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Panoramica sull'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [SDK Aspose.Cells Cloud su GitHub](https://github.com/aspose-cells-cloud)  

---
---