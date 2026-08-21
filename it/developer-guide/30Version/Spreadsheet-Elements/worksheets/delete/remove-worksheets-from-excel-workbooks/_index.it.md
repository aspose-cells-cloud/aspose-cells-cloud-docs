---
title: "Elimina Foglio di Lavoro"
second_title: "Documenti"
linktype: "Un foglio di lavoro"
type: docs
url: /worksheets/delete-worksheet/
aliases: [/remove-worksheets-from-excel-workbooks/]
keywords: "Aspose.Cells Cloud, Elimina Foglio di Lavoro, Excel, Foglio di Calcolo, REST API"
description: "Elimina un foglio di lavoro da un file Excel utilizzando l'API REST di Aspose.Cells Cloud. Supporta SDK per C#, Java, PHP, Ruby, Node.js, Python, Perl, Go e cURL."
weight: 20
ArticleTitle: "Elimina Foglio di Lavoro – Aspose.Cells Cloud API"
---

Questa REST API consente di eliminare un foglio di lavoro.  
Prerequisiti: per chiamare questa API devi fornire un token di autenticazione JWT valido nell'intestazione **Authorization** e avere accesso alla posizione di archiviazione in cui si trova il file Excel.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*Nota: L'API utilizza la versione **v3.0**, che è l'attuale versione stabile. Eventuali cambiamenti di versione futuri saranno comunicati nelle note di rilascio.*

### **Parametri della richiesta**

| Nome Parametro | Tipo   | Posizione | Descrizione              |
| -------------- | ------ | --------- | ------------------------ |
| name           | string | path      | Nome del documento.      |
| sheetName      | string | path      | Nome del foglio di lavoro. |
| folder         | string | query     | Cartella del documento.  |
| storageName    | string | query     | Nome dell'archivio.      |

Possibili risposte HTTP:

| Codice Stato | Descrizione                                      |
| ----------- | ------------------------------------------------ |
| 200 OK      | Foglio di lavoro eliminato con successo.        |
| 400 Bad Request | Parametri della richiesta non validi.         |
| 401 Unauthorized | Autenticazione non riuscita o token mancante. |
| 404 Not Found | Il file Excel o il foglio di lavoro specificato non esiste. |
| 500 Internal Server Error | Errore imprevisto del server.           |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Tutte le richieste devono essere effettuate tramite HTTPS; l'API non supporta connessioni non TLS.*

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

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}