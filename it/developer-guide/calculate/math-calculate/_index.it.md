---
title: Aspose.Cells Cloud Web API - Aggiungi, sottrai, moltiplica, dividi e percentuale su un intervallo di fogli di calcolo/Excel
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: Calcolo matematico
type: docs
url: /it/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: Guida completa per l'utilizzo di Math Calculate API per eseguire calcoli nei fogli di calcolo Excel
weight: 100
kwords: Calcolo matematico, Cloud REST API, Addizione, Meno, Moltiplicazione, Divisione, Percentuale, Office Cloud, Aspose.Cells
---
Gli sviluppatori possono utilizzare questo API per eseguire calcoli di addizione, sottrazione, moltiplicazione, divisione e percentuale su intervalli specificati di fogli di calcolo/Excel.

|**Calcola operazione** | Descrizione|
|:- |:- |
|**Aggiungere** |+ |
|**Meno** |-  |
|**Moltiplicare** |*  |
|**Dividere** |/ |
|**Percentuale** |% |

## **Matematica Calcola API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| Foglio di calcolo| File| FormData| Carica il file del foglio di calcolo per l'elaborazione.|
| operazione| Corda| Domanda| L'operazione matematica da eseguire (addizione, sottrazione, moltiplicazione, divisione e percentuale).|
| valore| Corda| Domanda| Un valore da utilizzare nel calcolo, se applicabile.|
| foglio di lavoro| Corda| Domanda| Nome del foglio di lavoro su cui operare.|
| allineare| Corda| Domanda| L'intervallo di celle da includere nel calcolo.|
| regione| Corda| Domanda|Definisce la regione specifica del foglio di calcolo.|
| password| Corda| Domanda| La password per aprire il file del foglio di calcolo, se protetto.|

### **Risposta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovremmo usare Math Calculate API?

Il calcolo matematico API è adatto per calcoli batch su fogli di calcolo.

## Perché dovresti usare Math Calculate API?

- Eseguire calcoli matematici in batch.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il calcolo matematico API con gli SDK

### Specifiche di Math Calculator API

 IL[Matematica Calcola Specifica](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) definisce un'interfaccia di programmazione accessibile al pubblico, che consente agli sviluppatori di interagire con API direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di eseguire calcoli matematici per cella con solo un breve codice.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
