---
title: "Lavorare con l'eliminazione di righe in un foglio di calcolo Excel"
second_title: "Document"
linktitle: "Elimina"
type: docs
url: /rows/delete/
keywords: "Aspose.Cells, elimina riga, API Excel, REST, cloud, foglio di calcolo, Excel, SDK"
description: "Scopri come eliminare una singola riga o più righe in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi di codice per Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift."
weight: 20
ArticleTitle: "Lavorare con l'eliminazione di righe in un foglio di calcolo Excel – Guida all'API Aspose.Cells Cloud"
---

## Operazioni di eliminazione disponibili

Gli esempi seguenti mostrano come eliminare una singola riga vuota o più righe da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud.

- [Come eliminare una riga vuota in un foglio di calcolo Excel](/cells/rows/delete/row/)
- [Come eliminare più righe in un foglio di calcolo Excel](/cells/rows/delete/rows/)

**Riferimento API**

| Elemento                | Dettagli |
|---------------------|---------------------------------------------------------------|
| **Metodo HTTP**     | DELETE |
| **Endpoint**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Parametri di percorso**| `fileName` – nome del file Excel (obbligatorio)<br>`sheetName` – nome del foglio di calcolo (obbligatorio) |
| **Parametri di query**| `startrow` – indice della prima riga da eliminare (obbligatorio)<br>`totalRows` – numero di righe da eliminare (obbligatorio)<br>`storage` – nome dello storage cloud (opzionale)<br>`folder` – percorso della cartella nello storage (opzionale) |
| **Corpo della richiesta**    | *Nessuno* |
| **Esempio di risposta**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Codici di stato possibili**| 200 OK – righe eliminate correttamente<br>400 Bad Request – parametri non validi<br>401 Unauthorized – errore di autenticazione<br>404 Not Found – file o foglio di calcolo non trovato<br>500 Internal Server Error – problema lato server |

**Vedi anche**

- [Aggiungi riga](/cells/rows/add/)
- [Ottieni riga](/cells/rows/get/)
- [Copia riga](/cells/rows/copy/)
- [Nascondi riga](/cells/rows/hide/)
- [Panoramica sulle righe](/cells/rows/)