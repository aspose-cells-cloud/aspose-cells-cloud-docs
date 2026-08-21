---
title: "Ottieni MinColumn da un foglio di lavoro Excel"
type: docs
url: /it/get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Ottieni MinColumn, Foglio di lavoro, SDK, API cloud
description: Recupera l'indice minimo della colonna contenente dati in un foglio di lavoro di un file Excel tramite l'API REST Aspose.Cells Cloud.
ArticleTitle: "Ottieni MinColumn da un foglio di lavoro Excel - Aspose.Cells Cloud API"
---

Questa REST API restituisce l'indice minimo della colonna contenente dati in un foglio di lavoro Excel quando il parametro `cellOrMethodName` è impostato su `mincolumn`.

- **Esempio cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Dettagli della richiesta**

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|--------------|-------------|
| `cellOrMethodName` | stringa | Sì | Valore fisso `mincolumn` per indicare l'operazione. |
| `folder` | stringa | No | Percorso della cartella contenente il workbook (se diverso dalla root). |
| `storageName` | stringa | No | Nome dell'archivio Aspose Cloud da utilizzare. |

**Dettagli della risposta**

L'API restituisce un oggetto JSON con una singola proprietà:

```json
{
  "MinColumn": integer   // Indice in base zero della colonna più a sinistra contenente dati.
}
```

Codici di stato HTTP tipici:

- **200 OK** – Richiesta riuscita, restituisce il valore `MinColumn`.  
- **401 Unauthorized** – Token di autenticazione mancante o non valido.  
- **404 Not Found** – Il workbook, il foglio di lavoro o l'intervallo di celle specificati non esistono.  
- **500 Internal Server Error** – Errore imprevisto del server.

- **Utilizzo degli SDK di Aspose.Cells Cloud**

L'utilizzo di un SDK rappresenta il metodo più efficiente per lo sviluppo. Un SDK nasconde i dettagli di basso livello, consentendoti di concentrarti sulla logica del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}
---