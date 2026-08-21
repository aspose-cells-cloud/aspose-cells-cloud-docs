---
title: "Converti Excel in Markdown"
second_title: "Documenti"
linktitle: "Excel in Markdown"
type: docs
url: /convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, conversione, Aspose.Cells Cloud, REST API, conversione da Excel a Markdown, API Markdown di Aspose Cells, esportazione Excel in Markdown"
description: "Converti fogli di lavoro Excel in Markdown usando l'API REST di Aspose.Cells Cloud – include esempio cURL, frammenti di codice SDK, parametri obbligatori e dettagli sull'autenticazione."
weight: 100
ArticleTitle: "Converti Excel in Markdown – Documentazione API Aspose.Cells Cloud"
---

Questa API REST converte un file di foglio di calcolo in un file in formato Markdown.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della query


| Nome parametro        | Tipo   | Posizione | Descrizione                                                                                       |
| --------------------- | ------ | --------- | ------------------------------------------------------------------------------------------------- |
| password              | string | query     | Password richiesta per aprire il file Excel.                                                      |
| storageName           | string | query     | Nome dello storage in cui si trova il file.                                                       |
| checkExcelRestriction | bool   | query     | Indica se applicare restrizioni specifiche di Excel quando si modificano celle o oggetti correlati. |
| datafile              | file   | body      | Il file Excel da caricare come prima parte del contenuto multipart.                               |

### Risposta

L'API restituisce un oggetto JSON di tipo **FileInfo**:

- **FileInfo** – oggetto contenente il nome, le dimensioni e il contenuto codificato in base64 del file Markdown generato.

```json
{
  "Filename": "esempio.md",
  "FileSize": 12345,
  "FileContent": "stringa_in_base64"
}
```

### Risposte di errore

| Codice HTTP | Descrizione                                                       | Corpo JSON di esempio                           |
| ----------- | ----------------------------------------------------------------- | ----------------------------------------------- |
| 401         | Non autorizzato – token mancante o non valido.                    | `{"error":"Token di accesso non valido."}`      |
| 400         | Richiesta non valida – parametri obbligatori mancanti o formato file non valido. | `{"error":"Il campo 'datafile' è obbligatorio."}` |
| 500         | Errore interno del server – problema imprevisto nel server.       | `{"error":"Si è verificato un errore imprevisto."}` |



## Come usare l'API PostConvertWorkbookToMarkdown con gli SDK

### Specifica dell'API PostConvertWorkbookToMarkdown

La [Specifica OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@tuo_file_excel.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "esempio.md",
  "FileSize": 12345,
  "FileContent": "stringa_in_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'uso di un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Altre API che implementano questa funzionalità

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Salva un file Excel come HTML con impostazioni aggiuntive e memorizza il risultato.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converte un file Excel in HTML con opzioni aggiuntive e restituisce il risultato nella risposta.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un file Excel e può convertirlo in HTML con impostazioni opzionali.
---