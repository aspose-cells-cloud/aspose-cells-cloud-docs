---
title: "Aggiornamento dello stile per la tabella pivot"
second_title: "Documento"
linktitle: "Formatta tutto"
type: docs
url: /it/pivot-tables/format-all/
aliases: [  /it/update-style-for-pivot-table/ ]
keywords: "tabella pivot, aggiornamento stile, Aspose.Cells Cloud, REST API, Excel, foglio di calcolo, API, stile tabella pivot, formatta tutto"
description: "Scopri come aggiornare lo stile di un'intera tabella pivot utilizzando l'API REST di Aspose.Cells Cloud. Include i dettagli della richiesta, un esempio cURL e frammenti di codice SDK per diversi linguaggi di programmazione."
weight: 100
ArticleTitle: "Aggiornamento dello stile per la tabella pivot - Aspose.Cells Cloud API"
---

Questa REST API aggiorna lo stile di una tabella pivot.

## API PostPivotTableStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**Prerequisiti / Autenticazione**  
È necessario fornire un token di accesso JWT valido nell'intestazione `Authorization` (ad esempio, `Bearer <token JWT>`). Assicurati che il token disponga delle autorizzazioni per accedere al foglio di calcolo e alla cartella di lavoro specificati.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo    | Posizione | Descrizione                                                                                      |
| --------------- | ------- | --------- | ------------------------------------------------------------------------------------------------ |
| name            | string  | path      | Nome del file della cartella di lavoro.                                                          |
| sheetName       | string  | path      | Foglio di calcolo contenente la tabella pivot.                                                   |
| pivotTableIndex | integer | path      | Indice in base zero della tabella pivot da formattare.                                           |
| style           | object  | body      | DTO di stile che definisce la formattazione da applicare.                                        |
| needReCalculate | boolean | query     | Impostare su **true** per ricalcolare la tabella pivot dopo la formattazione; il valore predefinito è **false**. |
| folder          | string  | query     | Cartella in cui è memorizzata la cartella di lavoro.                                             |
| storageName     | string  | query     | Nome del servizio di archiviazione.                                                              |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di eseguire direttamente interazioni REST dal browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato).  |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                            |
| 500    | Errore interno del server   | Errore imprevisto sul server.                                               |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il metodo più rapido per sviluppare con l'API. L'SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulla logica di business. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

L'esempio di codice seguente mostra come chiamare l'API utilizzando l'SDK Go:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}