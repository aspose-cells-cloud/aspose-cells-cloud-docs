---
title: "Imposta il valore di un intervallo in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Imposta valori"
type: docs
url: /it/ranges/update/values/
aliases: [  /it/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells, API Excel, imposta valore intervallo, API REST, SDK cloud, aggiornamento foglio di lavoro"
description: "Scopri come impostare il valore di una cella o di un intervallo in un libro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempio cURL, codice di esempio con SDK e gestione degli errori."
weight: 72
ArticleTitle: "Imposta il valore di un intervallo in un foglio di lavoro Excel – API Aspose.Cells Cloud"
---

Utilizza questa API REST per impostare un valore in un intervallo specificato. Quando appropriato, il valore viene convertito in un altro tipo di dati e il formato numerico della cella viene ripristinato.

**Prerequisiti**  
- Un account Aspose Cloud valido.  
- Un token JWT che include l'ambito `Cells.ReadWrite`.  
- Il libro deve essere già caricato nella posizione di archiviazione di destinazione.

## API PostWorksheetCellsRangeValue

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

I parametri della richiesta sono:

| Nome Parametro | Tipo    | Posizione | Descrizione                                                |
|----------------|---------|-----------|------------------------------------------------------------|
| name           | string  | path      | Nome del libro                                             |
| sheetName      | string  | path      | Nome del foglio di lavoro                                  |
| value          | string  | query     | Valore di input                                            |
| range          | object  | body      | Oggetto intervallo nel foglio di lavoro                    |
| isConverted    | boolean | query     | Indica se il valore di input deve essere convertito        |
| setStyle       | boolean | query     | Indica se applicare lo stile alle celle di destinazione    |
| folder         | string  | query     | Cartella del libro                                         |
| storageName    | string  | query     | Nome dell'archiviazione                                    |

**Esempio di oggetto `range`** che può essere inviato nel corpo della richiesta:

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL. **Includi un token JWT valido nell'header `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
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

**Schema della risposta**

| Campo   | Tipo    | Descrizione                                              |
|---------|---------|----------------------------------------------------------|
| Code    | integer | Codice di stato HTTP dell'operazione.                    |
| Status  | string  | Breve descrizione del risultato (es. "OK").              |
| Message | string  | Messaggio di errore dettagliato in caso di fallimento (opzionale). |
| Result  | object  | Dati aggiuntivi restituiti per chiamate riuscite (opzionale). |

**Codici di stato HTTP possibili**

- **200 OK** – Il valore dell'intervallo è stato impostato correttamente.  
- **400 Bad Request** – Parametri non validi o corpo della richiesta malformato.  
- **401 Unauthorized** – Token JWT mancante o non valido.  
- **403 Forbidden** – Autorizzazioni insufficienti per l'operazione richiesta.  
- **404 Not Found** – Il libro, il foglio di lavoro o l'intervallo specificato non esistono.  
- **500 Internal Server Error** – Errore imprevisto del server.

*Esempio di risposta di errore per un 400 Bad Request:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "All'oggetto 'range' mancano campi obbligatori."
}
```

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}