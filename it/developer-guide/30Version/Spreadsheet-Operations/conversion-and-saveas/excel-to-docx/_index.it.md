---
title: "Excel in Docx"
second_title: "Documento"
linktype: "Excel to Docx"
type: docs
url: convert-excel-file-to-docx-file/
keywords: "conversione da Excel a Docx, Aspose.Cells Cloud, REST API, conversione di fogli elettronici, generazione di documenti"
description: "Converti fogli elettronici Excel in documenti DOCX utilizzando l'API REST di Aspose.Cells Cloud. Supporta numerosi SDK e linguaggi di programmazione per un'integrazione semplice."
weight: 90
---

Questa API REST converte un file di foglio elettronico in un file in formato DOCX.

## API REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione tramite token JWT</a>.



**Parametri della query**

| Nome parametro        | Tipo   | Descrizione                                                                                          |
| --------------------- | ------ | ---------------------------------------------------------------------------------------------------- |
| password              | string | La password necessaria per aprire il file Excel.                                                     |
| storageName           | string | Il nome dello storage in cui si trova il file.                                                       |
| checkExcelRestriction | bool   | Indica se verificare le restrizioni del file Excel quando l’utente modifica oggetti correlati alle celle. |

**Parametro del corpo della richiesta**

| Nome parametro | Tipo      | Descrizione                                                       |
| -------------- | --------- | ----------------------------------------------------------------- |
| datafile       | data file | Il file di dati salvato nella prima parte del corpo della richiesta multipart. |

**Risposta**

L’API restituisce un oggetto **FileInfo** che contiene il file Word generato.

| Campo           | Tipo   | Descrizione                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Nome del file Word (ad esempio, `esempio.docx`). |
| **FileSize**    | int    | Dimensione del file in byte.                  |
| **FileContent** | string | Contenuto del file Word in base64.            |


[FileInfo](/cells/file-info/)

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione.                           |
| 500  | Errore interno del server   | Errore imprevisto nel server.                                               |
## Come utilizzare l'API PostConvertWorkbookToDocx con gli SDK

### Specifica dell'API PostConvertWorkbookToDocx

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "esempio.docx",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’uso di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Altre API che implementano questa funzione

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Salva un file Excel come file DOCX con impostazioni aggiuntive e memorizza il risultato nello storage specificato.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converte un file Excel in un file DOCX con impostazioni opzionali e restituisce il risultato nella risposta.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Recupera un workbook Excel e lo converte in un file DOCX con parametri opzionali.

---