---
---
title: "Aspose.Cells Cloud AI – Scomposizione delle attività, traduzione di fogli di calcolo e testo"
second_title: "Documento"
ArticleTitle: "Migliora le tue competenze sull'AI: impara la traduzione di Excel, la scomposizione delle attività e altro ancora"
linktitle: "AI"
type: docs
url: /ai/
keywords: "Aspose.Cells, Cloud AI, traduzione di Excel, scomposizione delle attività, REST API"
description: "Esplora Aspose.Cells Cloud AI per scomporre attività, tradurre cartelle di lavoro Excel e file di testo. Include endpoint REST, codice di esempio e best practice."
weight: 20
---

Aspose.Cells Cloud AI offre tre potenti servizi basati sull'intelligenza artificiale che semplificano il lavoro con dati di Excel e testo: **Scomponi attività utente**, **Traduci foglio di calcolo** e **Traduci file di testo**. Queste API consentono agli sviluppatori di suddividere programmaticamente obiettivi utente complessi in passi operativi, tradurre intere cartelle di lavoro o file di testo semplice e integrare i risultati in applicazioni personalizzate. Usa gli endpoint riportati di seguito per iniziare rapidamente, e fai riferimento alle specifiche dettagliate di richiesta/risposta fornite per ciascun servizio.

- **[Scomponi attività utente](https://docs.aspose.cloud/cells/decompose-user-task/)** – Converti obiettivi utente in piani d’azione sequenziali grazie a Aspose.Cells Cloud AI.  
  - **Metodo richiesta:** `POST`  
  - **URL endpoint:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **Intestazioni:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **Corpo richiesta (JSON):**  
    ```json
    {
      "task": "Genera un report trimestrale delle vendite con grafici e tabelle pivot"
    }
    ```  
  - **Risposta:** Restituisce il file del foglio di calcolo contenente l’elenco delle attività come file scaricabile.  
  - **Codici di stato:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **Prerequisiti:** Un token di accesso valido con ambito **CellsAI**.  
  - **Esempio di risposta ( frammento JSON):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **Note:** La cartella di lavoro generata include un foglio denominato **TaskList** con i passaggi ordinati. Limite di frequenza: 100 richieste al minuto.

- **[Traduci foglio di calcolo](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Traduci un intero foglio di calcolo con Aspose.Cells Cloud AI.  
  - **Metodo richiesta:** `POST`  
  - **URL endpoint:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **Intestazioni:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Parametri richiesta:**  
    - `file` – Il file Excel da tradurre (binario).  
    - `targetLanguage` – Codice linguistico ISO (ad esempio, `fr`, `de`).  
  - **Risposta:** Restituisce la cartella di lavoro tradotta come file scaricabile.  
  - **Codici di stato:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Prerequisiti:** Token di accesso con ambito **CellsAI** e spazio di archiviazione sufficiente.  
  - **Esempio di risposta ( framcento JSON):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **Note:** Vengono tradotti tutti i valori delle celle, i commenti e i nomi dei fogli. Limite di frequenza: 100 richieste al minuto.

- **[Traduci file di testo](https://docs.aspose.cloud/cells/translate-text-file/)** – Traduci un intero file di testo con Aspose.Cells Cloud AI.  
  - **Metodo richiesta:** `POST`  
  - **URL endpoint:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **Intestazioni:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Parametri richiesta:**  
    - `file` – Il file di testo da tradurre (binario).  
    - `targetLanguage` – Codice linguistico ISO (ad esempio, `es`, `ja`).  
  - **Risposta:** Restituisce il file di testo tradotto.  
  - **Codici di stato:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Prerequisiti:** Token di accesso valido con ambito **CellsAI**.  
  - **Esempio di risposta ( frammento JSON):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **Note:** Supporta file di testo semplice codificati in UTF‑8 fino a 5 MB. Limite di frequenza: 100 richieste al minuto.