---
title: "Lavorare con i filtri pivot"
second_title: "Documento"
linktitle: Filtri
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Aspose.Cells, Tabella pivot, Filtro, REST API, Cloud"
description: "Scopri come aggiungere, recuperare ed eliminare i filtri della tabella pivot utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi delle richieste, i parametri obbligatori, un esempio cURL e frammenti di codice SDK per C# e Go."
weight: 50
ArticleTitle: "Lavorare con i filtri pivot – Documentazione di Aspose.Cells Cloud"
---

Questa API REST aggiunge un **filtro pivot** alla tabella pivot presente all'indice specificato.

**Prerequisiti**  
Prima di chiamare questo endpoint è necessario:

- Generare un token di accesso OAuth/JWT valido e includeerlo nell'intestazione `Authorization`.
- Assicurarsi che il foglio di calcolo di destinazione sia archiviato in una cartella cloud a cui si ha accesso (specificare `folder` e opzionalmente `storageName`).
- Utilizzare la versione 3.0 o successiva dell'API REST di Aspose.Cells Cloud.

## API PutWorksheetPivotTableFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Sicurezza e autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro      | Tipo    | Posizione | Descrizione                                                                                     |
| ------------------- | ------- | -------- | ----------------------------------------------------------------------------------------------- |
| **name**            | string  | path     | Nome del file Excel.                                                                            |
| **sheetName**       | string  | path     | Foglio di calcolo contenente la tabella pivot.                                                  |
| **pivotTableIndex** | integer | path     | Indice in base zero della tabella pivot alla quale applicare il filtro.                         |
| **filter**          | object  | body     | Oggetto JSON che definisce le impostazioni del filtro. Vedere la tabella **schema del filtro** riportata di seguito. |
| **needReCalculate** | boolean | query    | Se impostato su **true**, forza il foglio di calcolo a ricalcolarsi dopo l'aggiunta del filtro. Default: **false**. |
| **folder**          | string  | query    | Cartella nell'archivio cloud in cui si trova il file.                                           |
| **storageName**     | string  | query    | Nome dell'archivio cloud.                                                                       |

**Schema del filtro**

| Proprietà                    | Tipo    | Descrizione                                                                                 |
| ---------------------------- | ------- | ------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | Impostazioni per un filtro automatico; può essere omesso se non utilizzato.                 |
| **EvaluationOrder**          | integer | Ordine in cui viene valutato il filtro.                                                     |
| **FieldIndex**               | integer | Indice in base zero del campo a cui si applica il filtro.                                   |
| **FilterType**               | string  | Tipo di filtro (ad es. `Value`, `Count`, `Label`).                                          |
| **MeasureFldIndex**          | integer | Indice del campo misura, se applicabile.                                                    |
| **MemberPropertyFieldIndex** | integer | Indice del campo proprietà membro, se applicabile.                                          |
| **Name**                     | string  | Nome facoltativo del filtro.                                                                 |
| **Value1**                   | string  | Primo valore utilizzato dal filtro (ad es. limite inferiore per un intervallo).             |
| **Value2**                   | string  | Secondo valore utilizzato dal filtro (ad es. limite superiore per un intervallo).           |
| **CustomFilters**            | array   | Raccolta di oggetti filtro personalizzato (ciascuno con `FilterOperatorType`, `Value1`, `Value2`). |
| **DynamicFilter**            | object  | Impostazioni per un filtro dinamico (ad es. Top10, Bottom10).                               |
| **IconFilter**               | object  | Impostazioni per un filtro basato su icone.                                                 |
| **Top10Filter**              | object  | Impostazioni per un filtro Top10/Bottom10.                                                  |
| **ColorFilter**              | object  | Impostazioni per un filtro basato sul colore.                                               |
| **Visibledropdown**          | boolean | Indica se il menu a discesa del filtro è visibile.                                           |

> **Nota:** Tutti i parametri elencati sopra sono obbligatori, a meno che non siano esplicitamente contrassegnati come facoltativi nella documentazione dell'API.

### Codici di risposta

| Codice | Significato                                  |
| ------ | -------------------------------------------- |
| 200    | Filtro aggiunto correttamente.               |
| 400    | Richiesta non valida – parametri non validi. |
| 401    | Non autorizzato – token mancante o non valido. |
| 404    | Non trovato – foglio di calcolo o tabella pivot mancante. |
| 500    | Errore interno del server.                   |

**Best practice**  
- Mantenere gli oggetti filtro il più piccoli possibile; definizioni di filtri grandi possono aumentare la latenza della richiesta.  
- Le chiamate sono idempotenti: aggiungere lo stesso filtro due volte non crea duplicati.  
- Rispettare il limite di frequenza dell'API: 100 richieste al minuto per account.  

*Note aggiuntive:*  
- La dimensione massima di una definizione di filtro è di 1 MB; payload più grandi verranno rifiutati con un errore 400.  
- Quando si utilizza `needReCalculate=true`, il ricalcolo può aumentare il tempo di risposta per fogli di calcolo di grandi dimensioni.  

Puoi esplorare l'intera definizione OpenAPI qui:  
[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Esempio di richiesta cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK per il cloud

Utilizzare un SDK è il modo più rapido per sviluppare con Aspose.Cells Cloud. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // Inizializza il client API (sostituisci con le tue credenziali)
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // Costruisci l'oggetto filtro
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // Prepara la richiesta
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // Esegui la richiesta
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Stato: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

Per ulteriori operazioni relative alle tabelle pivot, consulta la documentazione relativa ai filtri **Aggiungi**, **Elimina** e **Pulisci**.