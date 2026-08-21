---
title: "Salva il Workbook di Excel – Aspose.Cells Cloud API"
secondo titolo: "Document"
linktitle: "Salva come"
type: docs
url: /save-an-excel-file-as-other-formats-files/
alias:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, Salva come, PDF, CSV, JSON, Markdown, REST API"
description: "Salva i workbook di Excel in PDF, CSV, JSON, Markdown e altri formati utilizzando l'API REST di Aspose.Cells Cloud."
weight: 30
---

Questa API REST consente di **salvare** un file Excel in diversi formati.  
Prima di chiamare questo endpoint, assicurati di avere un token di accesso OAuth 2.0 valido e che il workbook di origine sia memorizzato nella tua archiviazione Aspose Cloud.

**Prerequisiti**  
1. Ottieni un token di accesso JWT e includilo nell'intestazione `Authorization: Bearer <token>` di ogni richiesta.  
2. Carica il workbook di origine nell'archiviazione Aspose Cloud (oppure conferma che esista già).  
3. Conosci il nome dell'archiviazione e il percorso della cartella in cui si trova il workbook.

## API PostWorkbookSaveAs

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametro del percorso**

| Nome parametro | Tipo   | Descrizione                        |
| -------------- | ------ | ---------------------------------- |
| name           | string | Nome del file Excel.               |

### **Parametro di query**

| Nome parametro        | Tipo   | Descrizione                                                                                     |
| --------------------- | ------ | ----------------------------------------------------------------------------------------------- |
| newfilename           | string | Nuovo nome del file da salvare.                                                                |
| isAutoFitRows         | string | Se `true`, ridimensiona automaticamente tutte le righe nel workbook. Il valore predefinito è `false`. |
| isAutoFitColumns      | string | Se `true`, ridimensiona automaticamente le larghezze delle colonne nel workbook. Il valore predefinito è `false`. |
| folder                | string | Cartella contenente il workbook originale.                                                     |
| storageName           | string | Nome dell'archiviazione in cui si trova il file di origine.                                    |
| outStorageName        | string | Nome dell'archiviazione in cui verrà salvato il file di output.                                |
| checkExcelRestriction | bool   | Specifica se applicare le restrizioni di Excel durante la modifica di celle o oggetti correlati. |
| region                | string | Impostazioni regionali applicate al workbook.                                                  |
| pageWideFitOnPerSheet | bool   | Adatta la larghezza della pagina a ciascun foglio di calcolo durante la conversione.           |
| pageTallFitOnPerSheet | bool   | Adatta l'altezza della pagina a ciascun foglio di calcolo durante la conversione.             |
| sheetName             | string | Nome del foglio di calcolo da convertire.                                                      |
| pageIndex             | string | Indice della pagina da convertire all'interno del foglio specificato (richiede `sheetName`).    |
| onePagePerSheet       | bool   | Durante la conversione in PDF, genera una pagina per ciascun foglio di calcolo.                |

### **Parametro del corpo della richiesta**

| Nome parametro | Tipo   | Descrizione                                                    |
| -------------- | ------ | -------------------------------------------------------------- |
| SaveOptions    | Object | Opzioni di salvataggio fornite nella seconda parte della richiesta multipart. |

**Esempio di corpo della richiesta (parte JSON della richiesta multipart)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Risposta

L'API restituisce un oggetto `SaveResponse`.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                             |
|--------|-----------------------------|-------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                        |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                       |
| 500    | Errore interno del server   | Errore imprevisto del server.                                           |

## Come usare l'API PostWorkbookSaveAs con gli SDK

### Specifica dell'API PostWorkbookSaveAs

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello in modo che tu possa concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

Per altri scenari di conversione, consulta le guide [Converti Excel in PDF](/convert-excel-to-pdf/) e [Esporta Excel in CSV](/export-excel-to-csv/).