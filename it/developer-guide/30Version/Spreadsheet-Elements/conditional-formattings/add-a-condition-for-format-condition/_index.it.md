---
---
title: Aggiungi una condizione alla formattazione condizionale
description: Scopri come aggiungere una condizione alla formattazione condizionale di un foglio di lavoro utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, autenticazione, esempio cURL, frammenti SDK e gestione degli errori.
keywords: "Aspose.Cells Cloud, formattazione condizionale, aggiungi condizione, API REST, Excel, foglio di lavoro"
type: docs
url: /conditional-formattings/add-a-condition/it/
aliases:
  - /add-a-condition-for-format-condition/it/
weight: 40
---

# Aggiungi una condizione alla formattazione condizionale

Aggiungi una condizione a una regola esistente di formattazione condizionale in un foglio di lavoro utilizzando l'API REST di Aspose.Cells Cloud (v3.0).

---

## Prerequisiti

| Requisito | Dettagli |
|-----------|----------|
| **Autenticazione** | Un token di accesso JWT valido (Bearer) ottenuto tramite il flusso OAuth 2.0. |
| **Versione API** | v3.0 – l'URL dell'endpoint contiene `/v3.0/`. |
| **Archiviazione** | Il workbook deve trovarsi in una posizione di archiviazione accessibile a Aspose.Cells Cloud (quella predefinita è `Default`). |
| **Permessi** | Permessi di lettura/scrittura sul workbook di destinazione. |
| **Formati supportati** | Qualsiasi formato di workbook supportato da Aspose.Cells (ad esempio `.xlsx`, `.xls`, `.xlsm`). |

---

## Endpoint

**Metodo HTTP:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Parametro | Posizione | Tipo | Obbligatorio | Descrizione |
|-----------|-----------|------|--------------|-------------|
| `name` | Path | string | **Sì** | Nome del file del workbook (inclusa l'estensione). |
| `sheetName` | Path | string | **Sì** | Nome del foglio di lavoro contenente la formattazione condizionale. |
| `index` | Path | integer | **Sì** | Indice in base zero della raccolta di formattazione condizionale da modificare. |
| `type` | Query | string | **Sì** | Tipo di condizione. Valori ammessi: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Query | string | **Sì** | Operatore per la condizione. Valori ammessi: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Query | string | **Sì** | Prima formula/valore associato alla condizione. |
| `formula2` | Query | string | No | Seconda formula/valore (richiesto solo per operatori che ne richiedono due, ad esempio `Between`). |
| `folder` | Query | string | No | Cartella in archiviazione dove si trova il workbook. |
| `storageName` | Query | string | No | Nome del servizio di archiviazione. |

> **Nota:** Tutti i parametri di percorso (`name`, `sheetName`, `index`) e i parametri di query `type`, `operatorType`, `formula1` sono obbligatori. `formula2`, `folder` e `storageName` sono facoltativi.

---

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*Sostituisci `<jwt_token>` con un token di accesso valido e regola `name`, `sheetName`, `index` e i valori di query secondo le tue esigenze.*

---

## Risposta in caso di successo

```json
{
  "Code": "200",
  "Status": "OK"
}
```

La risposta indica che la condizione è stata aggiunta correttamente. L'operazione restituisce un oggetto generico `CellsCloudResponse` contenente il codice di stato HTTP e un breve messaggio di stato.

---

## Risposte di errore

| Codice HTTP | Motivo | Esempio di corpo |
|-------------|--------|------------------|
| **400** | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore di parametro non valido." }` |
| **401** | Non autorizzato – token JWT mancante o non valido. | `{ "Code":"401", "Message":"Token di accesso mancante o non valido." }` |
| **404** | Non trovato – workbook, foglio di lavoro o indice di formattazione condizionale non esistenti. | `{ "Code":"404", "Message":"File non trovato." }` |
| **500** | Errore interno del server – guasto imprevisto del server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

---

## Note e criticità comuni

* **Codifica dei parametri** – Codifica in URL i caratteri speciali in `formula1`/`formula2` (ad esempio, gli spazi → `%20`).  
* **Compatibilità dell'operatore** – Alcuni operatori (ad esempio `Between`) richiedono sia `formula1` che `formula2`. Ometti `formula2` per operatori che richiedono un solo valore.  
* **Indice della formattazione condizionale** – L'indice è in base zero. Utilizza l'endpoint **Get Conditional Formattings** per recuperare l'indice corretto in caso di incertezze.  
* **Cartella di archiviazione** – Se il workbook si trova in una cartella diversa da quella predefinita, fornisci il parametro di query `folder`; altrimenti l'API assume la cartella radice.  
* **Limitazione della velocità** – Aspose.Cells Cloud applica limiti di richieste per account. Se ricevi una risposta 429, riduci la frequenza delle richieste e riprova dopo un breve intervallo.

---

## Esempi di SDK

Di seguito sono riportati frammenti pronti all'uso per gli SDK più diffusi. Sostituisci i valori segnaposto (`YOUR_FILE`, `YOUR_SHEET`, ecc.) con i tuoi dati.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // opzionale
        string storageName = null;     // opzionale

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Eccezione durante la chiamata a ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Risposta: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Stato:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Stato: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Eccezione durante la chiamata a ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Stato: " . $result->{status} . "\n";
};
if ($@) {
    warn "Eccezione durante la chiamata a ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Errore: %v\n", err)
        return
    }
    fmt.Printf("Stato: %s\n", resp.Status)
}
```

> **SDK mancanti** – Se il linguaggio necessario non è elencato, consulta la **documentazione di riferimento API** generica e costruisci manualmente la richiesta HTTP.

---

## Vedi anche

- **[Get Conditional Formattings](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – Recupera l'elenco delle regole di formattazione condizionale per un foglio di lavoro.  
- **[Delete Conditional Formatting](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – Rimuove una regola esistente di formattazione condizionale.  
- **[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – Definizione completa, leggibile da macchina, di questa operazione.  

---
---