---
title: "Aggiungi un criterio personalizzato in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Aggiungi filtro personalizzato"
type: docs
url: /it/autofilter/add-custom-filter/
aliases: [/it/filter-a-list-with-a-custom-criteria/,/it/autofilter/add-a-custom-filter/]
keywords: "Excel, filtro personalizzato, Aspose.Cells Cloud, API REST, autofiltro, foglio di calcolo, criteri personalizzati"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per aggiungere un filtro personalizzato a un foglio di calcolo Excel. Include i dettagli della richiesta, un esempio cURL e frammenti di codice SDK per diversi linguaggi di programmazione."
weight: 65
ArticleTitle: "Aggiungi un criterio personalizzato in un foglio di calcolo Excel – Aspose.Cells Cloud API"
---

Questa API REST filtra un elenco utilizzando un **criterio personalizzato**.

## API PutWorksheetCustomFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta:

| Nome parametro | Tipo    | Posizione                     | Descrizione                                                                 |
|----------------|---------|------------------------------|-----------------------------------------------------------------------------|
| name           | string  | path                         | Nome del file Excel.                                                     |
| sheetName      | string  | path                         | Nome del foglio di calcolo contenente i dati da filtrare.               |
| range          | string  | query                        | Intervallo di celle a cui verrà applicato il filtro (ad esempio, `A1:B1`).             |
| fieldIndex     | integer | query                        | Indice in base zero della colonna su cui viene applicato il filtro.             |
| operatorType1  | string  | query                        | Primo operatore di confronto (ad esempio, `LessOrEqual`, `Equal`).                  |
| criteria1      | string  | query                        | Primo valore o espressione di filtro.                                          |
| isAnd          | boolean | query                        | Se `true`, combina i due criteri con **AND**; altrimenti **OR**.       |
| operatorType2  | string  | query                        | Secondo operatore di confronto (opzionale).                                     |
| criteria2      | string  | query                        | Secondo valore o espressione di filtro (opzionale).                              |
| matchBlanks    | boolean | query                        | Se `true`, include le celle vuote nei risultati del filtro.                    |
| refresh        | boolean | query                        | Se `true`, forza il ricaricamento del foglio di calcolo dopo l'applicazione del filtro.      |
| folder         | string  | query                        | Percorso della cartella nello storage in cui si trova il file.                          |
| storageName    | string  | query                        | Nome del servizio di storage.                                                |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                     | Descrizione                                      |
|--------|----------------------------------|--------------------------------------------------|
| 200    | OK                               | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida             | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato                  | Token JWT non valido o mancante. |
| 413    | Payload troppo grande            | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server        | Errore imprevisto del server. |

## Come utilizzare l'API PutWorksheetCustomFilter con gli SDK

### Specifica dell'API PutWorksheetCustomFilter

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello in modo che tu possa concentrarti sulla logica del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Per altre operazioni di AutoFilter, come l'aggiunta di un filtro standard o di un filtro per data, consulta le pagine di documentazione correlate all'interno della sezione AutoFilter.