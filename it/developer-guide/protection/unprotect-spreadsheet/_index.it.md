---
title: "Aspose.Cells Cloud Excel Unprotect Web API – Rimuovi password di apertura e modifica in modo programmatico"
second_title: "Documento"
ArticleTitle: "Rimuovi protezione password Excel – Sblocca password di apertura e modifica istantaneamente"
linktitle: "Rimuovi protezione foglio di calcolo"
type: docs
url: /it/unprotect-spreadsheet/
keywords: "rimuovi protezione, foglio di calcolo, Aspose.Cells, API, Excel, rimozione password"
description: "Rimuovi password di apertura e modifica dai file Excel in modo programmatico con l'API Aspose.Cells Cloud Unprotect Spreadsheet. Supporta .xlsx/.xls, autenticazione OAuth2 e elaborazione in batch."
weight: 100
---

L'API Unprotect Spreadsheet rimuove la protezione tramite password di apertura e modifica dai file Excel in una singola chiamata. È ideale per pipeline di dati, sistemi di gestione documentale e flussi di lavoro di migrazione.

## **API Unprotect Spreadsheet**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                                                          |
| -------------- | ------ | --------- | ------------------------------------------------------------------------------------ |
| Spreadsheet    | File   | FormData  | Il file Excel da sproteggere.                                                        |
| password       | String | Query     | La password che protegge il file contro l'apertura.                                  |
| modifyPassword | String | Query     | La password richiesta per modificare il file (opzionale se è impostata solo la password di apertura). |
| outPath        | String | Query     | (Opzionale) Percorso della cartella in cui verrà salvato il workbook sproteggiato.  |
| outStorageName | String | Query     | (Opzionale) Nome dello storage in cui verrà scritto il file di output.              |
| region         | String | Query     | (Opzionale) Impostazioni della regione del foglio di calcolo.                       |

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Una risposta positiva restituisce il file sproteggiato come stream. Il file può essere salvato nella posizione specificata da `outPath`/`outStorageName` o recuperato direttamente dal payload della risposta.

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                      |
| ------ | ----------------------- | ---------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                 |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                |
| 500    | Errore interno del server | Errore imprevisto sul server.                                    |

## Quando utilizzare l'API Unprotect Spreadsheet?

- **Ripristinare l'accesso ai workbook protetti** – Rimuovi rapidamente le password di apertura o modifica dimenticate senza intervento manuale.
- **Automatizzare lo sblocco in blocco** – Elabora un gran numero di file in progetti di migrazione dati o archiviazione.
- **Integrare con flussi di lavoro esistenti** – Combina con API di storage o conversione per creare pipeline end-to-end (ad esempio, caricamento → rimozione protezione → conversione in PDF).
- **Mantenere la sicurezza dei dati** – L'operazione avviene lato server, mantenendo i file originali sicuri mentre la versione sproteggiata viene archiviata nel tuo storage cloud.

## Come utilizzare l'API Unprotect Spreadsheet con gli SDK

### **Specifica OpenAPI**

La [Specifica API UnProtect Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) fornisce un'interfaccia di programmazione accessibile pubblicamente per facilitare interazioni REST dirette da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=VecchiaPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Utilizzare gli SDK Aspose.Cells Cloud**

L'utilizzo di un SDK semplifica la chiamata gestendo l'autenticazione, la costruzione della richiesta e l'analisi della risposta. Gli SDK sono disponibili per molte linguaggi e includono metodi già pronti per la rimozione della protezione dai fogli di calcolo.

I seguenti esempi di codice illustrano come chiamare l'API Unprotect Spreadsheet utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}