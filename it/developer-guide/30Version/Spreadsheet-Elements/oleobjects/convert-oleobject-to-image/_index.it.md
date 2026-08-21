---
title: "Convertire OLE Object in Immagine – Aspose.Cells Cloud REST API"
description: "Recupera un oggetto OLE incorporato in un foglio di calcolo Excel e convertilo in PNG, JPEG, TIFF, GIF, EMF o BMP utilizzando l'API REST di Aspose.Cells Cloud."
keywords:
  - "convertire OLE object in immagine"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "conversione immagine"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# Convertire OLE Object in Immagine

Recupera un oggetto OLE incorporato in un foglio di calcolo e restituiscilo nel formato immagine richiesto.

---

## Prerequisiti

Prima di chiamare questo endpoint, assicurati di avere:

1. **Account Aspose.Cells Cloud** – registrati sul [portale Aspose Cloud](https://dashboard.aspose.cloud/).  
2. **Cartella di lavoro caricata nello storage cloud** – utilizza l’API **Upload File** o l’interfaccia utente di Aspose Cloud.  
3. **Token di accesso JWT** – ottieni un token seguendo la [guida all’autenticazione](/total/getting-started/rest-api-overview/authenticating-api-requests/).  

---

## Sicurezza e Autenticazione

Tutte le API di Aspose.Cells Cloud richiedono l’**autenticazione basata su token JWT**. Includi il token nell’intestazione `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

Sono supportati solo endpoint HTTPS; non utilizzare mai `http://`.

---

## Richiesta

### Metodo HTTP
`GET`

### Endpoint
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Parametri del percorso

| Nome          | Tipo   | Obbligatorio | Descrizione                              |
|---------------|--------|--------------|------------------------------------------|
| `name`        | string | ✅           | Nome del file della cartella di lavoro (es. `Book1.xlsx`). |
| `sheetName`   | string | ✅           | Foglio di calcolo contenente l’oggetto OLE. |
| `objectNumber`| integer| ✅           | Indice in base zero dell’oggetto OLE.      |

### Parametri di query

| Nome         | Tipo   | Obbligatorio | Descrizione |
|--------------|--------|--------------|-------------|
| `format`     | string | ❌           | Format immagine desiderato (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). Se omesso, il valore predefinito è `png`. |
| `folder`     | string | ❌           | Percorso della cartella in cui si trova la cartella di lavoro. |
| `storageName`| string | ❌           | Nome del servizio di storage (es. `MyCloud`). |

---

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*Sostituisci `<jwt-token>` con un token JWT valido.*

---

## Risposta

| Stato | Content‑Type            | Descrizione |
|-------|-------------------------|-------------|
| `200` | `image/png` (o il formato richiesto) | Dati binari dell’immagine che rappresentano l’oggetto OLE. |
| `400` | `application/json`      | Parametri della richiesta non validi. |
| `401` | `application/json`      | Autenticazione non riuscita (JWT mancante o non valido). |
| `404` | `application/json`      | La cartella di lavoro, il foglio di calcolo o l’oggetto OLE specificati non sono stati trovati. |
| `500` | `application/json`      | Errore lato server. |

### Gestione del payload binario

L’API restituisce byte immagine grezzi. Puoi:

* **Salvare direttamente su file** (esempio Linux/macOS):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **Codificare in Base64** per debug o per l’inserimento in JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *Esempio (troncato) di output Base64:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Risposte di errore

| Stato HTTP | Codice                 | Messaggio |
|------------|------------------------|---------|
| `400`      | `InvalidParameter`     | Uno o più parametri della richiesta non sono validi. |
| `401`      | `AuthenticationFailed`| Token JWT mancante o non valido. |
| `404`      | `PropertyNotFound`     | La cartella di lavoro, il foglio di calcolo o l’oggetto OLE richiesti non esistono. |
| `500`      | `InternalError`        | Si è verificato un errore imprevisto sul server. |

---

## Esempi con SDK

I frammenti seguenti mostrano come chiamare l’operazione utilizzando gli SDK ufficiali. Sostituisci `YOUR_JWT_TOKEN` e altri segnaposto con i tuoi valori effettivi.

| Linguaggio | Esempio |
|------------|---------|
| **C#** | <details><summary>Mostra codice</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Mostra codice</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Mostra codice</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Mostra codice</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Mostra codice</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Mostra codice</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Mostra codice</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Mostra codice</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(L’elenco completo degli SDK è disponibile nel [repository GitHub](https://github.com/aspose-cells-cloud).)*

---

## Operazioni correlate

- **Aggiungi OLE Object** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **Aggiorna OLE Object** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Elimina OLE Object** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Ottieni elenco OLE Object** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

Per dettagli, consulta le pagine di riferimento corrispondenti delle API.

---

## Risorse aggiuntive

- **Specifiche OpenAPI** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Guida all’autenticazione** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Repository SDK** – <https://github.com/aspose-cells-cloud>
- **Prestazioni e accessibilità** – Esegui audit con Lighthouse e axe‑core per garantire tempi di caricamento ottimali e conformità WCAG 2.1 AA.