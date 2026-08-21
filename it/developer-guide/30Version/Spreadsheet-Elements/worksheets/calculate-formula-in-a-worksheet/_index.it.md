---
title: "Calcolare una formula in un foglio di lavoro Excel"
second_title: "Documento"
linktype: "Calcola"
type: docs
url: /it/worksheets/calculate-formula/
aliases: [/it/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, calcolo formula, API REST, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Calcola formule in un foglio di lavoro Excel usando l'API REST di Aspose.Cells Cloud. Supporta numerosi SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) con esempi pronti all'uso."
weight: 20
ArticleTitle: "Calcolare una formula in un foglio di lavoro Excel – Documentazione di Aspose.Cells Cloud"
---

Questa API REST restituisce il **valore calcolato di una formula** in un foglio di lavoro. Può essere utilizzata per **valutare direttamente una formula Excel** dalla tua applicazione.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **Parametri della richiesta**

| Nome parametro | Tipo   | Posizione | Descrizione                                             |
| -------------- | ------ | --------- | ------------------------------------------------------- |
| name           | string | path      | Nome del file Excel.                                    |
| sheetName      | string | path      | Nome del foglio di lavoro contenente la formula.        |
| formula        | string | query     | La formula da valutare (es. `SUM(A5:A10)`).             |
| folder         | string | query     | Cartella in cui è memorizzato il documento.             |
| storageName    | string | query     | Nome del servizio di archiviazione (se applicabile).    |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Autenticazione

Tutte le richieste devono includere un valido **token JWT Bearer** nell'header `Authorization`:

```
Authorization: Bearer <your_jwt_token>
```

Puoi ottenere un token seguendo il flusso OAuth 2.0 descritto nella guida all'autenticazione di Aspose.Cells Cloud.

### Possibili codici di stato della risposta

| Codice | Descrizione                                     |
|--------|-------------------------------------------------|
| 200    | Richiesta riuscita; il valore della formula viene restituito. |
| 400    | Richiesta non valida – parametri mancanti o non validi. |
| 401    | Non autorizzato – token JWT non valido o mancante. |
| 404    | Non trovato – il file o il foglio di lavoro specificato non esiste. |
| 500    | Errore interno del server – condizione imprevista sul server. |

Puoi utilizzare lo strumento a riga di comando **cURL** per chiamare facilmente i servizi web di Aspose.Cells Cloud. L'esempio seguente mostra come richiedere il risultato di una formula con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per integrare l'API. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**Vedi anche:**  
- [Ottenere un foglio di lavoro](https://docs.aspose.cloud/cells/it/worksheets/get-worksheet/)  
- [Aggiornare un foglio di lavoro](https://docs.aspose.cloud/cells/it/worksheets/update-worksheet/)  
- [Calcolare tutte le formule](https://docs.aspose.cloud/cells/it/worksheets/calculate-all-formulas/)  
---