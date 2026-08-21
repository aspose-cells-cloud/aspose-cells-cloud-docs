---
title: "Aspose.Cells Cloud – Unisci, dividi & importa dati di fogli di calcolo"
second_title: "Documento"
ArticleTitle: "Elaborazione dei dati dei fogli di calcolo – Unisci, dividi & importa"
linktitle: "Elaborazione dei dati"
type: docs
url: /it/data-processing/
keywords: "Aspose.Cells Cloud, elaborazione dati foglio di calcolo, unione Excel, divisione Excel, importazione CSV, importazione JSON, API"
description: "Guida dettagliata per l'importazione di dati CSV/JSON, l'unione di cartelle di lavoro Excel remote e la divisione di fogli di calcolo di grandi dimensioni tramite l'API REST di Aspose.Cells Cloud, inclusi esempi di richieste e risposte."
weight: 30
---

**Aspose.Cells Cloud** – un servizio RESTful che consente la manipolazione programmata di file Excel nel cloud. Supporta l'importazione di dati da vari formati, l'unione di cartelle di lavoro e la divisione di fogli di calcolo di grandi dimensioni.

La sezione **Elaborazione dei dati** dell'API Aspose.Cells Cloud consente di importare, unire e dividere i dati dei fogli di calcolo in modo programmato. Usa gli endpoint riportati di seguito per gestire importazioni CSV/JSON, combinare cartelle di lavoro o dividere file di grandi dimensioni in parti più gestibili.

## Importazione e gestione dei dati

- **[Importa dati CSV, JSON, XML nei file Excel](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

L'operazione di importazione accetta payload in formato CSV, JSON o XML e crea un nuovo foglio (o aggiorna uno esistente) nella cartella di lavoro di destinazione.

**Dettagli endpoint**

| Metodo HTTP | Endpoint | Corpo della richiesta | Risposta in caso di successo |
|-------------|----------|-----------------------|------------------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` o `text/csv` (a seconda del formato) | `200 OK` con JSON contenente i metadati aggiornati della cartella di lavoro |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *nessuno* | Restituisce il file della cartella di lavoro elaborata |

**Esempio di richiesta cURL (importazione CSV)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Esempio di risposta JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **Prerequisiti**: È necessario un token di accesso OAuth2. Il file di origine deve trovarsi nello storage di Aspose Cloud o essere fornito tramite upload multipart.

## Operazione di unione di file

- **[Unisci file Excel remoti in una cartella di lavoro specificata](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Unisci più file Excel in una singola cartella di lavoro](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Unisci file Excel che corrispondono in una cartella remota](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

L’unione combina due o più cartelle di lavoro in una singola cartella di lavoro di destinazione. L’API supporta sia elenchi espliciti di file che fusioni basate su pattern all’interno di una cartella di storage.

**Dettagli endpoint**

| Metodo HTTP | Endpoint | Parametri | Risposta in caso di successo |
|-------------|----------|-----------|------------------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (array di nomi file), `target` (nome facoltativo della cartella di lavoro di destinazione) | `200 OK` con JSON che descrive la cartella di lavoro unita |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` con metadati della cartella di lavoro unita |

**Esempio di richiesta cURL (unione elenco esplicito)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Esempio di risposta JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Prerequisiti**: Tutte le cartelle di lavoro di origine devono essere memorizzate nella stessa posizione dello storage cloud e l’utente chiamante deve disporre di autorizzazioni di lettura/scrittura.

## Operazione di divisione di file

- **[Dividi un file Excel in più file in base ai fogli](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Dividi un file Excel secondo regole personalizzate](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

La divisione estrae singoli fogli o gruppi di righe/colonne in file di cartelle di lavoro separati.

**Dettagli endpoint**

| Metodo HTTP | Endpoint | Parametri | Risposta in caso di successo |
|-------------|----------|-----------|------------------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (es. `worksheet`), `outputFolder` | `200 OK` con elenco di URL dei file generati |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | JSON di regola personalizzata (dimensione pagina, intervallo righe, ecc.) | `200 OK` con dettagli dei file suddivisi |

**Esempio di richiesta cURL (divisione per foglio)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Esempio di risposta JSON**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Prerequisiti**: La cartella di lavoro di origine deve essere accessibile nello storage di Aspose Cloud e l’utente chiamante deve disporre di autorizzazioni di scrittura per la cartella di destinazione.