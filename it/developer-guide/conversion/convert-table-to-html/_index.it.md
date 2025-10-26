---
title: Aspose.Cells Cloud Web API - Converti i dati di una tabella di un foglio di calcolo in un file HTML
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Html fil
linktitle: Converti tabella in HTM
type: docs
url: /it/convert-table-to-html/
keywords: Excel Table to HTML, Spreadsheet Conversion, Aspose.Cells Cloud Web API, REST, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Service
description: Converti facilmente le tabelle dai file di fogli di calcolo locali nel formato HTML utilizzando il nostro API basato su cloud
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, HTML, PDF, CSV, JSON, Markdown, Corrispondenza celle vuote in Excel
---
Converti i dati di un foglio di calcolo locale/tabella Excel in un file HTML.

## **Converti tabella in HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| Foglio di calcolo| File| FormData| Carica il file del foglio di calcolo da convertire.|
| foglio di lavoro| Corda| Domanda| Il nome del foglio di lavoro Spreadsheet/Excel|
| nometabella| Corda| Domanda| Nome della tabella da convertire.|
| Percorso in uscita| Corda| Domanda| (Facoltativo) Il percorso della cartella in cui verrà archiviato il file convertito. Il valore predefinito è null.|
|outStorageName| Corda| Domanda| Nome di archiviazione designato per il file di output.|
| fontPosizione| Corda| Domanda| Specificare font personalizzati per la conversione.|
| regione| Corda| Domanda| Definisci le impostazioni della regione del foglio di calcolo.|
| password| Corda| Domanda| La password richiesta per accedere al file del foglio di calcolo.|

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

## Perché dovresti usare Convert Table to Html API?

- Non è necessario alcuno spazio di archiviazione nel cloud, riducendo così il carico sulle risorse cloud.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare la conversione da tabella a HTML API con gli SDK?

### Converti tabella in HTML API Specifiche

 IL[Converti tabella in HTML API Specifiche](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) descrive un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente dal browser web.

### Utilizzare gli SDK cloud Aspose.Cells

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di convertire i dati di una tabella di un foglio di calcolo in un file HTML con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
