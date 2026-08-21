---
title: "Copia righe in un foglio di calcolo Excel"
description: "Copia dati e formati da righe specifiche intere in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include autenticazione, dettagli di richiesta/risposta, gestione degli errori ed esempi di SDK."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Copia righe in un foglio di calcolo Excel <span style="float:right;">v3.0</span>

Copia dati e formati da righe specifiche intere in un foglio di calcolo.

---

## Prerequisiti

| # | Requisito |
|---|-----------|
| 1 | Un token **JWT** valido. Consulta la [guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | Il workbook (`{name}`) deve già esistere nella **cartella** / **archivio** selezionata. |
| 3 | Il foglio di destinazione (`{sheetName}`) deve essere presente nel workbook. |
| 4 | (Opzionale) Conoscere la **cartella** e il **storageName** se il file non si trova nella posizione predefinita. |

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*Tutti i parametri del percorso sono distingui maiuscole/minuscole.*

### Parametri del percorso

| Parametro | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|--------------|-------------|
| `name`    | string | ✅ | Nome del file del workbook (es. `test.xlsx`). |
| `sheetName` | string | ✅ | Nome del foglio di calcolo (es. `Sheet1`). |

### Parametri di query

| Parametro            | Tipo    | Obbligatorio | Descrizione |
|----------------------|---------|--------------|-------------|
| `sourceRowIndex`     | integer | ✅ | Indice in base zero della riga di origine. |
| `destinationRowIndex`| integer | ✅ | Indice in base zero dove verranno inserite le righe. |
| `rowNumber`          | integer | ✅ | Numero di righe da copiare. |
| `worksheet`          | string  | ❌ | Identificatore del foglio di calcolo; di solito uguale a **sheetName**. |
| `folder`             | string  | ❌ | Percorso della cartella contenente il workbook. |
| `storageName`        | string  | ❌ | Nome del servizio di archiviazione. |

---

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota**  
> Sostituisci `<jwt token>` con un token JWT valido ottenuto dal servizio di autenticazione.

---

## Risposta in caso di successo

| Codice | Descrizione |
|--------|-------------|
| **200** | Righe copiate con successo. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Il corpo della risposta è un'istanza di `CellsCloudResponse`.

---

## Gestione degli errori

| Codice HTTP | Significato | Corpo dell'esempio |
|-------------|-------------|--------------------|
| **400** | Richiesta non valida – parametri mancanti/errati. | `{ "Code": 400, "Message": "sourceRowIndex non valido." }` |
| **401** | Non autorizzato – token JWT non valido o mancante. | `{ "Code": 401, "Message": "Autenticazione non riuscita." }` |
| **404** | Non trovato – workbook o foglio di calcolo inesistente. | `{ "Code": 404, "Message": "File non trovato." }` |
| **500** | Errore interno del server – condizione imprevista del server. | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

**Linee guida per la gestione**

* **400** – Verifica che tutti i parametri di query obbligatori siano presenti e formattati correttamente.  
* **401** – Rigenera o aggiorna il token JWT.  
* **404** – Conferma i nomi del workbook e del foglio di calcolo e assicurati che il file esista nella cartella/archivio specificata.  
* **500** – Riprova dopo un breve ritardo; se il problema persiste, contatta il supporto Aspose.

---

## Esempi di SDK

I frammenti seguenti mostrano come richiamare l'operazione **Copia righe** utilizzando gli SDK ufficiali di Aspose.Cells Cloud.

| Lingua | Esempio |
|--------|---------|
| **C#**   | <details><summary>Mostra codice</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Mostra codice</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Mostra codice</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Mostra codice</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Mostra codice</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Mostra codice</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Mostra codice</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Mostra codice</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*I file sorgente completi sono disponibili nel repository GitHub [Aspose‑Cells‑Cloud](https://github.com/aspose-cells-cloud).*

---

## Vedi anche

- [Aggiungi riga in un foglio di calcolo Excel](/rows/add/)  
- [Elimina riga in un foglio di calcolo Excel](/rows/delete/)  
- [Aggiorna riga in un foglio di calcolo Excel](/rows/update/)  

--- 

*Pagina generata il **{{DATE}}**. Per la versione più recente di questa API, consulta la [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*