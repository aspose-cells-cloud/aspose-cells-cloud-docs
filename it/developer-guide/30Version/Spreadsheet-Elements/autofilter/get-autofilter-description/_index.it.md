---
---
title: "Ottieni AutoFiltro"
description: "Recupera la descrizione dell'AutoFiltro da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud."
keywords: "AutoFiltro, Excel, Aspose.Cells Cloud, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# Recuperare la descrizione dell'AutoFiltro da un foglio di calcolo

**Versione:** v3.0  
**Endpoint:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **Nota:** Tutti gli esempi di richiesta utilizzano **HTTPS**. Non inviare mai token JWT su connessioni non sicure.

---

## Panoramica

Un **AutoFiltro** consente agli utenti di filtrare le righe di un foglio di calcolo in base ai valori delle colonne, ai colori, ai criteri personalizzati e molto altro. Questa API restituisce la configurazione completa dell'AutoFiltro—including le colonne filtrate, l'intervallo e i dettagli di ordinamento—così da poter ispezionare o replicare programmaticamente le impostazioni di filtro.

---

## Prerequisiti

| Requisito | Descrizione |
|-----------|-------------|
| **Autenticazione** | È necessario un token JWT valido. Consulta la [guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Posizione del file** | Il libro di lavoro deve essere memorizzato in Aspose Cloud Storage (o in uno storage esterno collegato). |
| **Formati supportati** | Qualsiasi formato Excel supportato da Aspose.Cells (ad esempio, `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (opzionale)** | Se preferisci utilizzare un SDK, installa il pacchetto appropriato (ad esempio, `dotnet add package Aspose.Cells-Cloud` per .NET). |

---

## Richiesta

### Richiesta HTTP

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### Parametri del percorso

| Parametro   | Tipo   | Descrizione |
|-------------|--------|-------------|
| `name`      | string | **Obbligatorio.** Nome del file del libro di lavoro, inclusa l'estensione. |
| `sheetName` | string | **Obbligatorio.** Nome del foglio di calcolo da cui recuperare l'AutoFiltro. |

### Parametri di query

| Parametro     | Tipo   | Descrizione |
|---------------|--------|-------------|
| `folder`      | string | Percorso della cartella nello storage in cui si trova il libro di lavoro. |
| `storageName` | string | Nome dello storage da utilizzare. |

### Sicurezza

L'API utilizza l'**autenticazione basata su token JWT**. Includi il token nell'header `Authorization`:

```http
Authorization: Bearer <your_jwt_token>
```

---

## Esempio di richiesta (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Risposta

Il servizio restituisce un oggetto JSON che racchiude il modello `AutoFilter`.

### Schema della risposta riuscita

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### Esempio di risposta

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFiltro",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |
---

## Esempi di SDK

L'operazione è disponibile in tutti gli SDK di Aspose.Cells Cloud. Di seguito sono riportati frammenti pronti all'uso.

| Linguaggio | Esempio |
|------------|---------|
| **C#** | <details><summary>Mostra codice</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>Mostra codice</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>Mostra codice</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>Mostra codice</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Mostra codice</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>Mostra codice</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>Mostra codice</summary>```go\nimport (\n    "fmt"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), "Book1.xlsx", "Sheet1", "MyFolder", "MyStorage")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>Mostra codice</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

Per un elenco completo di SDK e istruzioni di installazione, visita il [repository GitHub di Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).

---

## Vedi anche

- [AutoFiltro – Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [Guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Operazioni sugli storage](https://docs.aspose.cloud/cells/storage/)  

---