---
---
title: "Lavorare con i commenti di Excel"
second_title: "Document"
linktitle: "Commenti"
type: docs
url: /comments/
aliases: [/working-with-comments/]
keywords: "Aspose.Cells Cloud, API dei commenti di Excel, commenti di fogli di calcolo, API REST"
description: "Scopri come aggiungere, recuperare, aggiornare ed eliminare i commenti di Excel utilizzando l'API REST di Aspose.Cells Cloud v3.0, con esempi di codice, prerequisiti e gestione degli errori."
weight: 100
ArticleTitle: "Lavorare con i commenti di Excel – Guida all'API di Aspose.Cells Cloud"
---

Quando si crea un file di workbook di Excel, gli utenti possono aggiungere commenti per diversi motivi. Un utilizzo comune è spiegare una formula in una cella, specialmente quando il file verrà condiviso con altri. I commenti possono inoltre fungere da promemoria, note per i collaboratori o come mezzo per fare riferimenti incrociati con altri workbook. Una volta aggiunto un commento, Excel consente di ridimensionare, modellare e formattare il riquadro del commento in base allo stile preferito. Padroneggiare la gestione dei commenti aiuta gli utenti a sfruttare al meglio questa funzionalità.

**Prerequisiti**

- Un account attivo Aspose.Cells Cloud.  
- Un **token di accesso** valido ottenuto tramite OAuth 2.0.  
- Versione dell'API **v3.0** (gli endpoint utilizzati in questa guida appartengono a questa versione).  
- Opzionale: Aspose.Cells SDK per il linguaggio preferito per semplificare la costruzione delle richieste.

**Versione**

Gli esempi riportati di seguito fanno riferimento all'**API REST di Aspose.Cells Cloud v3.0**. Le future versioni dell'API potrebbero introdurre parametri aggiuntivi o modificare le strutture delle risposte; consultare sempre il riferimento più recente dell'API per dettagli aggiornati.

**Aggiungere un commento**

Per aggiungere un commento, inviare una richiesta **POST** al seguente endpoint:

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Parametri del percorso**

| Parametro | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|--------------|-------------|
| `file`    | string | Sì           | Nome del file del workbook (inclusa l'estensione). |
| `sheet`   | string | Sì           | Nome del foglio di calcolo in cui verrà aggiunto il commento. |

**Schema del corpo della richiesta**

| Campo     | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|--------------|-------------|
| `CellName`| string | Sì           | Indirizzo della cella in formato A1 (ad esempio, **B2**). |
| `Comment` | string | Sì           | Testo del commento da memorizzare. |
| `Author`  | string | No           | Nome dell'autore del commento. |

**Esempio di corpo della richiesta**

```json
{
  "CellName": "B2",
  "Comment": "Richiesta revisione",
  "Author": "Mario Rossi"
}
```

**Risposta di successo (esempio)** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "Mario Rossi",
    "HtmlComment": "Richiesta revisione",
    "Note": "Richiesta revisione"
  }
}
```

**Codici di errore comuni**

| Codice | Significato |
|--------|-------------|
| 400    | Indirizzo della cella o corpo della richiesta non validi |
| 401    | Non autorizzato – token mancante o non valido |
| 404    | Workbook o foglio di calcolo non trovato |

**Ottenere i commenti**

Recuperare tutti i commenti da un foglio di calcolo:

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Parametri del percorso**

| Parametro | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|--------------|-------------|
| `file`    | string | Sì           | Nome del file del workbook. |
| `sheet`   | string | Sì           | Nome del foglio di calcolo. |

**Esempio di risposta**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Alice",
      "HtmlComment": "Valore iniziale",
      "Note": "Valore iniziale"
    },
    {
      "CellName": "B2",
      "Author": "Mario Rossi",
      "HtmlComment": "Richiesta revisione",
      "Note": "Richiesta revisione"
    }
  ]
}
```

**Aggiornare un commento**

Per modificare un commento esistente, inviare una richiesta **PUT**. Il commento è identificato dal proprio **indice** all'interno della raccolta di commenti del foglio di calcolo (l'indice parte da 0).

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Parametri del percorso**

| Parametro      | Tipo | Obbligatorio | Descrizione |
|----------------|------|--------------|-------------|
| `file`         | string | Sì         | Nome del file del workbook. |
| `sheet`        | string | Sì         | Nome del foglio di calcolo. |
| `commentIndex` | int  | Sì           | Indice in base zero del commento da aggiornare. |

**Schema del corpo della richiesta**

| Campo    | Tipo   | Obbligatorio | Descrizione |
|----------|--------|--------------|-------------|
| `Comment`| string | Sì           | Nuovo testo del commento. |
| `Author` | string | No           | Nome dell'autore aggiornato (opzionale). |

**Esempio di corpo della richiesta**

```json
{
  "Comment": "Testo della nota aggiornato",
  "Author": "Mario Rossi"
}
```

La risposta segue la stessa struttura della risposta dell'operazione **Aggiungere un commento**.

**Eliminare un commento**

Rimuovere un singolo commento tramite il proprio indice:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**Parametri del percorso**

| Parametro      | Tipo | Obbligatorio | Descrizione |
|----------------|------|--------------|-------------|
| `file`         | string | Sì         | Nome del file del workbook. |
| `sheet`        | string | Sì         | Nome del foglio di calcolo. |
| `commentIndex` | int  | Sì           | Indice in base zero del commento da eliminare. |

Una cancellazione riuscita restituisce:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Eliminare tutti i commenti**

Per cancellare tutti i commenti da un foglio di calcolo:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Parametri del percorso**

| Parametro | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|--------------|-------------|
| `file`    | string | Sì           | Nome del file del workbook. |
| `sheet`   | string | Sì           | Nome del foglio di calcolo. |

**Linee guida per la gestione degli errori**

- **404 Not Found** – Verificare che l'ID del workbook, il nome del foglio di calcolo e l'indice del commento siano corretti.  
- **400 Bad Request** – Controllare la sintassi JSON e i campi obbligatori (`CellName`, `Comment`).  
- **429 Too Many Requests** – Implementare un ritardo esponenziale e rispettare l'intestazione `Retry-After`.

**Riepilogo**

- I commenti di Excel vengono utilizzati per [aggiungere una nota o spiegare una formula in una cella](/cells/comments/add/).  
- Excel offre agli utenti la flessibilità di [modificare](/cells/comments/update/), [eliminare](/cells/comments/delete/) e [visualizzare](/cells/comments/get/) o [nascondere](/cells/comments/update/) i commenti in un foglio di calcolo.  
- Gli utenti possono inoltre [ridimensionare](/cells/comments/update/) e [spostare](/cells/comments/update/) il riquadro del commento.  

Per ulteriori informazioni su come lavorare con altri elementi dei fogli di calcolo, consultare la guida su [lavorare con le celle](/cells/working-with-cells/).