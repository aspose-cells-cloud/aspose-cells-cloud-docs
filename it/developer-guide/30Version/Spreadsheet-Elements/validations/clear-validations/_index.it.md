---
title: "Elimina tutte le convalidhe dei fogli di lavoro – Aspose.Cells Cloud API"
second_title: "Documentazione"
linktitle: "Elimina"
type: docs
url: /validations/clear/
keywords: "Aspose.Cells Cloud, elimina convalidhe dei fogli di lavoro, Excel, API REST, convalida spreadsheet, API"
description: "Rimuovi tutte le regole di convalida dei dati da un foglio di lavoro in un file Excel utilizzando l'API REST di Aspose.Cells Cloud. Include fasi di autenticazione, dettagli della richiesta, esempio cURL, schema di risposta, gestione degli errori e frammenti SDK."
weight: 10
---

**Prerequisiti**

- Un account Aspose Cloud valido.
- Un token di accesso JWT ottenuto tramite l'API di autenticazione Aspose Cloud (`/connect/token`).
- Il workbook deve essere archiviato nel tuo spazio di archiviazione Aspose Cloud (oppure devono essere forniti i parametri di query `folder`/`storageName` appropriati).

Questa API REST elimina tutte le convalidhe dei fogli di lavoro da un foglio Excel.

## API REST

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Parametri della richiesta**

| Nome del parametro | Tipo   | Posizione | Descrizione                                             |
| ------------------ | ------ | --------- | ------------------------------------------------------- |
| name               | string | path      | Il nome del documento Excel.                            |
| sheetName          | string | path      | Il nome del foglio di lavoro contenente le convalidhe. |
| folder             | string | query     | La cartella in cui è archiviato il documento.          |
| storageName        | string | query     | Il nome del servizio di archiviazione.                  |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API con cURL dopo aver ottenuto un token JWT.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
  -X DELETE \
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

### Gestione degli errori

| Status HTTP | Significato           | Descrizione                                              |
| ----------- | --------------------- | -------------------------------------------------------- |
| 400         | Richiesta non valida  | La richiesta è malformata o mancano parametri obbligatori. |
| 401         | Non autorizzato       | Il token JWT è mancante, non valido o scaduto.           |
| 404         | Non trovato           | Il workbook o il foglio di lavoro specificato non esiste. |
| 500         | Errore interno del server | Si è verificato un errore imprevisto lato server.         |

Il payload dell'errore segue la stessa struttura JSON con i campi `Code` e `Message`, ad esempio:

```json
{
  "Code": 401,
  "Message": "Token non valido o scaduto."
}
```

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Controlla il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}