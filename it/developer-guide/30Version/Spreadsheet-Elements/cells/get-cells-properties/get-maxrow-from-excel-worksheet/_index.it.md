---
title: "Recuperare il numero massimo di riga in un foglio di calcolo Excel – Aspose.Cells Cloud API"
type: docs
url: /it/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Recuperare il numero massimo di riga in un foglio di calcolo Excel – Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, Cloud SDK, Foglio di calcolo, Foglio, GetMaxRow"
description: "Scopri come recuperare il numero massimo di riga in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, lo schema della risposta, esempi di SDK e note sull'uso."
---

Questa REST API restituisce il **numero massimo di riga** in un foglio di calcolo Excel quando il parametro `cellOrMethodName` è impostato su `maxrow`.

- **Esempio cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Utilizzo degli SDK di Aspose.Cells Cloud**

Utilizzare un SDK rappresenta il modo più efficiente per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulla logica del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**Riferimento API**

| Elemento | Dettagli |
|--------|----------|
| **Metodo** | `GET` |
| **Endpoint** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **Parametri di percorso** | `fileName` – nome del file Excel (obbligatorio) <br> `sheetName` – nome del foglio di calcolo (obbligatorio) |
| **Parametri di query** | `folder` – percorso della cartella nello storage (opzionale) <br> `storageName` – nome dello storage (opzionale) |
| **Risposta in caso di successo** | `200 OK` <br> ```json { "MaxRow": integer } ``` |
| **Risposte in caso di errore** | `400 Bad Request` – parametri non validi <br> `401 Unauthorized` – fallimento dell'autenticazione <br> `404 Not Found` – file o foglio non trovato |

**Prerequisiti**

- Un token di autenticazione valido di Aspose Cloud.  
- Il workbook di destinazione deve essere caricato nello storage di Aspose Cloud o accessibile tramite un URL pubblico.  

**Note**

- L'operazione è disponibile dalla versione **v3.0** dell'API in poi.  
- Il valore `MaxRow` restituito corrisponde all'indice della riga utilizzata più alta (1‑basato). Per un foglio vuoto, il valore è generalmente `1`.  

Gli esempi di SDK riportati di seguito illustrano come richiamare l'operazione in diverse lingue di programmazione.