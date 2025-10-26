---
title: Aspose.Cells Cloud Webb API - Aggiungi un foglio di lavoro a un foglio di calcolo
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: Aggiungi foglio di lavoro al foglio di calcolo
type: docs
url: /it/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: Cloud Web Aspose.Cells consente agli sviluppatori di aggiungere in modo efficiente un nuovo foglio di lavoro a una cartella di lavoro, garantendo il controllo sul tipo, sulla posizione e sul nome del foglio di lavoro. Questa funzionalità migliora la gestione e la flessibilità delle cartelle di lavoro.
weight: 100
kwords: Excel, Office Cloud, REST, Foglio di calcolo, PDF, CSV, JSON, Markdown, Gestisci fogli di lavoro Excel, Creazione di fogli di calcolo dinamici
---
Aggiungere un foglio di lavoro al foglio di calcolo, specificando il tipo e la posizione del foglio di lavoro.

|**Tipo di foglio di lavoro** | Descrizione|
|:- |:- |
|**VB** | Modulo Visual Basic|
|**Foglio di lavoro** | Foglio di lavoro|
|**Grafico** | Foglio grafico|
|**BIFF4Macro** | Foglio macro BIFF4|
|**Macro Internazionale** | Foglio macro internazionale|
|**Altro** | Foglio macro internazionale|
|**Dialogo** | Foglio di lavoro sul dialogo|

## **Aggiungi foglio di lavoro al foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo.|
|tipo di foglio|Corda|Domanda|Specifica il nome del nuovo foglio di lavoro. Se non specificato, verrà assegnato un nome predefinito.|
|posizione|Intero|Domanda|Specifica la posizione in cui inserire il nuovo foglio di lavoro. Se non specificato, il foglio di lavoro verrà aggiunto alla fine della cartella di lavoro.|
|Nome foglio|Corda|Domanda|Specifica il tipo di foglio di lavoro da aggiungere. Se non specificato, verrà utilizzato un tipo di foglio di lavoro predefinito.|
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

## Dove dovremmo usare Aggiungi foglio di lavoro al foglio di calcolo API?

Quando devi aggiungere un foglio di lavoro a un foglio di calcolo, puoi usare questo API.

## Perché dovresti usare Aggiungi foglio di lavoro al foglio di calcolo API?

- Aggiungere un foglio di lavoro al foglio di calcolo, specificandone il tipo e la posizione.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare Aggiungi foglio di lavoro al foglio di calcolo API con SDK

### Aggiungi foglio di lavoro al foglio di calcolo API Specifiche

 IL[Aggiungi foglio di lavoro al foglio di calcolo API Specifiche](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di aggiungere un foglio di lavoro a un foglio di calcolo con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate API ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
