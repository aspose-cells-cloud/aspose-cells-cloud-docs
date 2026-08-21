---
title: "Cancella formattazione condizionale"
type: docs
url: /conditional-formattings/clear/
aliases: [/clear-all-condition-formattings/]
keywords: "Aspose.Cells Cloud, REST API, cancella formattazione condizionale, Excel, fogli di lavoro, JWT, v3.2"
description: "Elimina tutte le regole di formattazione condizionale da un foglio di lavoro mediante l'API Aspose.Cells Cloud (v3.2). Scopri la sintassi della richiesta, i parametri obbligatori, le fasi di autenticazione e consulta codici di esempio in vari SDK."
weight: 80
---

Questa API REST cancella tutte le regole di formattazione condizionale da un foglio di lavoro.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Parametri della richiesta

| Nome del parametro | Tipo   | Posizione | Descrizione                                                           |
| ------------------ | ------ | --------- | --------------------------------------------------------------------- |
| **name**           | string | path      | Nome del file del workbook (ad esempio, `Book1.xlsx`).               |
| **sheetName**      | string | path      | Nome del foglio di lavoro dal quale rimuovere la formattazione condizionale. |
| **folder**         | string | query     | _(Opzionale)_ Percorso della cartella nello storage in cui si trova il workbook. |
| **storageName**    | string | query     | _(Opzionale)_ Nome del servizio di storage.                          |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) definisce un'interfaccia di programmazione pubblicamente accessibile e **la Specifica OpenAPI** consente di eseguire direttamente interazioni REST da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Risposte di errore

| Codice HTTP | Motivo                                              | Corpo di esempio                                                    |
| ----------- | --------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore del parametro non valido." }`   |
| **401**     | Non autorizzato – token JWT mancante o non valido.  | `{ "Code":"401", "Message":"Il token di accesso è mancante o non valido." }` |
| **404**     | Non trovato – il workbook o il foglio di lavoro non esistono. | `{ "Code":"404", "Message":"File non trovato." }`                 |
| **500**     | Errore interno del server – errore imprevisto nel server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

## Esempi SDK

L'utilizzo di un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}