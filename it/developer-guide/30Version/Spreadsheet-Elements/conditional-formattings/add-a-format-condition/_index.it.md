---
title: "Aggiungi Condizione di Formato"
type: docs
url: /conditional-formattings/add-format-condition/
aliases: [/add-a-format-condition/]
keywords: "Aspose.Cells Cloud, API Formato Condizionale, Aggiungi Condizione di Formato, API REST Excel, API Cells"
description: "Scopri come aggiungere una condizione di formato a un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include la sintassi della richiesta, i parametri, un esempio sicuro con cURL e frammenti di codice SDK."
ArticleTitle: "Aggiungi Condizione di Formato – Documentazione API Aspose.Cells Cloud"
weight: 50
---

Questa REST API aggiunge una condizione di formato a un foglio di calcolo.

## Sicurezza e Autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione | Descrizione                                                                 |
| -------------- | ------- | --------- | --------------------------------------------------------------------------- |
| name           | string  | path      | Il nome del file Excel (cartella di lavoro).                               |
| sheetName      | string  | path      | Il nome del foglio di calcolo contenente l'intervallo da formattare.       |
| index          | integer | path      | L'indice in base zero della condizione di formato da aggiungere o sostituire. |
| cellArea       | string  | query     | L'intervallo di celle (es. `A1:C3`) a cui si applica la condizione.        |
| type           | string  | query     | Il tipo di condizione (es. `Expression`, `CellValue`).                     |
| operatorType   | string  | query     | L'operatore della condizione (es. `Between`, `Equal`).                     |
| formula1       | string  | query     | La prima formula o valore utilizzata dalla condizione.                     |
| formula2       | string  | query     | La seconda formula o valore (richiesto per alcuni operatori come `Between`). |
| folder         | string  | query     | La cartella nello storage in cui si trova il file Excel.                   |
| storageName    | string  | query     | Il nome del servizio di storage (es. `Default`).                           |

### Risposte di errore

| Codice HTTP | Motivo                                                | Esempio di corpo                                                  |
| ----------- | ----------------------------------------------------- | ----------------------------------------------------------------- |
| **400**     | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore di parametro non valido." }`  |
| **401**     | Non autorizzato – token JWT mancante o non valido.    | `{ "Code":"401", "Message":"Token di accesso mancante o non valido." }` |
| **404**     | Non trovato – il file Excel o il foglio di calcolo non esistono. | `{ "Code":"404", "Message":"File non trovato." }`               |
| **500**     | Errore interno del server – errore imprevisto nel server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

### Risposta di successo

| Codice HTTP | Motivo                                                  | Esempio di corpo                           |
| ----------- | ------------------------------------------------------- | ------------------------------------------ |
| **200**     | OK – condizione aggiunta o aggiornata correttamente.    | `{ "Code": "200", "Status": "OK" }`        |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) definiscono un'interfaccia di programmazione pubblicamente accessibile e permettono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare **cURL** per richiamare l'API Aspose.Cells. L'esempio seguente mostra una richiesta completa, inclusivo di un corpo JSON vuoto.

### Esempio cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}