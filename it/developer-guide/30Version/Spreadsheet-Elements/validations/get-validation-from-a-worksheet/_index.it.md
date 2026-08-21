---
title: "Ottenere una convalida del foglio di calcolo per indice da un foglio di calcolo Excel"
second_title: "Document"
linktype: "Get"
type: docs
url: /it/validations/get/
aliases: [  /it/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, API per la convalida del foglio di calcolo, ottenere la convalida per indice, API REST di Excel, Aspose.Cells SDK"
description: "Recuperare una convalida del foglio di calcolo tramite il relativo indice in base zero da un file di lavoro Excel utilizzando l'API Aspose.Cells Cloud (v3.0). Include esempio cURL, schema di risposta, codici di errore e frammenti di codice SDK per C#, Java, Python e altri."
weight: 10
---

Questa API REST recupera una convalida del foglio di calcolo tramite il suo indice da un foglio di calcolo Excel.  
Prima di chiamare l'endpoint, ottieni un token JWT tramite l'endpoint `/connect/token` e includilo nell'header `Authorization` come `Bearer <jwt token>`.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                           |
| --------------- | ------- | --------- | ----------------------------------------------------- |
| name            | string  | path      | Nome del file di lavoro.                              |
| sheetName       | string  | path      | Nome del foglio di calcolo.                           |
| validationIndex | integer | path      | Indice in base zero della convalida da recuperare.    |
| folder          | string  | query     | Cartella contenente il file di lavoro.                |
| storageName     | string  | query     | Nome del servizio di archiviazione.                   |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Schema della risposta**

| Campo          | Tipo    | Descrizione                                                                   |
| -------------- | ------- | ----------------------------------------------------------------------------- |
| AlertStyle     | string  | Stile dell'avviso mostrato all'utente (Stop, Warning, Information).          |
| AreaList       | array   | Collezione di intervalli di celle a cui si applica la convalida.             |
| IgnoreBlank    | boolean | Se `true`, le celle vuote vengono ignorate durante la convalida.             |
| InCellDropDown | boolean | Se `true`, viene visualizzato un elenco a discesa nella cella.               |
| Operator       | string  | Operatore di confronto utilizzato per la convalida (ad esempio, `None`, `Between`). |
| ShowError      | boolean | Determina se mostrare un messaggio di errore in caso di convalida fallita.   |
| ShowInput      | boolean | Determina se mostrare un messaggio di input quando la cella viene selezionata. |
| Type           | string  | Tipo di convalida (ad esempio, `AnyValue`, `WholeNumber`, `Decimal`, ecc.).  |
| link.Href      | string  | URL di riferimento interno alla risorsa di convalida.                        |
| link.Rel       | string  | Tipo di relazione (sempre `self`).                                           |

**Codici di errore possibili**

| Status HTTP | Significato                                                               |
| ----------- | ------------------------------------------------------------------------- |
| 200         | Convalida recuperata correttamente.                                       |
| 400         | Richiesta non valida – parametri mancanti o non validi.                   |
| 401         | Non autorizzato – token JWT non valido o mancante.                        |
| 404         | Non trovato – il file di lavoro, il foglio di calcolo o l'indice della convalida non esistono. |
| 500         | Errore interno del server – condizione imprevista.                        |

## Famiglia di SDK per il cloud

Utilizzare un SDK è il modo più rapido per sviluppare con Aspose.Cells Cloud. Un SDK astrae i dettagli di basso livello, permettendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}

---