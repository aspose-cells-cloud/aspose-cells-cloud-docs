---
---
title: "Informazioni sul file"
second_title: "Documento"
linktitle: "Informazioni sul file"
type: docs
url: /file-info/
keywords: "File, Informazioni, Excel, Aspose.Cells, API cloud, Metadati, Base64"
description: "Recupera il nome, le dimensioni e il contenuto in Base64 di un file Excel tramite l'API Aspose.Cells Cloud. Include la sintassi della richiesta, codice di esempio e gestione degli errori."
weight: 79
ArticleTitle: "Informazioni sul file – Metadati e contenuto in Base64 dei file Excel (API Aspose.Cells Cloud)"
---

## Proprietà FileInfo


| Nome            | Tipo   | Descrizione                                                |
| --------------- | ------ | ---------------------------------------------------------- |
| **FileName**    | string | Il nome del file, inclusa la sua estensione.              |
| **FileSize**    | long   | La dimensione del file in byte.                            |
| **FileContent** | string | Contiene i dati grezzi del file Excel codificati in Base64. |

La risposta viene restituita in formato JSON con le stesse tre proprietà mostrate nella tabella precedente, ad esempio:

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### Errori

| Codice HTTP | Significato             | Quando si verifica                        |
| ----------- | ----------------------- | ----------------------------------------- |
| 200         | OK – richiesta riuscita. | Risposta normale.                         |
| 401         | Non autorizzato         | Token di autenticazione mancante o non valido. |
| 404         | Non trovato             | Il file specificato non esiste.           |
| 500         | Errore interno del server | Errore imprevisto lato server.            |

Per ciascun errore, assicurarsi che il token di autenticazione sia valido (401), verificare il percorso del file (404) o consultare la guida generale sulla gestione degli errori per le strategie di ritento (500).

## Vedere anche

- [Ottieni cartella di lavoro](https://docs.aspose.cloud/cells/get-workbook) – recupera un oggetto cartella di lavoro e i suoi fogli di calcolo.  
- [Scarica file](https://docs.aspose.cloud/cells/download-file) – scarica i byte grezzi del file senza codifica in Base64.  
- [Panoramica sull'autenticazione](https://docs.aspose.cloud/cells/authentication) – come ottenere e utilizzare i token di accesso.  
---