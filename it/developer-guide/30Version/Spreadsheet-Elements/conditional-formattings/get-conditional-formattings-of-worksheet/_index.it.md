---
title: "Ottenere le regole di formattazione condizionale"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, REST API, Excel, Formattazione condizionale, Foglio di lavoro, API di formattazione condizionale"
description: "Recupera tutte le regole di formattazione condizionale applicate a un foglio di lavoro utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, i passaggi di autenticazione, i parametri, esempi concisi di risposta e la gestione degli errori."
weight: 20
---

Questa API REST recupera le regole di formattazione condizionale applicate a un foglio di lavoro.

## Sicurezza e autenticazione
Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                                      |
| -------------- | ------ | --------- | ------------------------------------------------ |
| name           | string | path      | Il nome del file Excel.                          |
| sheetName      | string | path      | Il nome del foglio di lavoro.                    |
| folder         | string | query     | Il percorso della cartella in cui è memorizzato il file. |
| storageName    | string | query     | Il nome del servizio di archiviazione (opzionale). |

### Risposte di errore

| Codice HTTP | Motivo                                                    | Corpo di esempio                                                    |
| ----------- | --------------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Richiesta non valida – parametri mancanti o non validi.   | `{ "Code":"400", "Message":"Valore di parametro non valido." }`     |
| **401**     | Non autorizzato – token JWT mancante o non valido.        | `{ "Code":"401", "Message":"Il token di accesso è mancante o non valido." }` |
| **404**     | Non trovato – cartella di lavoro o foglio di lavoro inesistente. | `{ "Code":"404", "Message":"File non trovato." }`                   |
| **500**     | Errore interno del server – errore imprevisto nel server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

La <a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_L'esempio precedente mostra solo i campi più rilevanti per mantenere il payload conciso._

**Parametri di risposta**

| Parametro                                    | Tipo    | Descrizione                                                   |
|----------------------------------------------|---------|---------------------------------------------------------------|
| Status                                       | string  | Stato del risultato della richiesta (ad esempio, **OK**).     |
| ConditionalFormattings                       | object  | Contenitore per i dati di formattazione condizionale.         |
| ConditionalFormattings.Count                 | integer | Numero di regole di formattazione condizionale restituite.    |
| ConditionalFormattings.ConditionalFormattingList | array   | Elenco di oggetti di formattazione condizionale.              |
| ConditionalFormattingList[].sqref            | string  | Intervallo di celle a cui si applica la formattazione (ad esempio, **A1:B10**). |
| ConditionalFormattingList[].FormatConditions | array   | Raccolta di oggetti di condizione di formattazione per l'intervallo. |
| FormatConditions[].Priority                  | integer | Priorità di valutazione della condizione.                     |
| FormatConditions[].Type                      | string  | Tipo di condizione (ad esempio, **CellValue**).              |
| FormatConditions[].Operator                  | string  | Operatore utilizzato per la condizione (ad esempio, **GreaterThan**). |
| FormatConditions[].Formula1                  | string  | Prima formula o valore per la condizione.                     |
| FormatConditions[].Style                     | object  | Stile applicato quando la condizione è soddisfatta.           |
| Style.Font.Color                             | object  | Definizione colore RGBA per il carattere.                     |
| Style.Font.IsBold                            | boolean | Indica se il carattere è in grassetto.                        |

**Codici di stato HTTP**

| Codice | Significato               | Descrizione                                                  |
|--------|---------------------------|--------------------------------------------------------------|
| 200    | OK                        | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida      | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato           | Token JWT non valido o mancante.                             |
| 413    | Payload troppo grande     | Il file caricato supera il limite di dimensione.             |
| 500    | Errore interno del server | Errore imprevisto nel server.                                |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}
---