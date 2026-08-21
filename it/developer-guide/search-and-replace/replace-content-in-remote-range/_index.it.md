---
title: "Aspose.Cells Cloud Replace Web API – Aggiornamento del testo in un intervallo remoto di un foglio di calcolo"
second_title: "Documento"
ArticleTitle: "Sostituzione bulk del testo negli intervalli dei file Excel su cloud – API Trova e Sostituisci"
linktype: "Sostituisci il contenuto di un intervallo remoto"
type: docs
url: /it/replace-content-in-remote-range/
keywords: "sostituire testo intervallo excel remoto, Aspose.Cells Cloud API, trova e sostituisci Excel, modifica foglio di calcolo su cloud, aggiornamento file Excel remoto"
description: "Usa Aspose.Cells Cloud per cercare e sostituire testo in un intervallo specifico di un file Excel remoto. Supporta l'autenticazione, la gestione degli errori e SDK multipli."
weight: 100
---

Esegui la sostituzione bulk del testo in file Excel memorizzati su cloud. Cerca e aggiorna stringhe di testo specifiche all'interno di intervalli selezionati in modo efficiente utilizzando l'API Trova e Sostituisci di Aspose.Cells Cloud.

## **Sostituisci il contenuto dell’intervallo remoto tramite API**

### API Web

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                                                                                                       |
| :------------- | :----- | :------------------------------------ | :------------------------------------------------------------------------------------------------ ----------------------------------------------------------------------------------------------- |
| name           | String | Percorso                              | Nome del file del workbook memorizzato nello storage su cloud da modificare (ad es. `"report.xlsx"`).                                                            |
| searchText     | String | Query                                 | Stringa di testo da cercare all'interno del foglio di lavoro e dell'area cellulare specificati. Supporta la corrispondenza esatta del testo.                     |
| replaceText    | String | Query                                 | Stringa di testo che sostituirà tutte le occorrenze di `searchText` nell'intervallo specificato.                                                                |
| worksheet      | String | Percorso                              | Nome del foglio di lavoro in cui verrà eseguita l'operazione di trova e sostituisci.                                                                           |
| cellArea       | String | Percorso                              | Intervallo specifico di celle (ad es. `"A1:D20"`) in cui verrà effettuata la ricerca e la sostituzione del testo.                                                |
| folder         | String | Query                                 | Percorso della cartella nello storage su cloud in cui si trova il workbook di origine.                                                                         |
| storageName    | String | Query                                 | _(Opzionale)_ Nome dello storage su cloud in cui risiede il workbook. Se omesso, viene utilizzato lo storage predefinito.                                      |
| region         | String | Query                                 | _(Opzionale)_ Imposta la localizzazione per la gestione del testo, che può influenzare la distinzione tra maiuscole/minuscole e la codifica dei caratteri durante le ricerche (ad es. `"en-US"`, `"tr-TR"`). |
| password       | String | Query                                 | _(Opzionale)_ Se il workbook è protetto da password, fornire la password per aprirlo e modificarlo.                                                             |

### **Risposta**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

Una chiamata riuscita restituisce il seguente payload JSON concreto:

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### Codici di errore

| Codice | Messaggio       | Quando si verifica                                     |
| ------ | --------------- | ------------------------------------------------------ |
| 400    | Bad Request     | L'URI della richiesta o i parametri sono malformati.  |
| 401    | Unauthorized    | Token di autenticazione mancante o non valido.        |
| 404    | Not Found       | Il workbook specificato non può essere trovato o accesso. |
| 500    | Server Error    | Errore interno del server durante l'elaborazione del workbook. |

## Dove dovresti utilizzare l'API Sostituisci contenuto dell'intervallo in un foglio di calcolo remoto?

- **Aggiornamento batch di file su cloud**: Modifica il contenuto di più file Excel memorizzati su storage su cloud come AWS S3 o Azure Blob.
- **Popolamento dinamico di template su cloud**: Popola in batch dati dinamici per template di report memorizzati sul cloud.
- **Sincronizzazione cross-region dei file**: Sincronizza la coerenza dei contenuti dei file Excel su cloud tra diverse regioni geografiche.

## Perché dovresti utilizzare l'API Sostituisci contenuto dell'intervallo in un foglio di calcolo remoto?

- **Facile da usare per sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e una documentazione completa. Rispetto alla creazione di soluzioni personalizzate, riduce significativamente il carico di lavoro di sviluppo.
- **Riduzione dei costi del personale**: Diminuisce la necessità di figure dedicate alla gestione della compilazione dei documenti.
- **Pay-per-use**: Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione nulli**: Nessuna necessità di mantenere server, aggiornare software o gestire problemi di compatibilità.
- **Preserva la formattazione complessa di Excel** in un formato PDF universalmente accessibile.

## Come utilizzare l'API Sostituisci contenuto dell'intervallo in un foglio di calcolo remoto con gli SDK

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) definiscono un'interfaccia di programmazione accessibile pubblicamente e permettono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo degli SDK rappresenta il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare semplicemente la sostituzione del contenuto nei fogli di calcolo con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}