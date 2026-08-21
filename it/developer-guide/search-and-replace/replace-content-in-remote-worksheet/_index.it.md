---
title: "Aspose.Cells Cloud Replace Web API – Aggiorna il testo in un foglio di calcolo remoto"
second_title: "Documento"
ArticleTitle: "Trova e sostituisci il testo in un foglio di calcolo remoto con l'API Aspose.Cells Cloud"
linktitle: "Sostituisci il contenuto di un foglio di calcolo remoto"
type: docs
url: /it/replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, sostituisci testo, foglio di calcolo remoto, API Excel, foglio di calcolo cloud, trova e sostituisci, API REST"
description: "Sostituisci il testo in un foglio di calcolo specifico di un file Excel archiviato su Aspose Cloud. Supporta cartelle di lavoro protette da password, ricerche sensibili alla regione e aggiornamenti in blocco."
weight: 100
---

Sostituisci un determinato testo all'interno di un foglio di calcolo specifico di file Excel remoti. Aggiorna il contenuto in fogli di calcolo selezionati in modo efficiente utilizzando l'API di Aspose.Cells per la ricerca e sostituzione, per una modifica precisa dei fogli di calcolo.

## **API per la sostituzione del contenuto in un foglio di calcolo remoto**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                                                              |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name           | String | Percorso                       | Il nome del file della cartella di lavoro archiviato nell'archivio cloud da modificare (ad esempio, `"sales_report.xlsx"`, `"budget_2024.xls"`).                          |
| worksheet      | String | Percorso                       | Il nome del foglio di calcolo specifico in cui verrà eseguita l'operazione di ricerca e sostituzione (ad esempio, `"Q1_Sales"`, `"Sheet1"`).                               |
| searchText     | String | Query                      | La stringa di testo da cercare all'interno del foglio di calcolo specificato. La ricerca si applica a tutte le celle del foglio di calcolo, a meno che non venga ulteriormente limitata. |
| replaceText    | String | Query                      | La stringa di testo che sostituirà tutte le occorrenze di `searchText` trovate all'interno del foglio di calcolo specificato.                                              |
| folder         | String | Query                      | Il percorso della cartella nell'archivio cloud in cui si trova la cartella di lavoro di origine (ad esempio, `"/reports/monthly/"`, `"/finance/"`).                       |
| storageName    | String | Query                      | _(Facoltativo)_ Il nome dell'archivio cloud personalizzato (ad esempio, `"CorporateS3"`, `"AzureArchive"`). Se omesso, verrà utilizzato l'archivio cloud predefinito del tuo account. |
| region         | String | Query                      | _(Facoltativo)_ Imposta la localizzazione per la gestione del testo, che potrebbe influenzare la codifica dei caratteri e il comportamento della ricerca specifico della lingua all'interno del foglio di calcolo (ad esempio, `"en-GB"`, `"es-ES"`). |
| password       | String | Query                      | _(Facoltativo)_ Se la cartella di lavoro è protetta da password, fornisci la password per aprirla e modificarla.                                                          |

**Esempio di richiesta (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/sales_report.xlsx/worksheets/Sheet1/replace/content?searchText=OldValue&replaceText=NewValue&folder=/reports" \
     -H "Authorization: Bearer {access_token}"
```

### **Risposta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### **Codici di errore**

| Codice | Descrizione                              | Quando si verifica                                                   |
|--------|------------------------------------------|-----------------------------------------------------------------------|
| 400    | Richiesta non valida                     | L'URI della richiesta è malformato o mancano parametri obbligatori. |
| 401    | Non autorizzato                          | Il token di accesso è mancante, non valido o le credenziali del client sono errate. |
| 404    | Non trovato                              | La cartella di lavoro o il foglio di calcolo specificato non può essere trovato. |
| 500    | Errore interno del server                | Si è verificato un errore imprevisto durante l'elaborazione della richiesta. |

## Dove dovremmo utilizzare l'API per la sostituzione del contenuto del foglio di calcolo in un foglio di calcolo remoto?

- **Aggiornamento batch di file cloud**: Modifica il contenuto di più file Excel archiviati in archiviazione cloud come AWS S3 e Azure Blob.
- **Popolamento dinamico di modelli cloud**: Popola in blocco dati dinamici per modelli di report archiviati nel cloud.
- **Sincronizzazione inter-regionale dei file**: Sincronizza la coerenza del contenuto di file Excel in archiviazione cloud tra diverse regioni geografiche.

## Perché dovresti utilizzare l'API per la sostituzione del contenuto del foglio di calcolo in un foglio di calcolo remoto?

- **Facile da usare per gli sviluppatori**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e disponendo di una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering dei grafici, questo riduce notevolmente il carico di lavoro di sviluppo.
- **Riduzione dei costi del personale**: Diminuisce la necessità di personale dedicato alla consulenza dei documenti.
- **Pay-per-use (pagamento in base all'uso)**: Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione zero**: Nessuna necessità di mantenere server, aggiornare software o gestire problemi di compatibilità.

## Come utilizzare l'API per la sostituzione del contenuto del foglio di calcolo in un foglio di calcolo remoto con gli SDK

### Specifica OpenAPI

La [Specifica OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo migliore per velocizzare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendoti di implementare semplicemente la sostituzione del contenuto del foglio di calcolo in spreadsheet per celle con un codice minimo.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come interagire con i servizi web Aspose.Cells utilizzando vari SDK: