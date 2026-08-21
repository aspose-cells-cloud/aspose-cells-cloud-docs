---
title: "Ottenere l'ultima cella di un foglio di calcolo Excel – Aspose.Cells Cloud API (v4.0)"
type: docs
url: /it/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, API Excel, ottenere l'ultima cella, foglio di calcolo, cloud"
description: "Recupera l'indirizzo della cella finale di un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud v4.0. Include dettagli della richiesta, esempio cURL, risposta JSON ed esempi di SDK."
ArticleTitle: "Ottenere la cella finale di un foglio di calcolo Excel – Aspose.Cells Cloud API v4.0"
---

Questa API REST restituisce la **cella finale** (*endcell*) di un foglio di calcolo Excel quando il parametro `cellOrMethodName` è impostato su `endcell`.

**Panoramica**  
L'operazione **Get Last Cell** (Ottieni ultima cella) restituisce l'indirizzo dell'ultima cella utilizzata in un foglio specificato. È utile per determinare l'intervallo effettivo dei dati in un foglio senza dover esaminare l'intero libro.

- **Esempio cURL.**

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<More Info>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",
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

{{< /tab >}}

{{< /tabs >}}

### Parametri
| Parametro            | Tipo   | Obbligatorio | Descrizione |
|----------------------|--------|--------------|-------------|
| `fileName`           | string | Sì           | Nome del file Excel archiviato nel cloud. |
| `worksheetName`      | string | Sì           | Nome del foglio di calcolo dal quale recuperare l'ultima cella. |
| `cellOrMethodName`   | string | Sì           | Deve essere impostato su **`endcell`** per richiamare questa operazione. |
| `folder` *(opzionale)*| string | No          | Percorso della cartella cloud in cui si trova il libro. |
| `storageName` *(opzionale)*| string | No      | Nome dello storage. Se omesso, viene utilizzato lo storage predefinito. |

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | File caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

- **Utilizzare gli SDK di Aspose.Cells Cloud**

L'utilizzo di un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_In arrivo a breve._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

Per altre operazioni relative alla navigazione tra celle, consulta gli argomenti **[Ottieni prima cella](/it/get-first-cell-of-excel-worksheet/)** e **[Ottieni riga massima](/it/get-max-row-of-worksheet/)**.