---
---
title: "Aspose.Cells Cloud – API di calcolo matematico (Add, Subtract, Multiply, Divide, %)"
second_title: "Documento"
ArticleTitle: "Add, Subtract, Multiply, Divide e Percentuale nei fogli di calcolo/Excel"
linktitle: "Calcolo matematico"
type: docs
url: /math-calculate/
keywords: "API di calcolo matematico, Aspose.Cells Cloud, calcoli Excel, addizione, sottrazione, moltiplicazione, divisione, percentuale, elaborazione in blocco di file Excel, API REST"
description: "Scopri come utilizzare l'API di calcolo matematico di Aspose.Cells Cloud per applicare in blocco operazioni di addizione, sottrazione, moltiplicazione, divisione o percentuale su intervalli di Excel. Include il formato della richiesta, codice di esempio e gestione degli errori."
weight: 100
---

## **Introduzione**: Calcolo rapido nei fogli di calcolo – Formule per addizione, moltiplicazione, sottrazione, divisione e percentuale in un’unica API in esecuzione

_Esegui calcoli in blocco su intere colonne, righe o tabelle senza scrivere alcuna formula._

- **Operazioni matematiche di base**: aggiungi, sottrai, moltiplica o dividi ogni cella di un intervallo per qualsiasi numero
- **Percentuali**: aumenta/riduci di una percentuale, oppure calcola la percentuale di un numero (es. +15%, -8%, 20% di…)
- **Elaborazione in blocco**: applica a migliaia di celle istantaneamente—nessuna trascinamento di riempimento, nessuna formula matriciale, nessun VBA

| **Operazione di calcolo** | Descrizione |
| :------------------------ | :---------- |
| **Add** (Addizione)       | +           |
| **Subtract** (Sottrazione)| -           |
| **Multiply** (Moltiplicazione) | \*      |
| **Divide** (Divisione)    | /           |
| **Percentage** (Percentuale) | %        |

## **API di calcolo matematico**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                              |
| :------------- | :----- | :----------------------------------- | :--------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                             | Carica il file del foglio di calcolo da elaborare.                                       |
| operation      | String | Query                                | L’operazione matematica da eseguire (Add, Subtract, Multiply, Divide, Percentage).      |
| value          | String | Query                                | Un valore da utilizzare nel calcolo, se applicabile.                                     |
| worksheet      | String | Query                                | Il nome del foglio di calcolo su cui operare.                                            |
| range          | String | Query                                | L'intervallo di celle da includere nel calcolo.                                          |
| region         | String | Query                                | L'impostazione della regione del foglio di calcolo.                                      |
| password       | String | Query                                | La password per aprire il file del foglio di calcolo, se protetto.                       |

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

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                   |

## Dove dovresti utilizzare l’API di calcolo matematico?

- **Finanza**: aggiungi l’13% di IVA a un’intera colonna di prezzi di acquisto.
- **Inventario**: moltiplica la colonna dei kg per 2,2046 per convertire in blocco in libbre.
- **Retribuzioni**: aggiungi un bonus fisso di 1.000 alla colonna dei bonus per tutto lo staff.
- **Conversione valuta estera (FX)**: dividi la colonna delle vendite per il tasso di cambio corrente per ottenere importi in USD.
- **Valutazione**: sottrai 5 punti da ogni voto degli studenti come penalità per assenteismo.
- **E-commerce**: applica uno sconto promozionale del 15% riducendo in un solo click i prezzi dei prodotti.

## Perché dovresti utilizzare l’API di calcolo matematico?

- **Calcoli Excel veloci** – completa i report di fine mese in pochi secondi.
- **Aumento percentuale in blocco su Excel** – aggiorna prezzi, previsioni, commissioni in un solo click.
- **Aggiungi lo stesso numero a tutta una colonna** – inventario, conversione valuta, conversione unità.
- **Excel senza formule** – gli utenti non tecnici apprezzano la semplicità.
- Lo sviluppo può essere completato rapidamente sfruttando gli SDK esistenti.

**Note**  
La dimensione massima del file supportata è 200 MB. Il parametro `range` deve essere un indirizzo Excel valido (es. A1:B10). Fogli di calcolo molto grandi potrebbero richiedere un tempo di elaborazione aggiuntivo.

## Come utilizzare l’API di calcolo matematico con gli SDK

### Specifica dell’API di calcolo matematico

La [Specifiche dell’API di calcolo matematico](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) definisce un'interfaccia di programmazione accessibile pubblicamente, consentendo agli sviluppatori di interagire direttamente con l’API da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare gli SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli di basso livello, permettendoti di eseguire calcoli matematici per cella con pochissimo codice.  
Consulta gli [SDK di Aspose.Cells Cloud su GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK disponibili.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}