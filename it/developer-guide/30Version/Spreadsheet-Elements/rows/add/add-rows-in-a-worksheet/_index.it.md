---
title: "Aggiungi più righe a un foglio di lavoro Excel"
ArticleTitle: "Aggiungi più righe a un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud"
second_title: "Document"
linktype: "docs"
url: /it/rows/add/rows/
keywords: "Aspose.Cells Cloud, inserisci righe, foglio di lavoro Excel, API REST, SDK, aggiungi più righe"
description: "Scopri come utilizzare l'API REST Aspose.Cells Cloud per inserire più righe in un foglio di lavoro Excel. Questa guida copre l'endpoint, i parametri della richiesta, i comandi cURL di esempio e gli esempi di utilizzo degli SDK."
weight: 20
---

Questa API REST aggiunge diverse nuove righe a un foglio di lavoro Excel.

## API PutInsertWorksheetRows

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                                           |
|-----------------|---------|-----------|-----------------------------------------------------------------------|
| name            | string  | path      | Nome del workbook.                                                    |
| sheetName       | string  | path      | Nome del foglio di lavoro.                                            |
| startrow        | integer | query     | Indice della prima riga da inserire (**indicizzazione a 0**).         |
| totalRows       | integer | query     | Numero di righe da inserire.                                          |
| updateReference | boolean | query     | Indica se aggiornare i riferimenti alle celle dopo l'inserimento (`true` o `false`). |
| folder          | string  | query     | Cartella contenente il documento.                                     |
| storageName     | string  | query     | Nome dello storage.                                                   |

**Prerequisiti**  
Il workbook deve già esistere nello storage (o nella cartella) specificato prima di invocare questa operazione.

**Autenticazione**  
L'API richiede un token JWT valido. Includilo nell'intestazione `Authorization`, come mostrato nell'esempio cURL riportato di seguito.

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota:** Questa operazione `PUT` non richiede un corpo della richiesta; è possibile inviare un oggetto JSON vuoto (`{}`) se la libreria client impone un payload.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Codici di risposta possibili*  

- **200 OK** – Righe inserite correttamente.  
- **400 Bad Request** – Parametri non validi (ad esempio, indice di riga negativo).  
- **401 Unauthorized** – Token JWT mancante o non valido.  
- **404 Not Found** – Il workbook o il foglio di lavoro specificato non esiste.  
- **500 Internal Server Error** – Errore imprevisto del server.

{{< /tab >}}

{{< /tabs >}}

Per altre operazioni sulle righe, consulta le pagine correlate: **Elimina righe**, **Ottieni righe** e **Copia righe**.

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il metodo più rapido per lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}