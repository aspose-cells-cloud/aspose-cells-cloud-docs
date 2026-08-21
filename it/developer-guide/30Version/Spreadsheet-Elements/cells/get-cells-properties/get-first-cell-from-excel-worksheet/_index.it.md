---
title: "Ottenere la prima cella (A1) da un foglio di lavoro Excel"
type: docs
url: /it/get-first-cell-from-excel-worksheet/
weight: 20
keywords: "Aspose.Cells Cloud, Excel, REST API, Ottenere la prima cella, Foglio di lavoro, A1, API v3"
description: "Scopri come recuperare la prima cella (A1) di un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud v3.0. Include richiesta cURL, risposta JSON, esempi di errori e esempi di SDK per C#, Java, PHP, Python e altri."
ArticleTitle: "Ottenere la prima cella (A1) da un foglio di lavoro Excel tramite Aspose.Cells Cloud API"
---

Questa REST API mostra come recuperare la **prima cella** in un file Excel quando il parametro `cellOrMethodName` è impostato su `firstcell`.

**Endpoint**  
`GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{worksheet}/cells/firstcell`

- **Esempio cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/firstcell" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parametri**

| Parametro          | Tipo   | Descrizione                                                                 | Obbligatorio |
|--------------------|--------|-----------------------------------------------------------------------------|--------------|
| `cellOrMethodName` | string | Deve essere impostato su `firstcell` per recuperare la prima cella.       | Sì           |
| `fileName`         | string | Nome del file del workbook (ad esempio, `myWorkbook.xlsx`).                | Sì           |
| `worksheet`        | string | Nome del foglio di lavoro (ad esempio, `Sheet1`).                          | Sì           |
| `Authorization`    | header | Token Bearer per l'autenticazione.                                         | Sì           |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A1",
    "Row": 0,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**Risposte di errore**

- **401 Non autorizzato**

```json
{
  "Code": "401",
  "Message": "Token di accesso non valido."
}
```

- **404 Non trovato**

```json
{
  "Code": "404",
  "Message": "Il workbook, il foglio di lavoro o la cella specificati non esistono."
}
```

- **500 Errore interno del server**

```json
{
  "Code": "500",
  "Message": "Si è verificato un errore imprevisto sul server."
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                              |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.              |
| 500    | Errore interno del server   | Errore imprevisto sul server.                                 |

{{< /tab >}}

{{< /tabs >}}

- **Famiglia di SDK per il cloud**

Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}
---