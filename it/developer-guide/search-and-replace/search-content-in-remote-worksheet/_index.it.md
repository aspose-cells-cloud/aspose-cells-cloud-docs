---
title: "Aspose.Cells Cloud Excel Text Search Web API – Trova testo nel foglio di calcolo remoto"
second_title: "Documento"
ArticleTitle: "Cerca testo in un foglio di calcolo Excel remoto – Trova dati specifici"
linktitle: "Cerca contenuto nel foglio di calcolo remoto"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Aspose Cells, Excel API, ricerca testo, foglio di calcolo remoto"
description: "Cerca testo, numeri o formule in un foglio di calcolo Excel remoto utilizzando l'API Aspose.Cells Cloud. Supporta ricerche che non distinguono tra maiuscole e minuscole e file protetti da password."
weight: 100
---

## **Cerca contenuto nel foglio di calcolo remoto**

Cerca in modo programmatico un testo specifico all'interno di qualsiasi foglio di calcolo Excel utilizzando l'API Aspose.Cells Cloud. Il servizio è in grado di individuare testo, numeri o formule in file remoti memorizzati nello storage cloud, abilitando flussi di lavoro automatizzati per l'individuazione di dati, l'analisi dei contenuti e il controllo dei fogli di calcolo.

### **Web API**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta**

| Nome parametro | Tipo    | Percorso/Query String/Corpo HTTP | Descrizione                                                                                       |
| -------------- | ------- | -------------------------------- | ------------------------------------------------------------------------------------------------- |
| name           | String  | Percorso                         | **Obbligatorio.** Il nome del file del workbook target (ad esempio, `annual_report.xlsx`).       |
| worksheet      | String  | Percorso                         | **Obbligatorio.** Il foglio di calcolo all'interno del workbook in cui viene eseguita la ricerca. |
| searchText     | String  | Query                            | **Obbligatorio.** La stringa esatta o il numero da individuare.                                   |
| ignoreCase     | Boolean | Query                            | **Facoltativo.** Se `true`, la ricerca non distingue tra maiuscole e minuscole. Default: `false`. |
| folder         | String  | Query                            | **Facoltativo.** Percorso della cartella contenente il workbook. Se omesso, viene usata la root.  |
| storageName    | String  | Query                            | **Facoltativo.** Nome di uno storage cloud configurato personalmente. Se omesso, viene usato lo storage predefinito. |
| region         | String  | Query                            | **Facoltativo.** Impostazione locale (ad esempio, `it-IT`) che potrebbe influenzare il confronto tra testi. |
| password       | String  | Query                            | **Facoltativo.** Password per un workbook protetto. Omettere se il file non è crittografato.      |

### **Risposta**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Totale",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Totale",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Array di corrispondenze. Ogni elemento contiene l'indirizzo della cella (`cellName`), la stringa corrispondente (`text`) e il numero di occorrenze in quella cella (`occurrences`).
- **code** – Codice di stato HTTP restituito dal servizio.
- **status** – Descrizione testuale del risultato.

### **Codici di errore**

- **400 Bad Request** – URI API non valido o parametri malformati.
- **401 Unauthorized** – Token OAuth 2.0 mancante o non valido.
- **404 Not Found** – Impossibile individuare il workbook o il foglio di calcolo.
- **500 Server Error** – Si è verificata una condizione imprevista durante l'elaborazione della richiesta.

## Dove dovremmo utilizzare la funzione di ricerca del contenuto all'interno del foglio di calcolo dell'API Spreadsheet?

- **Audit di conformità del workbook:** individua rapidamente termini sensibili (ad esempio, “Riservato”) in tutto il file.
- **Associazione di dati tra fogli:** trova un numero di progetto o un nome cliente che appare su più fogli.
- **Verifica dei modelli:** dopo la generazione di report, conferma che i segnaposto come `{{Date}}` siano stati sostituiti.
- **Estrazione di dati storici:** cerca codici di eventi specifici in fogli di calcolo legacy per comprendere la logica aziendale passata.

## Perché dovresti utilizzare la funzione di ricerca del contenuto all'interno del foglio di calcolo dell'API Spreadsheet?

- **Facile da usare per gli sviluppatori:** SDK per molti linguaggi accelerano lo sviluppo e sono completamente documentati.
- **Riduzione dei costi del personale:** riduce la necessità di personale dedicato alla raccolta manuale di dati.
- **Pagamento in base all'uso:** paghi solo per le chiamate API effettivamente effettuate.
- **Nessuna manutenzione richiesta:** nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.
- **Preserva la formattazione complessa di Excel** quando esporti i risultati in PDF o altri formati.

## Come utilizzare la ricerca di link rotti all'interno del foglio di calcolo dell'API Spreadsheet con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono interazioni REST direttamente da un browser web.

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo migliore per velocizzare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendoti di implementare semplicemente la ricerca di contenuti all'interno del foglio di calcolo per celle con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK Aspose.Cells Cloud.