---
title: "Come aggiungere righe a un foglio di lavoro di Excel"
second_title: "Document"
linktype: "Add"
type: docs
url: /it/rows/add/
keywords: "Aspose.Cells, aggiungere righe, API Excel, REST, C#, Java, Python, Node.js"
description: "Guida passo-passo per aggiungere una singola riga o più righe a un foglio di lavoro di Excel utilizzando l'API REST di Aspose.Cells Cloud, con esempi di codice per C#, Java, Python e Node.js."
weight: 20
ArticleTitle: "Aggiungi righe a un foglio di lavoro di Excel tramite l'API Aspose.Cells Cloud – Guida passo-passo"
---

## Come aggiungere righe a un foglio di lavoro di Excel

Questo articolo spiega come inserire una singola riga vuota o più righe in un foglio di lavoro esistente utilizzando l'API REST di Aspose.Cells Cloud. Prima di procedere, assicurati di disporre di una chiave API valida e dell'SDK appropriato installato.

**Prerequisiti**  
- [ ] Account Aspose.Cells Cloud con abbonamento attivo.  
- [ ] Chiave API/Token di accesso generato dalla dashboard di Aspose Cloud.  
- [ ] Uno degli SDK supportati (C#, Java, Python, Node.js) installato e configurato.  

**Riferimento API**  
- **Metodo HTTP:** `POST`  
- **Endpoint:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **Parametri di percorso obbligatori:**  
  - `fileName` – Nome del file Excel memorizzato nel cloud.  
  - `sheetName` – Nome del foglio di lavoro in cui verranno aggiunte le righe.  
- **Parametri di query:**  
  - `startrow` – Indice in base zero della riga a partire dalla quale inizia l'inserimento.  
  - `totalRows` – Numero di righe da inserire.  
  - `folder` – (Opzionale) Percorso della cartella cloud del file.  
  - `storage` – (Opzionale) Nome dello storage se si utilizza uno storage non predefinito.  
- **Corpo della richiesta (esempio JSON):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **Esempio cURL**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **Risposta in caso di esito positivo (HTTP 200):** Restituisce le informazioni aggiornate sul foglio di lavoro, inclusa la nuova conta delle righe.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **Esempio di risposta di errore (HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "Parametro startrow non valido. Deve essere un intero non negativo."
  }
  ```

- **Codici di stato:**  

  | Codice | Significato                            |
  |--------|----------------------------------------|
  | 200    | Riga/e aggiunte correttamente          |
  | 400    | Parametri non validi o JSON malformato |
  | 401    | Autenticazione non riuscita            |
  | 404    | File o foglio di lavoro non trovato    |
  | 500    | Errore del server                      |

Di seguito sono riportati i collegamenti rapidi agli esempi dettagliati per l'aggiunta di righe:

- [Come aggiungere una riga vuota a un foglio di lavoro di Excel](/cells/rows/add/row/)
- [Come aggiungere più righe a un foglio di lavoro di Excel](/cells/rows/add/rows/)
---