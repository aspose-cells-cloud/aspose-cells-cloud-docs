---
title: "Lavorare con le immagini in Excel"
second_title: "Documenti"
linktitle: "Immagini"
type: docs
url: /it/pictures/
aliases: [  /it/working-with-pictures/ ]
keywords: "Excel, immagine, Aspose.Cells Cloud, REST API, gestione immagini, immagini Excel"
description: "Scopri come recuperare, aggiungere, aggiornare ed eliminare le immagini nei fogli di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi di codice per C#, Java, Python e altro ancora."
weight: 100
ArticleTitle: "Lavorare con le immagini in Excel – Documentazione di Aspose.Cells Cloud"
---

## Lavorare con le immagini in un file Excel

Questa guida spiega come lavorare con le **immagini** (chiamate anche immagini) nei fogli di lavoro Excel tramite l'API REST di Aspose.Cells Cloud. Copre le principali operazioni relative alle immagini—recuperarle, aggiungerle, aggiornarle ed eliminarle—and fornisce collegamenti ad esempi dettagliati per ciascuna attività.

**Prerequisiti**: un account Aspose.Cells Cloud, una chiave API valida e l'SDK appropriato installato per il linguaggio scelto.

- [Come ottenere un'immagine in un formato specifico da un foglio di lavoro Excel.](/it/cells/pictures/get/) – Recupera un'unica immagine nel formato richiesto (PNG, JPEG, ecc.) da un foglio di lavoro.  
- [Come ottenere tutte le informazioni sulle immagini da un foglio di lavoro Excel.](/it/cells/pictures/get-all/) | Elenca i metadati di ogni immagine contenuta in un foglio di lavoro.  
- [Come aggiungere un'immagine a un foglio di lavoro Excel.](/it/cells/pictures/add/) – Inserisce una nuova immagine in un foglio di lavoro, specificandone posizione e dimensioni.  
- [Come aggiornare un'immagine specifica da un foglio di lavoro Excel.](/it/cells/pictures/update/) – Modifica le proprietà (ad esempio, dimensioni e posizione) di un'immagine esistente.  
- [Come eliminare tutte le immagini da un foglio di lavoro Excel.](/it/cells/pictures/clear/) – Rimuove tutti gli oggetti immagine da un foglio di lavoro in una singola chiamata.  
- [Come eliminare un'immagine da un foglio di lavoro Excel.](/it/cells/pictures/delete/) – Elimina un’unica immagine identificata dal suo indice.  

**Riferimento API**

**Ottenere un'immagine in un formato specifico**

| Metodo HTTP | Endpoint | Parametri obbligatori | Richiesta di esempio | Risposta di esempio | Codici di stato |
|-------------|----------|-----------------------|----------------------|--------------------|-----------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path), `format` (query) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | Dati binari dell'immagine (PNG, JPEG, ecc.) | 200 OK, 400 Richiesta non valida, 401 Non autorizzato, 404 Non trovato, 500 Errore server |

**Ottenere tutte le informazioni sulle immagini**

| Metodo HTTP | Endpoint | Parametri obbligatori | Richiesta di esempio | Risposta di esempio | Codici di stato |
|-------------|----------|-----------------------|----------------------|--------------------|-----------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | Array JSON con metadati delle immagini (indice, nome, posizione, dimensioni) | 200 OK, 400, 401, 404, 500 |

**Aggiungere un’immagine**

| Metodo HTTP | Endpoint | Parametri obbligatori | Corpo della richiesta di esempio | Risposta di esempio | Codici di stato |
|-------------|----------|-----------------------|----------------------------------|--------------------|-----------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `{ "image": "<immagine-in-base64>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Creato, 400, 401, 404, 500 |

**Aggiornare un’immagine**

| Metodo HTTP | Endpoint | Parametri obbligatori | Corpo della richiesta di esempio | Risposta di esempio | Codici di stato |
|-------------|----------|-----------------------|----------------------------------|--------------------|-----------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Eliminare tutte le immagini**

| Metodo HTTP | Endpoint | Parametri obbligatori | Richiesta di esempio | Risposta di esempio | Codici di stato |
|-------------|----------|-----------------------|----------------------|--------------------|-----------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (path), `sheetName` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "Tutte le immagini eliminate." }` | 200 OK, 400, 401, 404, 500 |

**Eliminare un’immagine specifica**

| Metodo HTTP | Endpoint | Parametri obbligatori | Richiesta di esempio | Risposta di esempio | Codici di stato |
|-------------|----------|-----------------------|----------------------|--------------------|-----------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (path), `sheetName` (path), `pictureIndex` (path) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Immagine eliminata." }` | 200 OK, 400, 401, 404, 500 |

**Argomenti correlati**

Esplora altre operazioni relative alle immagini in Aspose.Cells Cloud:  
- [Lavorare con le forme](/it/cells/shapes/) – aggiungi, modifica ed elimina forme di disegno.  
- [Lavorare con i grafici](/it/cells/charts/) – crea e manipola oggetti grafico.  
- [Lavorare con le immagini nei fogli di lavoro](/it/cells/images/) – incorpora e gestisci file immagine grezzi.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Lavorare con le immagini in Excel – Documentazione di Aspose.Cells Cloud",
  "description": "Guida per recuperare, aggiungere, aggiornare ed eliminare immagini Excel tramite l'API REST di Aspose.Cells Cloud.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "immagini Excel, Aspose.Cells Cloud, REST API, gestione immagini",
  "url": "https://docs.aspose.cloud/it/cells/pictures/"
}
</script>