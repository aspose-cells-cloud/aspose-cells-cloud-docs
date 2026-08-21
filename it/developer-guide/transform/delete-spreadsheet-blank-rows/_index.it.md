---
title: "Aspose.Cells Cloud Web API – Elimina automaticamente le righe vuote/bianche"
second_title: "Documento"
ArticleTitle: "Come eliminare tutte le righe vuote in Excel – Guida completa alla pulizia dei dati"
linktitle: "Elimina righe vuote"
type: docs
url: /it/delete-spreadsheet-blank-rows/
keywords: "Aspose.Cells, Excel, righe vuote, eliminare righe, pulizia foglio elettronico, API"
description: "Rimuovi tutte le righe vuote dai file Excel tramite l'API Aspose.Cells Cloud. Veloce, pronta per l'elaborazione in batch e completamente programmabile – consulta gli esempi di codice in C#, Java, Python e altro ancora."
weight: 100
---

Elimina automaticamente tutte le righe vuote dai fogli elettronici Excel utilizzando l'API Aspose.Cells Cloud. La nostra API intelligente rileva e rimuove le righe prive di dati, formule, commenti o oggetti, preservando contemporaneamente tutto il resto del contenuto. Supporta l'elaborazione in batch, l'automazione nel cloud e l'integrazione senza soluzione di continuità per flussi di lavoro aziendali di pulizia dei dati.

## API DeleteSpreadsheetBlankRows

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


### Parametri della richiesta

| Nome del parametro | Tipo   | Posizione | Descrizione                                                                                                                                    |
|--------------------|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet        | File   | FormData  | Il file Excel (`.xlsx`, `.xls`, `.ods`, ecc.) da elaborare.                                                                                   |
| outPath            | String | Query     | (Opzionale) Directory di destinazione nel tuo archivio cloud per il foglio di calcolo pulito. Se omesso, il file viene salvato accanto a quello originale. |
| outStorageName     | String | Query     | Nome dell'archivio cloud configurato (es. `MyDropbox`, `CorporateOneDrive`). Richiesto quando si desidera salvare l'output in uno storage specifico. |
| region             | String | Query     | Impostazioni locali (es. `en-US`, `fr-FR`) applicate durante l'elaborazione.                                                                   |
| password           | String | Query     | Password per aprire un foglio elettronico crittografato. Omettere se il file non è protetto.                                                   |

**Autenticazione**  
Tutte le chiamate devono includere l'intestazione `Authorization: Bearer <access_token>`. Ottieni il token di accesso tramite il flusso OAuth2 di Aspose Cloud, come descritto nella guida all'autenticazione.

**Prerequisiti e note**  
- Assicurati che il tuo archivio Aspose Cloud sia configurato e che il foglio di calcolo di origine sia caricato prima di richiamare l'API.  
- I formati di file supportati includono `.xlsx`, `.xls`, `.ods` e altri tipi comuni di fogli elettronici.  
- La dimensione massima del file è di 150 MB per singola richiesta; i file più grandi devono essere elaborati a blocchi.  

### Risposta

L'API restituisce un array JSON contenente un riferimento al file elaborato.

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

### Codici di errore

- **400 Bad Request** – URI dell'API Aspose.Cells Cloud non valido.
- **401 Unauthorized** – Token di accesso o credenziali client non valide.
- **404 Not Found** – Impossibile accedere al file del foglio elettronico.
- **500 Server Error** – Si è verificato un errore imprevisto durante l'elaborazione del file.

## Dove dovresti utilizzare l'API per eliminare le righe vuote dei fogli elettronici?

- **Flussi di lavoro di importazione e pulizia dei dati** – Pulisci immediatamente le righe vuote finali o strutturali dopo aver importato dati da file CSV, database o API web.
- **Generazione di report e dashboard** – Garantisci un aspetto professionale rimuovendo le righe vuote superflue prima di finalizzare report finanziari, di vendita o operativi.
- **Preparazione dei dati per l’analisi (ETL)** – Pre-processa i dati Excel nelle pipeline ETL prima di caricarli in data warehouse (Snowflake, BigQuery) o strumenti BI (Tableau, Power BI).
- **Integrazione di sistemi e feed API** – Normalizza i file Excel ricevuti da sistemi partner, CRM o ERP rimuovendo le righe inutilizzate.
- **Automazione di documenti ed elaborazione in batch** – Rimuovi le righe segnaposto generate dai motori di template prima della distribuzione.
- **Elaborazione di contenuti generati dall’utente** – Standardizza i file Excel caricati da portali web o applicazioni prima di ulteriori elaborazioni o archiviazione.
- **Migrazione di dati legacy** – Semplifica gli archivi di vecchi fogli elettronici eliminando le righe vuote o segnaposto storici.

## Perché dovresti utilizzare l'API per eliminare le righe vuote dei fogli elettronici?

- **Facile da usare per sviluppatori** – Gli SDK sono disponibili per molteplici linguaggi, riducendo lo sforzo di sviluppo rispetto alla creazione di soluzioni personalizzate.
- **Riduzione dei costi di manodopera** – Elimina la necessità di pulizia manuale dei fogli elettronici o di personale dedicato.
- **Pay-per-use** – Paghi soltanto per le chiamate API effettivamente effettuate.
- **Costi zero di manutenzione** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare l'API per eliminare le righe vuote dei fogli elettronici con gli SDK

### Specifica dell'API Delete Spreadsheet Blank Rows

La [Specifiche dell'API per eliminare le righe vuote dei fogli elettronici](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) definisce un'interfaccia di programmazione accessibile pubblicamente e ti consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzo degli SDK Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendoti di eliminare le righe vuote nei fogli elettronici con pochissimo codice.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}  
{{</tab>}}  
{{< /tabs >}}