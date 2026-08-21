---
title: "Aggiornare un collegamento ipertestuale in un foglio di calcolo Excel – Guida all’API Aspose.Cells Cloud"
description: "Scopri come aggiornare un collegamento ipertestuale in un foglio di calcolo Excel utilizzando l’API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, schema del corpo della richiesta, esempio cURL, frammenti di codice SDK, gestione degli errori, limitazione della frequenza e prerequisiti."
keywords:
  - "Aspose.Cells"
  - "aggiornamento collegamento ipertestuale"
  - "Excel API"
  - "REST API"
  - "foglio di calcolo cloud"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Aggiornare un collegamento ipertestuale in un foglio di calcolo Excel  

**Versione API:** v3.0  

L’operazione **PostWorksheetHyperlink** aggiorna un collegamento ipertestuale esistente in un foglio di calcolo identificato dal suo indice in base zero.

---

## Indice
1. [Prerequisiti](#prerequisiti)  
2. [Limitazione della frequenza](#limitazione-della-frequenza)  
3. [Endpoint](#endpoint)  
4. [Parametri](#parametri)  
   - [Parametri di percorso](#parametri-di-percorso)  
   - [Parametri di query](#parametri-di-query)  
   - [Schema del corpo della richiesta](#schema-del-corpo-della-richiesta)  
5. [Risposte](#risposte)  
   - [Risposta di successo](#risposta-di-successo)  
   - [Risposte di errore](#risposte-di-errore)  
6. [Esempio cURL](#esempio-curl)  
7. [Frammenti di codice SDK](#frammenti-di-codice-sdk)  
8. [Vedi anche](#vedi-anche)  

---

## Prerequisiti <a name="prerequisiti"></a>

| Requisito | Descrizione |
|-----------|-------------|
| **Autenticazione** | Autenticazione basata su token JWT. Ottieni un token come descritto nella [Guida all’autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Archiviazione** | Il file di lavoro deve essere memorizzato in un’archiviazione supportata da Aspose Cloud (quella predefinita è **Default**). |
| **Autorizzazioni** | Il token JWT deve avere i permessi di lettura e scrittura sul file di lavoro di destinazione. |
| **Intestazioni** | `Content-Type: application/json` e `Accept: application/json` sono obbligatorie per tutte le richieste. |

---

## Limitazione della frequenza <a name="limitazione-della-frequenza"></a>

Aspose.Cells Cloud impone un **massimo di 60 richieste al minuto per ogni token di accesso**. Superare questo limite restituisce l’errore HTTP **429 Too Many Requests (Troppe richieste)**. Implementa un ritardo esponenziale o rispetta l’intestazione `Retry-After` quando si verifica il throttling.

---

## Endpoint <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*Aggiorna il collegamento ipertestuale identificato da `hyperlinkIndex` nel foglio `sheetName` del file `name`.*

---

## Parametri <a name="parametri"></a>

### Parametri di percorso <a name="parametri-di-percorso"></a>

| Nome            | Tipo   | Obbligatorio | Descrizione |
|-----------------|--------|--------------|-------------|
| `name`          | stringa | ✅ | Nome del file Excel (inclusa l’estensione). |
| `sheetName`     | stringa | ✅ | Nome del foglio di calcolo contenente il collegamento ipertestuale. |
| `hyperlinkIndex`| intero | ✅ | Indice in base zero del collegamento ipertestuale da aggiornare. |

### Parametri di query <a name="parametri-di-query"></a>

| Nome        | Tipo   | Obbligatorio | Descrizione |
|-------------|--------|--------------|-------------|
| `folder`    | stringa | ❌ | Percorso della cartella nell’archiviazione dove risiede il file di lavoro. |
| `storageName`| stringa | ❌ | Nome del servizio di archiviazione (es. `Default`). |

### Schema del corpo della richiesta <a name="schema-del-corpo-della-richiesta"></a>

Il corpo della richiesta deve contenere un oggetto **`hyperlink`**. Devono essere forniti solo i campi che si desidera modificare; i campi facoltativi omessi mantengono i loro valori attuali.

| Campo         | Tipo   | Obbligatorio | Descrizione |
|---------------|--------|--------------|-------------|
| `Address`     | stringa | ✅ | URL di destinazione del collegamento ipertestuale. |
| `Area`        | oggetto | ✅ | Intervallo di celle in cui è posizionato il collegamento ipertestuale. Deve contenere `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (tutti interi, in base zero). |
| `ScreenTip`   | stringa | ❌ | Suggerimento visualizzato al passaggio del mouse. |
| `TextToDisplay`| stringa | ❌ | Testo visualizzato all’interno della cella. |
| `link`        | oggetto | ❌ | Link ipertestuali (`Href`, `Rel`, `Title`, `Type`). Generalmente omesso nei payload di richiesta. |

**Definizione dell’oggetto `Area`**

| Sottocampo   | Tipo   | Obbligatorio | Descrizione |
|--------------|--------|--------------|-------------|
| `StartRow`   | intero | ✅ | Indice della riga iniziale in base zero. |
| `StartColumn`| intero | ✅ | Indice della colonna iniziale in base zero. |
| `EndRow`     | intero | ✅ | Indice della riga finale in base zero. |
| `EndColumn`  | intero | ✅ | Indice della colonna finale in base zero. |

---

## Risposte <a name="risposte"></a>

### Risposta di successo <a name="risposta-di-successo"></a>

| Campo | Tipo   | Descrizione |
|-------|--------|-------------|
| `Code`| intero | Codice di stato HTTP (200 per successo). |
| `Status`| stringa | Stato in forma testuale (`OK`). |
| `Hyperlink`| oggetto (opzionale) | L’oggetto collegamento ipertestuale aggiornato, restituito quando viene richiesto l’oggetto secondario `link`. |

**Esempio JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Risposte di errore <a name="risposte-di-errore"></a>

| Codice HTTP | Motivo | Corpo di esempio |
|-------------|--------|-----------------|
| **400** | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore di parametro non valido." }` |
| **401** | Non autorizzato – token JWT mancante o non valido. | `{ "Code":"401", "Message":"Token di accesso mancante o non valido." }` |
| **404** | Non trovato – il file di lavoro, il foglio di calcolo o il collegamento ipertestuale non esistono. | `{ "Code":"404", "Message":"File non trovato." }` |
| **429** | Troppe richieste – limite di frequenza superato. | `{ "Code":"429", "Message":"Limite di richieste superato. Riprovare più tardi." }` |
| **500** | Errore interno del server – errore imprevisto nel server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

---

## Esempio cURL <a name="esempio-curl"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "Homepage MSNBC",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Risposta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Suggerimento:* Salva il payload JSON in un file (es. `payload.json`) e fai riferimento ad esso con `--data @payload.json` per una copia-incolla più pulita.

---

## Frammenti di codice SDK <a name="frammenti-di-codice-sdk"></a>

I seguenti frammenti mostrano come chiamare **PostWorksheetHyperlink** utilizzando gli SDK ufficiali di Aspose.Cells Cloud. Sostituisci i valori segnaposto (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>`, ecc.) con dati reali.

| Linguaggio | Esempio |
|-----------|---------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"Homepage MSNBC\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"Homepage MSNBC\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"Homepage MSNBC\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'Homepage MSNBC',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"Homepage MSNBC\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('Homepage MSNBC');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'Homepage MSNBC',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'Homepage MSNBC', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*Tutti gli SDK sono open-source e sono disponibili nel [repository GitHub di Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

---

## Vedi anche <a name="vedi-also"></a>

- **Autenticazione** – [Introduzione ai token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Operazioni su archiviazione** – [Caricamento di un file](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Altre operazioni sui collegamenti ipertestuali** – [Aggiungere un collegamento ipertestuale](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [Eliminare un collegamento ipertestuale](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **Specifiche OpenAPI** – Definizione completa dell’endpoint: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

---

*Documento aggiornato l’ultima volta il: 2026‑07‑30*