---
title: "Calcola formula cella – Aspose.Cells Cloud API"
type: docs
url: /it/calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, calcola formula cella, Excel API, REST API, SDK"
description: "Calcola la formula di una cella Excel tramite l'API REST Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempio cURL e frammenti SDK."
ArticleTitle: "Calcola formula cella – Documentazione Aspose.Cells Cloud API"
---

## API REST

Questa API REST calcola la **formula della cella** in un foglio di lavoro Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Sicurezza e autenticazione

Le API Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione parametro (path/query/body) | Descrizione                                                        |
| -------------- | ------ | ------------------------------------- | ------------------------------------------------------------------ |
| name           | string | path                                  | Nome del file Excel (es. `Book1.xlsx`).                            |
| sheetName      | string | path                                  | Nome del foglio di lavoro contenente la cella.                     |
| cellName       | string | path                                  | Indirizzo della cella da calcolare (es. `A1`).                     |
| options        | object | body                                  | Oggetto JSON con opzioni di calcolo (vedi tabella **Oggetto options**). |
| folder         | string | query                                 | Cartella nello storage in cui è ubicato il file.                   |
| storageName    | string | query                                 | Nome dello storage Aspose Cloud.                                   |

#### Oggetto options

| Campo           | Tipo    | Descrizione                                                                     | Default |
| --------------- | ------- | ------------------------------------------------------------------------------- | ------- |
| CalcStackSize   | string  | Dimensione massima dello stack di calcolo.                                      | `"1"`   |
| IgnoreError     | boolean | Se `true`, gli errori di calcolo vengono ignorati e il valore della cella viene impostato su `#N/A`. | `false` |
| Recursive       | boolean | Abilita il calcolo ricorsivo delle celle dipendenti.                            | `false` |
| Precision       | string  | Numero di cifre decimali per i risultati numerici.                              | `"15"`  |
| UseThreading    | boolean | Abilita il calcolo multi‑thread.                                                 | `false` |


### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato).         |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                            |
| 500    | Errore interno del server   | Errore imprevisto nel server.                                               |

## Come utilizzare l'API PostCellCalculate con gli SDK

### Specifica dell'API PostCellCalculate

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL. **Prima ottieni un token JWT** autenticandoti presso l'endpoint `/connect/token` e sostituisci `<jwt token>` con il valore del token.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
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

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello e consente di concentrarsi sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
---