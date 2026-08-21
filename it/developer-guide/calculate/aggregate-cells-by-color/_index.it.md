---
title: "Aspose.Cells Cloud Web API – Somma e Conteggio per Colore in Excel"
second_title: "Documento"
ArticleTitle: "Somma, Conteggio, Media, Valore Massimo e Minimo per Colore in Foglio Elettronico/Excel"
LinkTitle: "Aggrega Celle per Colore"
type: docs
url: /it/aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregate, color, sum, count, average, min, max"
description: "Aggrega le celle di Excel in base al colore di sfondo o al colore del carattere (somma, conteggio, media, min, max) utilizzando l'API Aspose.Cells Cloud. Scopri l'endpoint, i parametri, l'autenticazione e gli esempi di SDK."
weight: 100
---

## Panoramica

L'API consente di eseguire calcoli sui dati in base al **colore** delle celle. Può effettuare somme, conteggi, medie e individuare i valori massimi e minimi in un foglio elettronico Excel in base al colore di riempimento o al colore del carattere delle celle.

| Operazione di Calcolo | Descrizione                                                  |
| :-------------------- | :----------------------------------------------------------- |
| Count (Conteggio)     | Determina il numero di celle aventi lo stesso colore.       |
| Sum (Somma)           | Calcola il valore totale delle celle aventi lo stesso colore. |
| Max Value (Valore Massimo) | Identifica il valore più alto tra le celle dello stesso colore. |
| Min Value (Valore Minimo) | Individua il valore più basso tra le celle dello stesso colore. |
| Average Value (Valore Medio) | Calcola il valore medio delle celle dello stesso colore.   |

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Sicurezza e Autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della Richiesta

| Nome Parametro | Tipo   | Posizione | Descrizione                                                    |
| :------------- | :----- | :-------- | :------------------------------------------------------------- |
| Spreadsheet    | File   | FormData  | Il workbook Excel da elaborare.                               |
| Worksheet      | String | Query     | Nome del foglio di lavoro contenente l'intervallo.            |
| Range          | String | Query     | Intervallo in stile A‑1 (es. `A1:B10`).                       |
| Operation      | String | Query     | Metodo di calcolo – `Sum`, `Count`, `Average`, `Min` o `Max`. |
| ColorPosition  | String | Query     | Determina quale colore valutare – `Background`, `Font`.      |
| Region         | String | Query     | Impostazione della regione del foglio elettronico (es. `us-east-1`). |
| Password       | String | Query     | Password per aprire un workbook protetto (opzionale).         |

#### Enumerazioni

- **ColorPosition**

  | Valore     | Significato                         |
  | :--------- | :---------------------------------- |
  | Background | Utilizza il colore di riempimento della cella. |
  | Font       | Utilizza il colore del carattere della cella. |

**Esempio di richiesta multipart/form‑data**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Risposta

Lo schema seguente descrive l'oggetto di risposta. Segue un esempio concreto.

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
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Esempio di risposta (valori reali)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**Codici di Stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Bad Request           | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Unauthorized          | Token JWT non valido o mancante.                                  |
| 413    | Payload Too Large     | Il file caricato supera il limite di dimensione.                  |
| 500    | Internal Server Error | Errore imprevisto nel server.                                     |

## Dove utilizzare l'API Aggregate by Color?

In un foglio elettronico, i dati appartenenti a diverse categorie sono spesso codificati a colori. Questa API consente di effettuare somme, conteggi, medie o individuare i valori minimi e massimi per ogni gruppo di colore, semplificando l'analisi dei dati basata sul colore.

## Perché utilizzare l'API Aggregate by Color?

L'API fornisce un modo rapido e affidabile per eseguire calcoli basati sul colore, senza dover scrivere logica di parsing personalizzata. Si integra perfettamente con gli SDK Aspose.Cells Cloud, consentendo agli sviluppatori di implementare l'aggregazione per colore in pochissime righe di codice.

## Come utilizzare l'API Aggregate by Color con gli SDK

### Specifica dell'API Aggregate by Color

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">Specifica dell'API Aggregate by Color</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo dell'SDK rappresenta il metodo più veloce per lo sviluppo, poiché astrae i dettagli di basso livello, consentendo di aggregare i calcoli per colore della cella con pochissime righe di codice.  
Consultare il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells Cloud utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**Note:**

- Quando si lavora con workbook protetti, includere il parametro di query opzionale `Password`; altrimenti la richiesta fallirà con un errore 401.
- La dimensione massima della richiesta per il file `Spreadsheet` è di 100 MB. Se è necessario elaborare file più grandi, considerare di caricare prima il workbook nello storage Aspose Cloud e farvi riferimento tramite il parametro `Path` (non mostrato qui).