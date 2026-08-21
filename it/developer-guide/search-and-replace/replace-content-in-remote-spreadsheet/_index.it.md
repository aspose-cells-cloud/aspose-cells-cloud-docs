---
---
title: "Aspose.Cells Cloud Replace Web API – Aggiornamento del testo nei fogli di calcolo remoti"
second_title: "Documento"
ArticleTitle: "Sostituzione di testo in blocco nei file Excel nel cloud – API Trova e Sostituisci"
linktitle: "Sostituisci il contenuto di un foglio di calcolo remoto"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, sostituisci contenuto, foglio di calcolo remoto, API trova e sostituisci, Excel nel cloud, sostituzione di testo in blocco"
description: "Usa l'API Trova e Sostituisci di Aspose.Cells Cloud per aggiornare in blocco il testo nei file Excel remoti. Endpoint HTTPS sicuro, autenticazione OAuth2 ed esempi di SDK pronti all'uso per un'integrazione rapida."
weight: 100
---

Esegui la sostituzione in blocco del testo in file Excel remoti archiviati nel cloud. Trova e aggiorna in modo efficiente stringhe di testo specifiche mediante l'API Trova e Sostituisci di Aspose.Cells Cloud per i fogli di calcolo nel cloud.


## **Sostituisci il contenuto nell'API Foglio di Calcolo Remoto**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della richiesta

| Nome del parametro | Tipo   | Posizione | Descrizione                                                                                                                                              |
|--------------------|--------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **name**           | String | Path      | Nome del file del foglio di calcolo archiviato nel cloud storage da modificare (ad esempio `"report.xlsx"`).                                             |
| **searchText**     | String | Query     | Stringa da individuare all'interno dell'intero foglio di calcolo. La ricerca distingue tra maiuscole e minuscole e si applica a tutti i fogli di lavoro, a meno che non venga limitata da altri parametri. |
| **replaceText**    | String | Query     | Stringa che sostituirà ogni occorrenza di `searchText`.                                                                                                  |
| **folder**         | String | Query     | Percorso della cartella nel cloud storage contenente il foglio di calcolo di origine (ad esempio `"/documents/quarterly/"`).                            |
| **storageName**    | String | Query     | _(Opzionale)_ Nome di un cloud storage personalizzato (ad esempio `"MyS3Bucket"`). Se omesso, verrà utilizzato lo storage predefinito configurato per l'account. |
| **region**         | String | Query     | _(Opzionale)_ Identificatore delle impostazioni locali che può influenzare la codifica dei caratteri e il comportamento della ricerca specifica della lingua (ad esempio `"en-US"`). |
| **password**       | String | Query     | _(Opzionale)_ Password per aprire un foglio di calcolo protetto.                                                                                        |

### Risposta

Una risposta tipica corretta restituisce lo stato dell'operazione e il numero di sostituzioni eseguite:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Codici di errore

- **400 Bad Request** – URI dell'API di Aspose.Cells Cloud non valido.
- **401 Unauthorized** – Token di accesso OAuth 2.0 mancante o non valido.
- **404 Not Found** – Il file foglio di calcolo specificato non può essere accessibile.
- **500 Server Error** – Si è verificato un problema imprevisto lato server durante l'elaborazione della richiesta.

## Quando utilizzare l'API Sostituisci il contenuto in un Foglio di Calcolo Remoto?

- **Aggiornamento in batch dei file nel cloud** – Modifica il contenuto di più file Excel archiviati nel cloud storage, come AWS S3 o Azure Blob.
- **Popolamento dinamico di modelli nel cloud** – Popola modelli di report archiviati nel cloud con dati aggiornati in tempo reale.
- **Sincronizzazione inter-regione dei file** – Mantiene i file Excel coerenti tra diverse regioni geografiche di archiviazione.

## Perché utilizzare l'API Sostituisci il contenuto in un Foglio di Calcolo Remoto?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud fornisce librerie SDK per molti linguaggi di programmazione, riducendo lo sforzo di sviluppo rispetto alla creazione di una soluzione personalizzata.
- **Riduzione dei costi del personale** – Elimina la necessità di personale dedicato per la consolidazione manuale dei documenti.
- **Pagamento in base all’uso** – Nessun investimento iniziale; paghi solo per le chiamate API effettivamente effettuate.
- **Costi di manutenzione nulli** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.
- **Mantiene tutta la formattazione delle celle, le formule e i grafici** – L'operazione conserva il layout e i calcoli originali del foglio di calcolo dopo la sostituzione del testo.

## Come utilizzare l'API Sostituisci il contenuto in un Foglio di Calcolo Remoto con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo migliore per velocizzare lo sviluppo. Gli SDK gestiscono i dettagli sottostanti, consentendoti di implementare semplicemente la sostituzione del contenuto nei fogli di calcolo con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells mediante vari SDK: