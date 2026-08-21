---
---
title: "Introduzione all'API Cloud di Aspose.Cells – Elaborare file Excel in 3 semplici passaggi"
second_title: "Documento"
ArticleTitle: "Introduzione all'API Cloud di Aspose.Cells"
linktitle: "Introduzione"
type: docs
url: /it/getting-started/
description: "Scopri come caricare, convertire e scaricare file Excel utilizzando l'API REST di Aspose.Cells Cloud in tre semplici passaggi. Include esempi di codice cURL."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, conversione foglio elettronico, Excel in PDF, foglio elettronico cloud, API Cloud di Aspose.Cells"
---

- [Panoramica](/cells/overview/)
- [Guida rapida](/cells/quickstart/)
- [SDK disponibili](/cells/available-sdks/)
- [Piattaforme supportate](/cells/supported-platforms/)
- [Formati di file supportati](/cells/supported-file-formats/)
- [Prova Aspose.Cells Cloud](/cells/evaluate-aspose-cells/)
- [Piano tariffario](/cells/pricing-plan/)
- [Supporto tecnico](/cells/technical-support/)
- [Come eseguire un contenitore Docker](/cells/how-to-run-docker-container/)

**Guida introduttiva**

Prima di iniziare, assicurati di avere una **chiave API valida di Aspose Cloud** e un **nome di archiviazione**. Queste credenziali sono obbligatorie per tutte le chiamate API successive.

**Passaggio 1: Caricamento di un file Excel**  
Carica il tuo file di lavoro di origine nell'archiviazione Aspose Cloud.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*Corpo della richiesta*: Il file viene inviato come flusso binario (`application/octet‑stream`).  
*Parametri obbligatori*:

- `path` – percorso nell'archiviazione in cui il file verrà salvato (ad esempio, `folder/sample.xlsx`).

**Passaggio 2: Conversione del file di lavoro in PDF**  
Invia una richiesta di conversione una volta caricato il file.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*Parametri obbligatori*:

- `name` – nome del file di lavoro caricato (ad esempio, `sample.xlsx`).
- `format` – formato di destinazione (`pdf`).
- `outputPath` – percorso nell'archiviazione dove verrà salvato il file convertito (ad esempio, `folder/result.pdf`).

*Payload della risposta di esempio* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**Passaggio 3: Scaricamento del PDF convertito**  
Recupera il PDF risultante dall'archiviazione.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*Parametri obbligatori*:

- `outputPath` – percorso del PDF generato nel passaggio precedente.

**Riepilogo di esempio di richiesta / risposta**

| Operazione | Metodo HTTP | Endpoint (esempio) | Parametri | Stato di successo |
|-----------|-------------|--------------------|-----------|-------------------|
| Caricamento | PUT | /cells/storage/file/{path} | `path` (posizione nell'archiviazione) | 200 OK |
| Conversione | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| Scaricamento | GET | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Codici di errore comuni**

- **400 Bad Request** – Parametri mancanti o non validi.  
- **401 Unauthorized** – Token di accesso non valido o mancante.  
- **404 Not Found** – Il file o il percorso specificato non esiste.  
- **500 Internal Server Error** – Errore imprevisto del server; riprovare o contattare il supporto.  
---