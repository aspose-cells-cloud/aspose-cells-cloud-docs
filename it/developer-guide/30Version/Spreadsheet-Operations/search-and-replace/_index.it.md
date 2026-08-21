---
---
title: "Cercare e sostituire contenuti di testo in file Excel"
second_title: "Documentazione"
linktitle: "Cerca e sostituisci"
type: docs
url: /it/search-and-replace/
aliases: [/it/working-with-text/, /it/text/]
description: "Scopri come cercare e sostituire testo in cartelle di lavoro e fogli di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud. Include il formato della richiesta, codice di esempio per .NET, Java, Python e gestione degli errori."
keywords: "Aspose.Cells Cloud, Excel, cerca e sostituisci, API REST, .NET, Java, Python"
weight: 20
ArticleTitle: "Cercare e sostituire testo in file Excel mediante l'API Aspose.Cells Cloud"
---

Le operazioni sul testo rappresentano processi complessi per i file Excel. Molteplici fattori contribuiscono a questa complessità e devono essere presi in considerazione durante l'elaborazione. Aspose.Cells Cloud fornisce un modo affidabile per cercare e sostituire testo in una vasta gamma di formati di fogli di calcolo.

Lavorare con il testo in cartelle di lavoro Excel richiede spesso di individuare stringhe specifiche e aggiornarle in più fogli. L'API Aspose.Cells Cloud semplifica questa operazione fornendo un'azione unificata di **ricerca e sostituzione** che funziona su qualsiasi formato di foglio di calcolo supportato.

## Panoramica

La ricerca e sostituzione consente di individuare stringhe specifiche in una cartella di lavoro o in un particolare foglio di calcolo e sostituirle con nuovi valori. L'operazione funziona con tutti i formati supportati da Aspose.Cells Cloud, come **XLS, XLSX, XLSM, XLSB, ODS, CSV** e altri. Utilizzando la funzionalità di **ricerca e sostituzione** è possibile pulire rapidamente i dati, correggere errori di battura ripetuti o applicare convenzioni di denominazione in blocco in tutta la cartella di lavoro.

## Prerequisiti

- Un account Aspose.Cloud attivo con un **Client‑Id** e una **Client‑Secret** validi.
- Token di accesso ottenuto tramite il flusso di autenticazione OAuth 2.0.
- La cartella di lavoro target deve essere memorizzata nell'archivio cloud di Aspose o accessibile tramite un URL pubblico.
- SDK richiesto installato (ad esempio, Aspose.Cells‑Cloud per .NET, Java o Python).

## Riferimento API

**Metodo:** `POST`  
**Endpoint**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| Parametro        | Tipo    | Obbligatorio | Descrizione                                                                                             |
| ---------------- | ------- | ------------ | ------------------------------------------------------------------------------------------------------- |
| `fileName`       | string  | Sì           | Nome della cartella di lavoro (inclusa l'estensione).                                                  |
| `folder`         | string  | No           | Percorso della cartella nell'archivio cloud.                                                            |
| `storage`        | string  | No           | Nome dell'archivio, se diverso da quello predefinito.                                                  |
| `sheetName`      | string  | No           | Nome del foglio di calcolo specifico; se omesso, l'operazione viene applicata all'intera cartella.     |
| `searchString`   | string  | Sì           | Testo da cercare.                                                                                       |
| `replaceString`  | string  | Sì           | Testo da utilizzare per la sostituzione delle occorrenze trovate.                                      |
| `ignoreCase`     | boolean | No           | Impostare su `true` per eseguire una ricerca che non distingue tra maiuscole e minuscole.               |
| `matchWholeCell` | boolean | No           | Impostare su `true` per sostituire solo le corrispondenze di intere celle.                              |

**Intestazioni**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**Corpo della richiesta (JSON)**

```json
{
  "searchString": "OldValue",
  "replaceString": "NewValue",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Sheet1"
}
```

**Risposta corretta (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## Format supportati

| Format                            | Estensione                |
| --------------------------------- | ------------------------- |
| Cartella di lavoro Excel          | .xls, .xlsx, .xlsm, .xlsb |
| Foglio di calcolo OpenDocument    | .ods                      |
| CSV                               | .csv                      |
| Altri (come supportati da Aspose.Cells) | —                         |

## Esempi di codice

Di seguito sono riportati esempi minimi per tre SDK popolari. Sostituire `{clientId}`, `{clientSecret}` e altri segnaposto con i valori effettivi. Questi esempi illustrano come eseguire un'operazione di **ricerca e sostituzione** in modo programmatico.

## Gestione errori e casi limite

| Codice HTTP | Significato                                         | Azione consigliata                                                  |
| ----------- | --------------------------------------------------- | ------------------------------------------------------------------- |
| 400         | Richiesta non valida – parametri mancanti o non validi | Verificare i campi obbligatori e i relativi tipi di dati.          |
| 401         | Non autorizzato – token non valido o scaduto       | Aggiornare il token di accesso.                                     |
| 404         | Non trovato – la cartella di lavoro o il foglio non esistono | Verificare il nome del file, il percorso della cartella e `sheetName`. |
| 415         | Tipo di supporto non supportato – formato file non valido | Assicurarsi che il file caricato sia in un formato Excel o CSV supportato. |
| 202         | Accettata – richiesta accettata per l'elaborazione | Effettuare il polling dello stato dell'operazione se viene utilizzata l'elaborazione asincrona. |
| 204         | Nessun contenuto – operazione riuscita senza corpo | La sostituzione è stata applicata; non sono stati restituiti dati aggiuntivi. |
| 500         | Errore interno del server – errore imprevisto      | Riprovare dopo un breve intervallo; contattare il supporto Aspose se il problema persiste. |

**Note:**  
- Le cartelle di lavoro di grandi dimensioni potrebbero superare i limiti di dimensione della richiesta; considerare di caricare prima il file nell'archivio cloud.  
- Quando `ignoreCase` è impostato su `true`, tenere presente che le mappature di maiuscole/minuscole specifiche della lingua possono influenzare i risultati.  
- L'utilizzo di `matchWholeCell` con formule non sostituirà le corrispondenze parziali all'interno del testo della formula.

## Ricerca e sostituzione in file Excel

- [Come ottenere gli elementi di testo da una cartella di lavoro Excel.](/it/cells/workbook/get-text-items/)
- [Come ottenere gli elementi di testo da un foglio di calcolo Excel.](/it/cells/worksheets/get-text-items/)
- [Come cercare testo da una cartella di lavoro Excel.](/it/cells/workbook/find-text/)
- [Come cercare testo da un foglio di calcolo Excel.](/it/cells/worksheets/find-text/)
- [Come cercare testo da file Excel senza caricare un file.](/it/cells/search/)
- [Come sostituire testo da una cartella di lavoro Excel.](/it/cells/workbook/replace-text/)
- [Come sostituire testo da un foglio di calcolo Excel.](/it/cells/worksheets/replace-text/)
- [Come sostituire testo da file Excel senza caricare un file.](/it/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Cercare e sostituire testo in file Excel mediante l'API Aspose.Cells Cloud",
  "description": "Documentazione per l'endpoint di ricerca e sostituzione di Aspose.Cells Cloud, incluso il formato della richiesta, i parametri, gli esempi e la gestione degli errori.",
  "url": "https://docs.aspose.cloud/it/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, cerca e sostituisci, API, REST"
}
</script>