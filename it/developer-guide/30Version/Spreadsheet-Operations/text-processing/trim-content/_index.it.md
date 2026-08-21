---
title: "API Aspose.Cells Trim Content – Rimuovi spazi e interruzioni di riga da Excel"
second_title: "Documento"
linktype: "Trim Content"
type: docs
url: /it/spreadsheet-trim-content/
keywords: "Aspose.Cells, API Trim Content, pulizia dati Excel, rimozione spazi da Excel, rimozione interruzioni di riga, pulizia dati fogli di calcolo"
description: "Utilizza l'API PostTrimContent di Aspose.Cells Cloud per rimuovere automaticamente spazi aggiuntivi, interruzioni di riga e caratteri indesiderati dalle celle di Excel. Scopri l'endpoint, il formato della richiesta, il codice di esempio e la gestione degli errori."
weight: 100
---

## **API Web Excel: PostTrimContent**

L'API **PostTrimContent** elabora e riduce il contenuto in un intervallo specificato all'interno di un foglio di calcolo. Rimuove spazi aggiuntivi, interruzioni di riga e altri caratteri non necessari dal contenuto delle celle selezionate, risultando utile per la pulizia delle voci di dati e per garantire una formattazione coerente dei fogli di calcolo.

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.


### **Descrizione della funzione**

- **Efficienza** – Riduce il contenuto solo all'interno dell'intervallo designato, risparmiando tempo e risorse evitando operazioni non necessarie sull'intero foglio di calcolo.
- **Flessibilità** – Consente all'utente di definire esattamente l'intervallo di celle da elaborare, adattandosi a diversi insiemi di dati e requisiti.
- **Integrità dei dati** – Rimuove spazi aggiuntivi e interruzioni di riga, contribuendo a mantenere dati coerenti e affidabili per l'analisi e la generazione di report.
- **Facilità d'uso** – Integrazione semplice con configurazione minima, adatto sia agli sviluppatori che agli utenti finali.

### **Parametri della richiesta**

| Nome parametro     | Tipo  | Posizione | Descrizione                                                                            |
| ------------------ | ----- | --------- | -------------------------------------------------------------------------------------- |
| trimContentOptions | Classe | Corpo     | Opzioni che specificano come deve essere ridotto il contenuto (ad es., intervallo di destinazione, modalità di riduzione). |

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nome file unito]",
    "Filesize" : [dimensione file],
    "FileContent" : "[Base64String]"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                            |
|--------|-----------------------------|------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad es., tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Come utilizzare l'API PostRemoveCharacters con gli SDK

### Specifica dell'API PostRemoveCharacters

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_Ultimo aggiornamento: 2026-03-30_