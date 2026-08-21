---
title: "Aspose.Cells Cloud Web API – Estrai testo"
second_title: "Aspose.Cells Cloud – Short-code online"
linktitle: "Estrai testo"
type: docs
url: /it/extract-text/
keywords: "Aspose.Cells Cloud, estrai testo, API Excel, estrazione testo celle, REST API"
description: "Estrai sottostringhe, numeri o caratteri dalle celle Excel utilizzando l'API Aspose.Cells Cloud. Supporta l'estrazione in base al testo precedente/seguito e in base alla posizione, nonché l'output diretto in un nuovo intervallo."
weight: 100
ArticleTitle: "Documentazione API Aspose.Cells Cloud per l'estrazione del testo"
---

Estrae sottostringhe, caratteri o numeri da una cella di un foglio di calcolo in un’altra cella, eliminando la necessità di formule complesse come FIND, MIN, LEFT o RIGHT.

## **API ExtractText**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### I parametri della richiesta dell’API **extractText** sono:

| Nome parametro   | Tipo    | Posizione           | Descrizione                                                                                                                     |
| ---------------- | ------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | File    | FormData           | Carica il file del foglio di calcolo.                                                                                           |
| extractTextType  | String  | Query              | Enum che indica la modalità di estrazione. Valori ammessi: `Before`, `After`, `BeforePosition`, `AfterPosition`.              |
| beforeText       | String  | Query              | Testo che deve comparire **prima** della sottostringa estratta. Utilizzato quando `extractTextType=Before`.                    |
| afterText        | String  | Query              | Testo che deve comparire **dopo** la sottostringa estratta. Utilizzato quando `extractTextType=After`.                         |
| beforePosition   | Integer | Query              | Numero di caratteri da restituire dal lato sinistro della cella. Utilizzato quando `extractTextType=BeforePosition`.          |
| afterPosition    | Integer | Query              | Numero di caratteri da restituire dal lato destro della cella. Utilizzato quando `extractTextType=AfterPosition`.             |
| outPositionRange | String  | Query              | L'intervallo di destinazione (ad es. `Sheet1!A1`) in cui verrà scritto il testo estratto.                                     |
| worksheet        | String  | Query              | Nome del foglio di calcolo contenente la cella di origine.                                                                     |
| range            | String  | Query              | La cella o l'intervallo di origine (ad es. `A1`).                                                                              |
| outPath          | String  | Query _(Opzionale)_ | Percorso della cartella nella memoria in cui verrà salvato il foglio di calcolo risultante. Se omesso, il risultato viene restituito nel corpo della risposta. |
| outStorageName   | String  | Query              | Nome della memoria da utilizzare per il file di output.                                                                        |
| region           | String  | Query              | Impostazione della regione del foglio di calcolo (ad es. `US`, `EU`).                                                          |
| password         | String  | Query              | Password per aprire un foglio di calcolo protetto.                                                                             |

**Esempio di richiesta cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Risposta**

Quando la richiesta ha successo, l’API restituisce un payload JSON contenente il testo estratto e l’indirizzo della cella in cui è stato scritto:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

Se il parametro `outPath` è fornito, la risposta contiene solo un messaggio di stato; il foglio di calcolo viene scritto nella posizione specificata.

**Esempio di risposta quando `outPath` è omesso**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### Codici di errore

- **200 OK** – Estrazione completata con successo.  
- **202 Accepted** – Richiesta accettata per l’elaborazione asincrona.  
- **400 Bad Request** – URI API Aspose.Cells Cloud non valido o parametri obbligatori mancanti.  
- **401 Unauthorized** – Token di accesso, client ID o client secret non validi.  
- **404 Not Found** – Impossibile accedere al file del foglio di calcolo specificato.  
- **500 Server Error** – Si è verificato un errore imprevisto durante l’elaborazione del foglio di calcolo.

## Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare semplicemente l’**Estrazione testo** per le celle con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// Esempio in C# – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Esempio in Java – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// Esempio in PHP – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Esempio in Ruby – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Esempio in Node.js – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Esempio in Python – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Esempio in Perl – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Esempio in Go – estrazione testo (codice omesso per brevità)
```

{{</tab>}}

{{< /tabs >}}