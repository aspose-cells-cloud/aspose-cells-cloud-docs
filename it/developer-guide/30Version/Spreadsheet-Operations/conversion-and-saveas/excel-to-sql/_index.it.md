---
title: "Excel in SQL"
second_title: "Documento"
linktitle: "Excel in SQL"
type: docs
url: /convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel in SQL, API cloud, conversion foglio elettronico, REST"
description: "Utilizza l'API REST Aspose.Cells Cloud per convertire fogli di calcolo Excel in file SQL. Supporta numerosi SDK e linguaggi di programmazione per un'integrazione fluida nelle tue applicazioni."
weight: 100
ArticleTitle: "Converti Excel in SQL – Aspose.Cells Cloud API"
---

Questa API REST converte un file di foglio elettronico in un file in formato SQL.

**Prerequisiti**  
Per utilizzare questo endpoint devi disporre di un token JWT valido generato come descritto nella guida <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>. L'API supporta file Excel entro i limiti di dimensione definiti nella documentazione del servizio e può gestire cartelle di lavoro protette da password qualora il parametro di query `password` venga fornito.

## API PostConvertWorkbookToSQL

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Sicurezza e autenticazione**

Le API REST Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametro di query**

| Nome parametro        | Tipo   | Descrizione                                                                                       |
| --------------------- | ------ | ------------------------------------------------------------------------------------------------- |
| password              | string | Password necessaria per aprire il file Excel.                                                    |
| storageName           | string | Nome dell'archiviazione in cui il file è conservato.                                              |
| checkExcelRestriction | bool   | Indica se verificare le limitazioni dei file Excel quando si modificano oggetti legati alle celle. |

### **Parametro del corpo della richiesta**

| Nome parametro | Tipo      | Descrizione                                                                     |
| -------------- | --------- | ------------------------------------------------------------------------------- |
| datafile       | file dati | Il file di foglio elettronico da convertire, incluso come prima parte della richiesta. |

### Risposta

L'API restituisce un oggetto **FileInfo** che contiene il file SQL generato.

| Campo           | Tipo   | Descrizione                                          |
| --------------- | ------ | ---------------------------------------------------- |
| **Filename**    | string | Nome del file SQL (ad esempio, `esempio.sql`).      |
| **FileSize**    | int    | Dimensione del file in byte.                         |
| **FileContent** | string | Contenuto del file SQL in formato Base64.            |

[FileInfo](/cells/file-info/)

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                              |
| ------ | --------------------------- | ------------------------------------------------------------------------ |
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante.                                         |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione.                        |
| 500  | Errore interno del server   | Errore imprevisto nel server.                                            |

## Come utilizzare l'API PostConvertWorkbookToSQL con gli SDK

### Specifica dell'API PostConvertWorkbookToSQL

La <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "esempio.sql",
  "FileSize": 1024,
  "FileContent": "stringa_in_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Altre API che implementano questa funzionalità

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Salva una cartella di lavoro in un formato differente e memorizza il risultato nell'archiviazione specificata.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converte una cartella di lavoro in un altro formato con impostazioni opzionali e restituisce il risultato nella risposta.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera una cartella di lavoro con impostazioni di conversione opzionali.

**Note**  
- Durante la conversione di file Excel protetti da password, assicurati di fornire il parametro di query `password`; altrimenti la conversione fallirà con un errore 400.  
- Il servizio restituisce il contenuto del file SQL in formato Base64: decodificalo prima di salvarlo in un file `.sql`.  

**File di esempio**  
Scarica una cartella di lavoro Excel di esempio [qui](https://example.com/sample.xlsx) e un risultato SQL già generato [qui](https://example.com/sample.sql) per testare rapidamente l'API.