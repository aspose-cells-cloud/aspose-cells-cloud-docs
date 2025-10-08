---
title: Aspose.Cells Cloud Web API - Intervallo di scambio nel foglio di calcolo
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: Scambio Rang
type: docs
url: /it/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: Lo strumento "Scambia intervalli per Excel API" fornisce un potente strumento per scambiare due colonne, righe, intervalli o singole celle all'interno di un file Excel. Questo strumento API consente agli utenti di riorganizzare in modo efficiente le proprie tabelle, garantendo che la formattazione originale dei dati venga preservata e che tutte le formule esistenti continuino a funzionare correttamente. Sfruttando questo strumento API, gli utenti possono semplificare le attività di manipolazione dei dati e mantenere l'integrità dei propri fogli di calcolo.
weight: 100
kwords: Excel, Office Cloud, REST, PDF, CSV, Json, Markdown
---
Scambia dati tra due colonne, righe, intervalli o singole celle in un file Excel.

## **Intervallo di cambio API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo.|
|foglio di lavoro1|Corda|Domanda|Specificare il foglio di lavoro che costituisce l'origine dell'area dati di scambio.|
|intervallo1|Corda|Domanda|Specificare l'origine dei dati di scambio.|
|foglio di lavoro2|Corda|Domanda|Specificare il foglio di lavoro che è la destinazione dell'area dati di scambio.|
|intervallo2|Corda|Domanda|Specificare la destinazione per i dati di scambio.|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Il percorso della cartella in cui è archiviata la cartella di lavoro. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome di archiviazione del file di output.|
|regione|Corda|Domanda|Impostazione della regione del foglio di calcolo.|
|password|Corda|Domanda|La password per aprire il file del foglio di calcolo.|

### **Risposta**

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

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovremmo usare lo Swap Range API?

Quando è necessario scambiare dati di intervallo in un foglio di calcolo, è possibile utilizzare questo API.

## Perché dovresti usare Swap Range API?

- Scambia rapidamente i dati di intervallo in un foglio di calcolo Excel.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare l'intervallo di swap API con gli SDK

### Specifiche della gamma Swap API

 IL[Specifiche della gamma Swap API](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di scambiare l'intervallo con il codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
