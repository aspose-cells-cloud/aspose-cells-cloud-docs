---
title: "Aggiungi un campo pivot a una tabella pivot"
second_title: "Document"
linktype: "Aggiungi campo pivot"
type: docs
url: /it/pivot-tables/add-pivot-field/
aliases: [  /it/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, tabella pivot, aggiungi campo pivot, API REST, SDK"
description: "Aggiungi un campo pivot a una tabella pivot esistente utilizzando l'API REST di Aspose.Cells Cloud. Include i dettagli della richiesta, un esempio cURL e frammenti di codice SDK."
weight: 40
ArticleTitle: "Aggiungi un campo pivot a una tabella pivot – Documentazione di Aspose.Cells Cloud"
---

Questa API REST **aggiunge** un campo pivot a una tabella pivot esistente.

> **Prerequisito:** Per chiamare questo endpoint è necessario includere un token di autenticazione JWT valido nell'intestazione `Authorization` e assicurarsi che il libro sia memorizzato nella cartella specificata o nello spazio di archiviazione predefinito.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### Parametri della richiesta

| Nome del parametro | Tipo    | Posizione | Descrizione                                                        |
|--------------------|---------|-----------|--------------------------------------------------------------------|
| name               | string  | path      | Nome del documento.                                               |
| sheetName          | string  | path      | Nome del foglio di lavoro.                                        |
| pivotTableIndex    | integer | path      | Indice della tabella pivot.                                       |
| pivotFieldType     | string  | query     | Tipo dell'area dei campi (ad esempio, Row, Column).              |
| request            | object  | body      | DTO contenente gli indici dei campi da aggiungere.               |
| needReCalculate    | boolean | query     | Impostare su **true** per ricalcolare la tabella pivot dopo l'operazione. |
| folder             | string  | query     | Cartella in cui è memorizzato il documento.                      |
| storageName        | string  | query     | Nome dello spazio di archiviazione.                               |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per chiamare i servizi web di Aspose.Cells. L'esempio seguente mostra come aggiungere un campo pivot utilizzando cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

{{< /tab >}}

{{< /tabs >}}

La risposta in caso di esito positivo restituisce un oggetto JSON con i campi `Code` e `Status`. Schema di esempio:

```json
{
  "Code": 0,        // intero che indica il codice di stato HTTP
  "Status": "OK"    // messaggio di stringa
}
```

Le risposte di errore possibili includono **400 Bad Request** per parametri mancanti, **401 Unauthorized** se il token non è valido e **500 Internal Server Error** per problemi lato server.

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo più rapido per integrare questa funzionalità. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**Vedi anche:**  
- [Aggiungi una tabella pivot](https://docs.aspose.cloud/cells/it/pivot-tables/add-pivot-table/)  
- [Elimina campo pivot](https://docs.aspose.cloud/cells/it/pivot-tables/delete-pivot-field/)