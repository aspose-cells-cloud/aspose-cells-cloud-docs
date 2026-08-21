---
title: "Conversione Avanzata di File Excel"
second_title: "Documenti"
linktype: "Conversione Avanzata"
type: docs
url: /it/advanced-convert-excel/
keywords: "Aspose.Cells, conversione Excel, API cloud, SDK"
description: "L'API REST Aspose.Cells Cloud offre potenti funzionalità per convertire cartelle di lavoro Excel in una vasta gamma di formati, configurare l'impostazione della pagina, le opzioni di salvataggio e le impostazioni di stampa. Gli SDK sono disponibili per Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift, consentendo un'integrazione semplice su molteplici piattaforme."
weight: 50
ArticleTitle: "Conversione Avanzata di File Excel – Guida all'API Aspose.Cells Cloud"
---

## API Cloud Avanzata per la Conversione Excel

L'operazione di Conversione Avanzata consente di trasformare una cartella di lavoro Excel in vari formati di output (PDF, HTML, CSV, ecc.), offrendo un controllo dettagliato sull'impostazione della pagina, sulle opzioni di salvataggio e sulle impostazioni di stampa.

**Prerequisiti / Autenticazione**  
Per utilizzare questo endpoint è necessario ottenere un token di accesso da Aspose.Cells Cloud e includeerlo nell'intestazione `Authorization` come token Bearer.

**Riferimento API**  
- **Metodo:** `PUT`  
- **Endpoint:** `/cells/convert`  
- **Parametri:**  
  - `format` (stringa, obbligatorio) – Format di output desiderato (ad esempio, `pdf`, `html`).  
  - `outPath` (stringa, facoltativo) – Percorso nello storage cloud in cui verrà salvato il file convertito.  
  - `options` (oggetto, facoltativo) – Oggetto JSON contenente opzioni avanzate di conversione come `pageSetup`, `saveOptions` e `printSettings`.  
- **Esempio di corpo della richiesta:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Risposta:**  
  - `200 OK` – Conversione riuscita; la risposta contiene il flusso del file convertito o un riferimento al file salvato.  
  - `400 Bad Request` – Parametri non validi o corpo della richiesta malformato.  
  - `401 Unauthorized` – Autenticazione non riuscita o token mancante.  
  - `500 Internal Server Error` – Errore lato server durante la conversione.  

**Codici di Stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtraggio applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Bad Request                 | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Unauthorized                | Token JWT non valido o mancante. |
| 413    | Payload Too Large           | Il file caricato supera il limite di dimensione. |
| 500    | Internal Server Error       | Errore imprevisto del server. |

**Note**  
* Alcuni formati di output presentano limitazioni specifiche (ad esempio, la conversione in HTML non preserva le macro). Consultare la documentazione specifica per ogni formato per ulteriori dettagli.

### La capacità di caricare file di fogli elettronici da diverse fonti di dati

### Impostazione della Pagina e Opzioni di Salvataggio

## Famiglia di SDK Cloud

L'utilizzo di un SDK accelera lo sviluppo gestendo i dettagli a basso livello, permettendoti di concentrarti sulle attività del tuo progetto.Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Conversione Avanzata",
  "description":"Converti una cartella di lavoro Excel in PDF/HTML/CSV con opzioni avanzate.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"Formato di output desiderato (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>