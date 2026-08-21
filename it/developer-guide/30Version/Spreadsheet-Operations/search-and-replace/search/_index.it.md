---
title: "Cercare testo nei file Excel – Aspose.Cells Cloud API"
description: "Cerca testo specifico in file Excel (XLS, XLSX, XLSM, XLSB) e ODS utilizzando l'API Aspose.Cells Cloud. Include dettagli della richiesta, esempi cURL e SDK, nonché gestione degli errori."
keywords: "Aspose.Cells, Excel, ricerca, API, REST"
type: docs
url: /it/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Cercare testo nei file Excel – Aspose.Cells Cloud API

## Panoramica
Aspose.Cells Cloud fornisce un endpoint **POST** che consente di cercare una stringa di testo all'interno di cartelle di lavoro Excel (XLS, XLSX, XLSM, XLSB) e di file di fogli di calcolo OpenDocument (ODS). L'API restituisce ogni cella contenente il testo richiesto, insieme a un collegamento al foglio di calcolo in cui è stata trovata la corrispondenza.

> **Casi d’uso**  
> - Convalidare che un valore specifico esista in un report prima di procedere con ulteriori elaborazioni.  
> - Creare uno strumento rapido di "trova e sostituisci" che elenchi innanzitutto tutte le occorrenze.  
> - Generare un indice di termini chiave in un batch di fogli di calcolo.

---

## Prerequisiti
| Requisito | Dettagli |
|-----------|----------|
| **Autenticazione** | Token JWT ottenuto tramite il flusso OAuth di Aspose Cloud. Il token deve includere l’ambito **Cells**. |
| **Formati supportati** | XLS, XLSX, XLSM, XLSB, ODS |
| **Dimensione massima del file** | 150 MB (compressi). File più grandi generano l’errore **413 Payload Too Large**. |
| **Intestazioni obbligatorie** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **Autorizzazioni** | Il token deve avere il permesso di *lettura* sull’archivio di destinazione (se si utilizza un archivio remoto); non è richiesto quando il file viene caricato come `multipart/form-data`. |

*Suggerimento:* Utilizza l’endpoint **/connect/token** per generare un token JWT. Consulta la [Guida all’autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) per maggiori dettagli.

---

## Endpoint

| Elemento | Valore |
|----------|--------|
| **Metodo HTTP** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **Scopo** | Cerca il testo specificato all’interno di una cartella di lavoro Excel caricata. |
| **Sicurezza** | Token JWT (Bearer) – consulta i *Prerequisiti* sopra. |

---

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

## Parametri della richiesta

| Nome | Tipo | Posizione | Obbligatorio | Descrizione |
|------|------|-----------|--------------|-------------|
| `file` | **file** | `formData` (multipart) | **Sì** | Il file del foglio di calcolo da caricare. |
| `text` | **string** | Query string | **Sì** | La stringa di testo da cercare. |
| `password` | **string** | Query string | No | Password per aprire una cartella di lavoro protetta, se richiesta. |
| `sheetname` | **string** | Query string | No | Nome del foglio di calcolo da limitare alla ricerca. Se omesso, vengono cercati tutti i fogli. |
| `checkExcelRestriction` | **boolean** | Query string | No (default: `true`) | Quando impostato su `true`, l’API convalida le restrizioni specifiche di Excel (ad esempio, celle di sola lettura) prima di effettuare la ricerca. |

---

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

*Sostituisci `<jwt-token>` con un token valido e regola i parametri della query in base alle tue esigenze.*

---

## Risposta in caso di successo

**HTTP 200 – Ricerca riuscita; la risposta contiene gli elementi di testo trovati.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Campi della risposta

| Campo | Tipo | Descrizione |
|-------|------|-------------|
| `Status` | string | Stato complessivo della richiesta (`OK` in caso di successo). |
| `Code` | integer | Codice di stato HTTP (200). |
| `TextItems.link` | object | Link ipermedia al collection resource. |
| `TextItems.TextItemList` | array | Elenco delle corrispondenze. Ogni elemento contiene: |
| `Text` | string | Valore della cella che ha trovato corrispondenza con il testo cercato. |
| `link` | object | Link ipermedia al foglio di calcolo in cui è stata trovata la corrispondenza (`Href` punta a `Workbook/worksheets/SheetName`). |

---

## Risposte di errore

| Codice HTTP | Significato | Causa tipica | Corpo dell’esempio |
|-------------|-------------|--------------|--------------------|
| **400** | Richiesta non valida | Parametri obbligatori mancanti, tipo di file non supportato o valori di query non validi. | `{ "Status":"Error","Code":400,"Message":"Il parametro di query 'text' è obbligatorio." }` |
| **401** | Non autorizzato | Token JWT mancante o non valido. | `{ "Status":"Error","Code":401,"Message":"Token di accesso non valido o scaduto." }` |
| **413** | Payload troppo grande | Il file caricato supera il limite di 150 MB. | `{ "Status":"Error","Code":413,"Message":"La dimensione del file supera il limite consentito." }` |
| **500** | Errore interno del server | Problema imprevisto lato server. | `{ "Status":"Error","Code":500,"Message":"Si è verificato un errore imprevisto." }` |

---

## Esempi di SDK

Di seguito sono riportati frammenti di codice minimi per l’operazione **PostSearch** utilizzando gli SDK ufficiali di Aspose.Cells Cloud. Sostituisci `YOUR_JWT_TOKEN` e il percorso del file con i tuoi valori.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(Gli SDK per PHP, Ruby, Go e Perl sono disponibili nel [repository GitHub di Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).)*

---

## Note aggiuntive

- **`checkExcelRestriction`** ha come valore predefinito `true`. Impostalo su `false` solo se sei certo che la cartella di lavoro non contenga celle protette che potrebbero interferire con la ricerca.
- L’API restituisce **link ipermedia** (`Href`) che possono essere utilizzati con altri endpoint di Aspose.Cells Cloud (ad esempio, per scaricare il foglio di calcolo o recuperare la formattazione delle celle).
- Quando si cercano in cartelle di lavoro di grandi dimensioni, considera di ridurre l’ambiente di ricerca mediante il parametro `sheetname` per migliorare i tempi di risposta.

---

## Link correlati

- **Guida all’autenticazione** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Specifiche OpenAPI per PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **SDK di Aspose.Cells Cloud** – <https://github.com/aspose-cells-cloud>
- **Limiti e quote** – <https://docs.aspose.cloud/total/getting-started/limits/>

---