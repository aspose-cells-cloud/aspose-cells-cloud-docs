---
title: "Aspose.Cells Cloud – Convertire il Workbook Excel in PDF, CSV, HTML e Altro (GET /cells/{name})"
second_title: "Documento"
linktitle: "Converti Excel"
type: docs
url: /it/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, conversione Excel, convertire Excel, PDF, CSV, HTML, ODS, JSON, formati immagine, esportazione foglio di calcolo, API, REST"
description: "Scopri come recuperare un workbook Excel in qualsiasi formato (PDF, CSV, HTML, PNG, ecc.) utilizzando l'API REST di Aspose.Cells Cloud. Include esempi cURL, SDK, autenticazione e dettagli sulla risposta."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Convertire il Workbook Excel in PDF, CSV, HTML e Altro (GET /cells/{name})"
---

Questa API REST recupera un workbook Excel in un formato diverso.

## API GetWorkBook

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della query**

| Nome parametro        | Tipo   | Descrizione                                                                                                                                                                          | Valore predefinito |
| --------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------ |
| format                | string | Format del file di destinazione (ad esempio, CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, ecc.). | –                  |
| password              | string | Password necessaria per aprire il file Excel.                                                                                                                                       | –                  |
| isAutoFit             | bool   | Adatta automaticamente la larghezza di righe e colonne.                                                                                                                             | false              |
| onlySaveTable         | bool   | Se **true**, vengono salvati solo i dati della tabella. Accetta `true` o `false`.                                                                                                   | false              |
| outPath               | string | Percorso in cui salvare il risultato. Per un singolo file, includere nome file ed estensione; per più file, specificare solo la cartella.                                            | –                  |
| outStorageName        | string | Nome dello storage in cui verrà salvato il file di output.                                                                                                                          | –                  |
| checkExcelRestriction | bool   | Verifica le restrizioni di Excel durante la modifica di celle o oggetti correlati.                                                                                                  | false              |
| region                | string | Impostazioni regionali applicate al workbook.                                                                                                                                       | –                  |
| pageWideFitOnPerSheet | bool   | Adatta la larghezza della pagina a ciascun foglio di calcolo durante la conversione in PDF.                                                                                        | false              |
| pageTallFitOnPerSheet | bool   | Adatta l'altezza della pagina a ciascun foglio di calcolo durante la conversione in PDF.                                                                                           | false              |
| onePagePerSheet       | bool   | Genera una pagina PDF per ciascun foglio di calcolo.                                                                                                                                | false              |
| folder                | string | Percorso della cartella del workbook originale.                                                                                                                                     | –                  |
| storageName           | string | Nome dello storage in cui si trova il file di origine.                                                                                                                              | –                  |

### Risposta

**Successo (200)**

- L’API restituisce un oggetto **[Workbook](/cells/workbook/)** contenente informazioni sulla struttura del workbook quando il parametro di query `format` è omesso.

- L’API restituisce il file convertito nel formato richiesto quando il parametro di query `format` specifica un tipo di file.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(dati binari PDF)
```

**Codici di stato HTTP**

| Codice | Significato                  | Descrizione                                             |
|--------|------------------------------|---------------------------------------------------------|
| 200    | OK                           | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida         | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato              | Token JWT non valido o mancante.                        |
| 413    | Payload troppo grande        | Il file caricato supera il limite di dimensione.       |
| 500    | Errore interno del server    | Errore imprevisto nel server.                           |

> **Note:**  
> - Workbook di grandi dimensioni potrebbero richiedere più tempo per essere convertiti; considerare l’aumento del timeout della richiesta.  
> - Alcuni formati (ad esempio, `ODS`) non sono supportati per determinate funzionalità di Excel, come le macro.

## Come utilizzare l’API GetWorkBook con gli SDK

> **Prerequisiti:**  
> - Un **token di accesso JWT** valido ottenuto tramite il flusso di autenticazione di Aspose.Cells.  
> - Il workbook di origine deve essere archiviato in uno storage supportato da Aspose o fornito direttamente nella richiesta.  
> - Assicurarsi che la versione dell’API (`v3.0`) corrisponda all’ultima versione rilasciata.

### Specifica dell’API GetWorkBook

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un’interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

### Esempio di richiesta

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere ai servizi web di Aspose.Cells. L’esempio seguente mostra una richiesta GET corretta con l’header di autorizzazione obbligatorio.

{{< tabs tabTotal="1" tabID="11" tabName11="Richiesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK rappresenta il metodo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per l’elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Vedi anche**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Converti Workbook (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Salva come (GET)</a>

---

_Ultimo aggiornamento: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Convertire il Workbook Excel in PDF, CSV, HTML e Altro (GET /cells/{name})",
  "description": "Documentazione per l’endpoint GET /cells/{name} di Aspose.Cells Cloud che converte i workbook Excel in vari formati come PDF, CSV, HTML e altri.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, conversione Excel, PDF, CSV, HTML, API, REST, cloud",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---