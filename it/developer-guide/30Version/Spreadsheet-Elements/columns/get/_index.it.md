---
title: Ottieni Dettagli Colonna – Riferimento API Cloud di Aspose.Cells (v4.0)
description: Recupera informazioni dettagliate su una colonna di un foglio di calcolo (indice, larghezza, stile, stato visibilità) utilizzando l'API REST di Aspose.Cells Cloud.
keywords: Aspose.Cells, API Cloud, colonna Excel, Ottieni colonna, API REST, JWT, foglio di calcolo
date: 2026-07-30
---

# Ottieni Dettagli Colonna  

Recupera informazioni dettagliate su una colonna specifica di un foglio di calcolo (indice, larghezza, stile, stato visibilità) da un file Excel memorizzato in Aspose Cloud.

## Tabella dei Contenuti
1. [Prerequisiti](#prerequisiti)  
2. [Autenticazione](#autenticazione)  
3. [Endpoint](#endpoint)  
4. [Parametri della Richiesta](#parametri-della-richiesta)  
5. [Esempio cURL](#esempio-curl)  
6. [Esempio di Risposta](#esempio-di-risposta)  
7. [Schema di Risposta](#schema-di-risposta)  
8. [Errori Possibili](#errori-possibili)  
9. [Esempi SDK](#esempi-sdk)  
10. [Risorse Aggiuntive](#risorse-aggiuntive)  

---

## Prerequisiti
- Un **token di accesso JWT** valido ottenuto tramite l'autenticazione di Aspose Cloud.  
- Il file del foglio di calcolo deve essere memorizzato in Aspose Cloud Storage (o in un altro archivio supportato) e il percorso della cartella (se presente) deve essere noto.  

---

## Autenticazione
Tutte le API di Aspose.Cells Cloud utilizzano l'**autenticazione basata su token JWT**. Includi il token nell'intestazione `Authorization`:

```http
Authorization: Bearer <access_token>
```

Per maggiori dettagli su come ottenere un token, consulta la [guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Endpoint
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – nome del file del foglio di calcolo (ad esempio, `test.xlsx`).  
- **{sheetName}** – nome del foglio di calcolo (ad esempio, `Sheet1`).  
- **{columnIndex}** – indice in base zero della colonna da recuperare.

---

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

## Parametri della Richiesta

| Nome            | Posizione | Tipo    | Obbligatorio | Descrizione |
|-----------------|-----------|---------|--------------|-------------|
| **name**        | path      | string  | Sì           | Nome del file del foglio di calcolo. |
| **sheetName**   | path      | string  | Sì           | Foglio di calcolo contenente la colonna. |
| **columnIndex** | path      | integer | Sì           | Indice in base zero della colonna da recuperare. |
| **folder**      | query     | string  | No           | Cartella di archiviazione in cui risiede il foglio di calcolo. |
| **storageName** | query     | string  | No           | Nome del servizio di archiviazione (ad esempio, Aspose Cloud Storage). |

---

## Esempio cURL
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Esempio di Risposta
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Schema di Risposta
| Campo                   | Tipo    | Descrizione |
|-------------------------|---------|-------------|
| `Column.GroupLevel`     | integer | Livello di raggruppamento della colonna (utilizzato per il raggruppamento). |
| `Column.Index`          | integer | Indice in base zero della colonna. |
| `Column.IsHidden`       | boolean | `true` se la colonna è nascosta; altrimenti `false`. |
| `Column.Width`          | number  | Larghezza della colonna espressa in caratteri. |
| `Column.Style`          | object  | Contiene un `link` alla risorsa di stile della colonna. |
| `Column.link`           | object  | Link self alla risorsa della colonna. |
| `Code`                  | integer | Codice di stato HTTP della risposta. |
| `Status`                | string  | Descrizione testuale dello stato (ad esempio, **OK**). |

---

## Errori Possibili
| Stato HTTP | Codice | Messaggio                    | Quando si verifica |
|------------|--------|------------------------------|--------------------|
| 400        | 400    | Bad Request                  | Parametri obbligatori mancanti o malformati. |
| 401        | 401    | Unauthorized                 | Intestazione `Authorization` mancante o non valida. |
| 404        | 404    | Not Found                    | Il foglio di calcolo, il foglio di calcolo o la colonna non esistono. |
| 500        | 500    | Internal Server Error        | Problema imprevisto lato server. |

### Esempio – 404 Not Found
```json
{
  "Code": 404,
  "Message": "Indice colonna fuori intervallo."
}
```

### Esempio – 401 Unauthorized
```json
{
  "Code": 401,
  "Message": "Token di autenticazione non valido o mancante."
}
```

---

## Esempi SDK
I frammenti di codice seguenti illustrano come chiamare l'operazione **Get Worksheet Columns** utilizzando gli SDK ufficiali di Aspose.Cells Cloud. Qualora un Gist non fosse più disponibile, il codice di esempio è fornito direttamente nel blocco.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// Configura il client API
var apiInstance = new CellsApi("client_id", "client_secret");

// Imposta i parametri obbligatori
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // opzionale
string storageName = "MyStorage";    // opzionale

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Indice colonna: " + response.Column.Index);
    Console.WriteLine("Larghezza: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Eccezione durante la chiamata a CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // opzionale
        String storageName = "MyStorage";    // opzionale

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Indice colonna: " + result.getColumn().getIndex());
            System.out.println("Larghezza: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Eccezione durante la chiamata a CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # opzionale
storage_name = "MyStorage"  # opzionale

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Indice colonna:", response.column.index)
    print("Larghezza:", response.column.width)
except Exception as e:
    print("Eccezione durante la chiamata a CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // opzionale
const storageName = "MyStorage"; // opzionale

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Indice colonna:", result.column?.index);
        console.log("Larghezza:", result.column?.width);
    })
    .catch((error) => {
        console.error("Errore durante la chiamata a getWorksheetColumns:", error);
    });
```

</details>

> **Nota:** Tutti gli SDK gestiscono automaticamente l'intestazione `Authorization` dopo aver fornito `client_id` e `client_secret`.

---

## Risorse Aggiuntive
- **Specifica OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **Guida all'autenticazione:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Repository GitHub (SDK ed esempi):** <https://github.com/aspose-cells-cloud>  

--- 

*Documento aggiornato l’ultima volta il 2026-07-30.*