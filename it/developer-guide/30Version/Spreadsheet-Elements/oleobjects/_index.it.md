---
title: "Lavorare con gli oggetti OLE di Excel"
second_title: "Documento"
linktitle: "OleObjects"
type: docs
url: /it/oleobjects/
aliases: [  /it/working-with-oleobjects/ ]
keywords: "OLE, Excel, Aspose.Cells, API, Cloud"
description: "Utilizza l'API REST Aspose.Cells Cloud per recuperare, aggiungere, aggiornare, eliminare e convertire gli oggetti OLE nei fogli di calcolo Excel. Sono disponibili SDK per Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift e Android."
weight: 100
ArticleTitle: "Lavorare con gli oggetti OLE di Excel – Guida per recuperare, aggiungere, aggiornare, eliminare e convertire gli oggetti OLE"
---

**Come lavorare con gli oggetti OLE in un foglio di calcolo Excel**

L'API REST Aspose.Cells Cloud fornisce un insieme completo di operazioni per gestire gli oggetti OLE in modo programmatico. Di seguito è riportato un riferimento conciso per ciascuna operazione, inclusi il metodo HTTP, il modello di endpoint, i parametri obbligatori e un breve esempio di risposta.

- [Come recuperare un oggetto OLE da un foglio di calcolo Excel](/cells/oleobjects/get/)
  - **Metodo:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametri:** `fileName` (stringa), `sheetName` (stringa), `oleObjectIndex` (intero)  
  - **Esempio di risposta:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [Come aggiungere un oggetto OLE in un foglio di calcolo Excel](/cells/oleobjects/add/)
  - **Metodo:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parametri:** `fileName`, `sheetName`, `oleObject` (binario o in base‑64), `imageFormat` (opzionale)  
  - **Esempio di corpo della richiesta:** multipart/form‑data con il flusso di file.  
  - **Esempio di risposta:** `201 Created` con l'header della posizione del nuovo oggetto OLE.

- [Come aggiornare un oggetto OLE specifico in un foglio di calcolo Excel](/cells/oleobjects/update/)
  - **Metodo:** `PUT`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametri:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (contenuto aggiornato)  
  - **Esempio di risposta:** `200 OK` con i metadati aggiornati dell'oggetto.

- [Come convertire un oggetto OLE in un'immagine in un foglio di calcolo Excel](/cells/oleobjects/convert/)
  - **Metodo:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Parametri:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (ad esempio, `png`, `jpeg`)  
  - **Esempio di risposta:** Flusso binario dell'immagine dell'oggetto OLE convertito.

- [Come eliminare tutti gli oggetti OLE in un foglio di calcolo Excel](/cells/oleobjects/clear/)
  - **Metodo:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parametri:** `fileName`, `sheetName`  
  - **Esempio di risposta:** `204 No Content` che indica che tutti gli oggetti OLE sono stati rimossi.

- [Come eliminare un oggetto OLE specifico in un foglio di calcolo Excel](/cells/oleobjects/delete/)
  - **Metodo:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametri:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Esempio di risposta:** `204 No Content` che conferma l'eliminazione dell'oggetto.