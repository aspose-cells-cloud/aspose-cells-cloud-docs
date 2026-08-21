---
title: "Aggiungi Testo a Excel: Inserisci Dati in Modo Efficienti con l'API Web per Fogli di Calcolo"
second_title: "Documento"
linktitle: "Aggiungi Testo"
type: docs
url: /it/excel-add-text/
keywords: "Excel, Aspose.Cells, Aggiungi Testo, API Foglio di Calcolo, API REST, Office Cloud, Inserimento Testo, API Excel"
description: "Aggiunge testo in una posizione specifica all'interno di un foglio di calcolo Excel tramite l'API Aspose.Cells Cloud."
weight: 100
---

Aggiunge contenuto di testo in una posizione specifica all'interno di un foglio di calcolo. Richiede un oggetto che definisce il testo da aggiungere e la posizione in cui inserirlo.

## **API Excel: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Sicurezza e Autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Descrizione della Funzione**

Questo metodo aggiunge in modo sicuro nuovo testo alle celle specificate, supportando diversi modi di inserimento e la gestione dei formati.

- **Aggiungi testo all'inizio delle celle selezionate**  
  Antepone il testo a tutte le celle selezionate, garantendo coerenza nell'inserimento dei dati. Ideale per aggiungere identificativi o etichette comuni, come codici prodotto, categorie o prefissi.

- **Inserisci caratteri prima o dopo un testo specifico**  
  Posiziona caratteri prima o dopo il testo target nelle celle selezionate, permettendo di creare facilmente contenuti strutturati e organizzati.

- **Aggiungi lo stesso testo alla fine di ogni cella selezionata**  
  Aggiunge testo identico alla fine di più celle in un’unica operazione, semplificando l’inserimento dei dati e garantendo un aspetto uniforme.

- **Inserisci testo prima o dopo un numero specifico di caratteri**  
  Inserisce testo dopo un numero definito di caratteri a partire dall’inizio o dalla fine di ogni cella nell’intervallo di destinazione. Casi d’uso tipici includono la formattazione di codici, timestamp o delimitatori personalizzati.

### **Parametri della Richiesta**

| Nome Parametro | Tipo  | Posizione | Descrizione                                                                 |
| -------------- | ----- | --------- | --------------------------------------------------------------------------- |
| addTextOptions | Classe | Corpo     | Specifica il contenuto del testo e la posizione in cui aggiungerlo.        |

### **Risposta**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "Contenuto File: stringa_base64_codificata"
}
```

**Codici di Stato HTTP**

| Codice | Significato                 | Descrizione                                                    |
|--------|-----------------------------|----------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta Non Validata      | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non Autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload Troppo Grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore Interno del Server   | Errore imprevisto del server. |

## Come Usare l’API PostAddTextContent con gli SDK

### Specifica dell’API PostAddTextContent

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) definiscono un’interfaccia di programmazione pubblicamente accessibile e permettono di effettuare direttamente interazioni REST dal browser web.

### Usare gli SDK Aspose.Cells Cloud

L’uso di un SDK è il modo più efficiente per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells usando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}