---
title: "Aspose.Cells Cloud API – Converti grafico Excel in PDF"
second_title: "Documento"
ArticleTitle: "Come convertire un grafico di un foglio di calcolo locale in un file PDF: Guida passo-passo"
linktitle: "Converti grafico in PDF"
type: docs
url: /it/convert-chart-to-pdf/
keywords: "Aspose Cells, grafico, PDF, Excel, conversione, API cloud"
description: "Esporta grafici da file Excel locali nel formato PDF utilizzando l'API REST di Aspose.Cells Cloud. Supporta i file XLSX e XLS."
weight: 100
---

Esporta grafici da un file Excel locale nel formato [PDF](https://docs.fileformat.com/pdf/) utilizzando l'API Cloud.

## **Converti grafico in PDF – API Web**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo    | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                 |
|----------------|---------|--------------------------------------|-----------------------------------------------------------------------------|
| Spreadsheet    | File    | FormData                             | Carica il file del foglio di calcolo.                                       |
| worksheet      | String  | Query                                | Il nome del foglio di calcolo contenente il grafico.                        |
| chartIndex     | Integer | Query                                | L'indice del grafico da convertire.                                         |
| outPath        | String  | Query                                | (Opzionale) Il percorso della cartella in cui viene salvato il file convertito. Default: null. |
| outStorageName | String  | Query                                | Nome dell'archivio di output per il file.                                   |
| fontsLocation  | String  | Query                                | Usa font personalizzati, se necessario.                                      |
| region         | String  | Query                                | Impostazione della regione del foglio di calcolo.                           |
| password       | String  | Query                                | La password per aprire il file del foglio di calcolo.                       |

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
|--------|-------------------------|-------------------------------------------------------------------|
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto sul server.                                    |

## Dove dovresti utilizzare l’API Converti grafico in PDF?

### **1. Resoconti aziendali e automazione**

- **Reparti finanziari**: grafici dei report finanziari mensili → archiviazione PDF
- **Team di vendita**: grafici di andamento delle performance → report PDF per i clienti
- **Analisi di marketing**: grafici di performance delle campagne → riassunti esecutivi PDF
- **Gestione operativa**: grafici di monitoraggio della produzione → documenti PDF per la conformità

### **2. Sviluppo software e integrazione**

- **Applicazioni SaaS**: dati dei grafici generati dagli utenti → report PDF scaricabili
- **Sistemi enterprise**: grafici dei sistemi ERP/CRM → documentazione PDF per audit
- **Applicazioni mobile**: grafici di analisi in-app → file PDF condivisibili
- **Applicazioni web**: grafici delle dashboard → funzionalità di esportazione in PDF

### **3. Flussi di lavoro di elaborazione documenti**

- **Elaborazione in batch**: conversione simultanea in PDF di grafici da più file Excel
- **Attività pianificate**: generazione automatica di report giornalieri/settimanali con grafici
- **Output basati su modelli**: formati di grafico standard → documenti PDF
- **Assemblaggio documenti**: combinazione di grafici con altri contenuti in formato PDF

### **4. Applicazioni specifiche per settore**

- **Istituzioni di ricerca**: grafici di dati sperimentali → figure PDF per articoli scientifici
- **Settore educativo**: grafici di materiali didattici → materiali per corsi PDF
- **Aziende di consulenza**: grafici di analisi → documenti PDF per i clienti
- **Industria manifatturiera**: grafici di controllo qualità → report PDF per ispezioni
- **Sanità**: grafici di dati dei pazienti → record medici PDF
- **Pubblica amministrazione**: grafici statistici → pubblicazioni ufficiali PDF

### **5. Gestione e distribuzione dei contenuti**

- **Gestione di asset digitali**: archiviazione di grafici in formato PDF standardizzato
- **Basi di conoscenza**: documentazione tecnica con grafici PDF incorporati
- **Portali clienti**: consegna sicura di report PDF agli stakeholder
- **Conformità normativa**: generazione di documentazione PDF pronta per audit

## Perché utilizzare l’API Converti grafico in PDF?

- Puoi convertire i grafici **senza caricare preventivamente il workbook**, risparmiando spazio di archiviazione e riducendo i costi.
- Lo sviluppo può essere completato rapidamente sfruttando gli SDK esistenti di Aspose.Cells Cloud.
- **Integrazione semplice**: API REST con documentazione chiara.
- **Architettura scalabile**: gestisce carichi di lavoro che vanno da operazioni di piccole dimensioni a quelle su scala enterprise.

## Come utilizzare l’API Converti grafico in PDF con gli SDK?

### Specifica dell’API Converti grafico in PDF

La [Specifica dell’API Converti grafico in PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

## Utilizza gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli di basso livello e ti permette di convertire un grafico in un file PDF con pochissimo codice.  
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells Cloud utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}