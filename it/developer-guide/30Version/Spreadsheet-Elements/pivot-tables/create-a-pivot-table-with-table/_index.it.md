---
---
title: "Convertire una tabella in una tabella pivot"
second_title: "Document"
linktype: "Convert"
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases:
  [
    /create-a-pivottable-with-table/,
    /create-new-pivot-table-with-list-object-as-source-data/,
  ]
keywords: "tabella pivot, oggetto elenco, Aspose.Cells Cloud, REST API, convertire una tabella in una tabella pivot"
description: "Scopri come creare una tabella pivot da un oggetto elenco utilizzando l'API REST di Aspose.Cells Cloud. Include i dettagli della richiesta, un esempio cURL e riferimenti agli SDK."
weight: 60
ArticleTitle: "Convertire una tabella in una tabella pivot – Documentazione di Aspose.Cells Cloud"
---

Questa REST API crea una **tabella pivot** a partire da un oggetto elenco.

Una tabella pivot riassume i dati provenienti da un oggetto elenco, consentendo di analizzare e generare report su grandi insiemi di dati direttamente all'interno del foglio di calcolo.

**Prerequisiti:**  
- Un token JWT bearer valido per l'autenticazione.  
- Il foglio di calcolo deve esistere nella posizione di archiviazione specificata.  
- Il foglio di lavoro di destinazione deve contenere l'oggetto elenco che si desidera riassumere.

## API PostWorksheetListObjectSummarizeWithPivotTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome del parametro | Tipo    | Posizione | Descrizione                                   |
| ------------------ | ------- | --------- | --------------------------------------------- |
| name               | string  | path      | Nome del file del foglio di calcolo.          |
| sheetName          | string  | path      | Foglio di lavoro contenente l'oggetto elenco. |
| listObjectIndex    | integer | path      | Indice dell'oggetto elenco nel foglio di lavoro. |
| destsheetName      | string  | query     | Nome del foglio di lavoro di destinazione.    |
| request            | object  | body      | Payload JSON che definisce la tabella pivot.  |
| folder             | string  | query     | Percorso della cartella in cui risiede il foglio di calcolo. |
| storageName        | string  | query     | Nome dell'archivio.                           |

Il corpo della richiesta deve seguire lo schema JSON definito di seguito:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Nome della nuova tabella pivot." },
    "DestCellName": { "type": "string", "description": "Cella in alto a sinistra della tabella pivot (ad esempio, \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Indici in base zero dei campi da posizionare nelle righe."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Indici in base zero dei campi da posizionare nelle colonne."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Indici in base zero dei campi da utilizzare come campi dati."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

La <a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*Nota: Utilizzare l'endpoint di produzione (`api.aspose.cloud`) negli ambienti di produzione. L'endpoint QA (`api-qa.aspose.cloud`) è destinato esclusivamente al testing. È richiesto HTTPS per tutte le chiamate in produzione.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di stato HTTP**

| Codice | Significato                  | Descrizione                                              |
|--------|------------------------------|----------------------------------------------------------|
| 200    | OK                           | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida         | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato              | Token JWT non valido o mancante. |
| 413    | Payload troppo grande        | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server    | Errore imprevisto sul server. |

## Famiglia di SDK per il cloud

L'utilizzo di un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:  
---