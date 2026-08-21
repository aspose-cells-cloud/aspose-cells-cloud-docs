---
title: Elimina interruzione di pagina verticale – Aspose.Cells Cloud REST API
description: Rimuovi un'interruzione di pagina verticale da un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include la sintassi della richiesta, i parametri, gli esempi, i codici di risposta e frammenti di codice per gli SDK.
keywords: elimina interruzione di pagina verticale, Aspose.Cells Cloud, API REST
slug: delete-vertical-page-break
api_version: v3.0
---

# Elimina interruzione di pagina verticale

Elimina un'interruzione di pagina verticale da un foglio di calcolo in un file Excel utilizzando l'API REST Aspose.Cells Cloud.

---

## Prerequisiti

* Un **token di autenticazione JWT** deve essere fornito nell'header `Authorization`.  
* Il file Excel (`{name}`) deve essere memorizzato nella **cartella** o **archivio** specificato e deve essere accessibile al client API.

---

## Richiesta HTTP

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Parametro | Tipo   | Posizione | Obbligatorio | Descrizione |
|-----------|--------|-----------|--------------|-------------|
| **name**      | string | path      | Sì           | Nome del file Excel. |
| **sheetName** | string | path      | Sì           | Nome del foglio di calcolo contenente l'interruzione di pagina. |
| **index**     | integer| path      | Sì           | Indice in base zero dell'interruzione di pagina verticale da eliminare. |
| **folder**    | string | query     | No           | Percorso della cartella in cui è memorizzato il file. |
| **storageName**| string| query     | No           | Nome del servizio di archiviazione. |

---

## Esempio di richiesta

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Risposta in caso di esito positivo

| Codice | Descrizione |
|--------|-------------|
| **200** | L'interruzione di pagina verticale è stata eliminata correttamente. |

**Esempio di payload**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Risposte di errore

| Codice HTTP | Descrizione |
|-------------|-------------|
| **401** | Non autorizzato – token mancante o non valido. |
| **404** | Non trovato – il file, il foglio di calcolo o l'indice dell'interruzione di pagina specificati non esistono. |
| **400** | Richiesta non valida – sintassi della richiesta errata o parametri non validi. |
| **500** | Errore interno del server – si è verificata una condizione imprevista. |

**Esempi di payload di errore**

*401 – Non autorizzato*

```json
{
  "Code": 401,
  "Message": "Token di autenticazione non valido."
}
```

*404 – Non trovato*

```json
{
  "Code": 404,
  "Message": "Il file, il foglio di calcolo o l'indice dell'interruzione di pagina specificati non sono stati trovati."
}
```

*400 – Richiesta non valida*

```json
{
  "Code": 400,
  "Message": "I parametri della richiesta non sono validi o sono malformati."
}
```

*500 – Errore interno del server*

```json
{
  "Code": 500,
  "Message": "Si è verificato un errore imprevisto nel server."
}
```

---

## Esempi di codice SDK

I seguenti esempi mostrano come chiamare l'operazione **DeleteVerticalPageBreak** utilizzando vari SDK di Aspose.Cells Cloud.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Eccezione durante la chiamata a CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Errore:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Errore:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Errore:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(I frammenti di codice per PHP, Ruby, Perl e altri linguaggi seguono lo stesso schema e sono disponibili nel repository ufficiale su GitHub.)*

---

## Risorse correlate

* **Specifica OpenAPI** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **SDK di Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>  
* **Guida all'autenticazione** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*Documento aggiornato l'ultima volta il: 2026‑07‑30*