---
title: "Rendi visibile un foglio di Excel"
second_title: "Documento"
linktitle: "Rendi visibile"
type: docs
url: /it/worksheets/unhide/
aliases: [  /it/unhide-excel-worksheets/ ]
keywords: "Aspose.Cells, rendi visibile foglio, Excel API, foglio di calcolo cloud, REST, visibilità foglio, cartella di lavoro Excel"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per rendere visibile un foglio in una cartella di lavoro Excel. Include dettagli della richiesta, esempi cURL e frammenti di codice SDK per diversi linguaggi di programmazione."
weight: 60
---

Questa API REST fornisce un endpoint per **rendere visibile un foglio** in una cartella di lavoro Excel.

**Prerequisiti**  
Prima di chiamare questa operazione, è necessario disporre di:

* Un token di accesso Aspose Cloud (JWT) valido incluso nell'header `Authorization`.  
* La cartella di lavoro memorizzata in una posizione di archiviazione supportata specificata tramite i parametri di query `folder` e `storageName`.  
* La cartella di lavoro deve essere in un formato supportato da Aspose.Cells (ad esempio, `.xls`, `.xlsx`, `.xlsm`).  

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                              |
| -------------- | ------- | --------- | ---------------------------------------- |
| name           | string  | path      | Nome del documento.                      |
| sheetName      | string  | path      | Nome del foglio di lavoro.               |
| isVisible      | boolean | query     | Nuovo valore di visibilità del foglio (`true`). |
| folder         | string  | query     | Cartella del documento.                  |
| storageName    | string  | query     | Nome dell'archiviazione.                 |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) definisce un'interfaccia di programmazione accessibile pubblicamente che consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per chiamare facilmente i servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una richiesta con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # sostituisci <jwt token> con il tuo token di accesso
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di risposta possibili**

| Codice HTTP | Significato                                           | Corpo di esempio (quando applicabile)                          |
|-------------|-------------------------------------------------------|----------------------------------------------------------------|
| 200         | Visibilità del foglio aggiornata con successo         | `{ "Code": 200, "Status": "OK" }`                              |
| 400         | Richiesta non valida – parametri mancanti o non validi | `{ "Code": 400, "Message": "Parametri della richiesta non validi." }` |
| 401         | Non autorizzato – token JWT mancante o non valido     | `{ "Code": 401, "Message": "Autenticazione non riuscita." }`   |
| 404         | Non trovato – cartella di lavoro o foglio inesistente | `{ "Code": 404, "Message": "File o foglio non trovato." }`     |
| 500         | Errore interno del server                             | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}
---