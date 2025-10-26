---
title: Aspose.Cells Cloud Web API - Somma, conteggio, valore medio, ecc. per colore in foglio di calcolo/Excel
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /it/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: Il Cloud Web Aspose.Cells API (Excel Cloud API) può eseguire calcoli di dati, sommatorie e medie e può anche trovare i valori massimi e minimi in un foglio di calcolo Excel in base al riempimento o al colore del carattere delle celle
weight: 100
kwords: Somma, Conteggio, Valore medio, Valore massimo, Valore minimo, Excel REST API, Operazioni foglio di calcolo, Aspose.Cells, Excel Cloud API
---
API può eseguire calcoli di dati, sommatorie e medie, e può anche trovare i valori massimi e minimi in un foglio di calcolo Excel in base al riempimento o al colore del carattere delle celle.

| Calcola operazione| Descrizione|
|:- |:- |
| Contare| Determina il numero di celle con lo stesso colore.|
| Somma| Calcola il valore totale delle celle con lo stesso colore.|
| Valore massimo| Identifica il valore più alto tra le celle con lo stesso colore.|
| Valore minimo| Trova il valore più basso tra le celle con lo stesso colore.|
|Valore medio| Calcola il valore medio delle celle con lo stesso colore.|

## **Aggregazione Cells per colore API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| Foglio di calcolo| File| FormData| Carica il file del foglio di calcolo.|
| Foglio di lavoro| Corda| Domanda| Specifica il foglio di lavoro.|
| Allineare| Corda| Domanda| Specifica l'intervallo.|
| Operazione| Corda| Domanda| Specificare i metodi di calcolo, tra cui Somma, Conteggio, Media, Min e Max.|
| Posizione del colore| Corda| Domanda| Indica il contenuto da sommare e contare in base al colore di sfondo e/o al colore del carattere.|
| Regione| Corda| Domanda| Impostazione della regione del foglio di calcolo.|
| Password| Corda| Domanda| La password per aprire il file del foglio di calcolo.|

### **Risposta**

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovremmo usare l'Aggregato per colore API?

In un foglio di calcolo, i dati di diverse categorie vengono visualizzati in colori diversi, consentendo operazioni come la somma, il conteggio, il calcolo delle medie e la ricerca dei valori massimi e minimi in base al colore.

## Perché dovresti usare Aggregate by Color API?

- Fornire metodi per l'analisi dei dati relativi al colore.
- Classificare e calcolare i dati in base al colore per fornire dati fondamentali per l'analisi dei dati.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare l'aggregato per colore API con gli SDK

### Aggregato per colore API Specifiche

 IL[Aggregato per colore API Specifiche](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

L'utilizzo dell'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di aggregare i calcoli in base al colore delle celle con solo un breve frammento di codice.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
