---
title: "Converti Excel in PDF – Aspose.Cells Cloud API"
ArticleTitle: "Converti Excel in PDF – Aspose.Cells Cloud API"
second_title: "Documenti"
linktitle: "Converti Excel in PDF"
type: docs
url: /it/convert-excel-file-to-pdf-file/
aliases: [/it/convert-excel-file-to-pdf-in-cloud/, /it/convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, conversione, API cloud"
description: "Scopri come convertire file di cartelle di lavoro Excel in PDF tramite l'API REST Aspose.Cells Cloud. Include esempi in cURL, SDK (C#, Java, Python) e una guida all'autenticazione."
weight: 80
---

Questa API REST converte un file di foglio elettronico in un file in formato PDF. **Prerequisiti:** ottenere un token di accesso JWT valido, assicurarsi che il file Excel di origine sia memorizzato in uno storage supportato e disporre delle autorizzazioni appropriate per richiamare l'endpoint di conversione.

## API PostConvertWorkbookToPDF

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'**[autenticazione tramite token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)**.

### **Parametro di query**

| Nome parametro        | Tipo   | Descrizione                                                                     |
| :-------------------- | :----- | :------------------------------------------------------------------------------ |
| password              | string | Password per aprire il file Excel.                                              |
| storageName           | string | Nome dello storage in cui è posizionato il file.                                |
| checkExcelRestriction | bool   | Indica se applicare le restrizioni sui file Excel quando si modificano oggetti correlati alle celle. |

Se omesso, `checkExcelRestriction` assume valore `false` per impostazione predefinita.

### **Parametro nel corpo della richiesta**

| Nome parametro | Tipo | Descrizione                                                     |
| :------------- | :--- | :-------------------------------------------------------------- |
| datafile       | file | File di dati salvato come prima parte del contenuto multipart. |

### **Risposta**

[FileInfo](/it/cells/file-info/)

La risposta restituisce un oggetto JSON contenente i metadati del file. Il file PDF può essere scaricato tramite il campo `FileContent` (in base64) oppure seguendo il link fornito in `FileInfo`. L’API restituisce un oggetto JSON di tipo **FileInfo**:

- **FileInfo** – oggetto contenente il nome, la dimensione e il contenuto in base64 del file **PDF** generato.

```json
{
  "Filename": "esempio.pdf",
  "FileSize": 12345,
  "FileContent": "stringa_in_base64"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                            |
|--------|-----------------------------|------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                       |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                       |
| 500    | Errore interno del server   | Errore imprevisto nel server.                                          |

## Come utilizzare l’API PostConvertWorkbookToPDF con gli SDK

### Specifica dell’API PostConvertWorkbookToPDF

La [Specifica OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare direttamente interazioni REST da un browser web.

**Intestazioni della richiesta**

| Intestazione  | Tipo   | Descrizione                                           |
| :------------ | :----- | :---------------------------------------------------- |
| Authorization | string | Token Bearer ottenuto tramite autenticazione JWT.    |
| Content-Type  | string | Deve essere `multipart/form-data` per il caricamento dei file. |
| Accept        | string | `application/json` per ricevere i metadati della risposta. |

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. Includi un token di accesso nell'intestazione `Authorization` ed esegui la richiesta riportata di seguito.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "Contenuto file: stringa_in_base64"
}
```

{{< /tab >}}

{{< /tabs >}}


### Utilizzo degli SDK Aspose.Cells Cloud

L'utilizzo di un SDK semplifica lo sviluppo gestendo automaticamente i dettagli di basso livello. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Altre API che implementano questa funzionalità

| **API**        | **Tipo** | **Descrizione**                                                       | **Link Swagger**                                                                            |
| :------------- | :------- | :-------------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT      | Converte una cartella di lavoro dal contenuto della richiesta in un formato specificato. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

L’API [POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) consente di salvare un file MS Excel come PDF con impostazioni aggiuntive e memorizzare il risultato nello storage.

Questa API REST converte un file Excel in PDF.

L’API [PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) consente di convertire un file MS Excel in PDF con impostazioni aggiuntive e restituire il risultato nella risposta.

L’API [GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) consente di convertire un file MS Excel in PDF con impostazioni aggiuntive e restituire il risultato nella risposta.

Queste API [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) e [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) definiscono un’interfaccia di programmazione pubblicamente accessibile e consentono di effettuare direttamente interazioni REST da un browser web.

Per ulteriori opzioni di conversione, consulta la pagina [Opzioni di salvataggio](/it/save-options/).