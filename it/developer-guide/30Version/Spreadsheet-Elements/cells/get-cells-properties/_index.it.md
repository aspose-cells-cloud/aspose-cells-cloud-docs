---
title: Ottieni Cells Proprietà
type: docs
url: /it/get-cells-properties/
weight: 130
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Ottieni Cells Proprietà
---
Questo REST API indica come `get a specific cell` in un file Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Nome del documento.|
| Nome foglio| corda| sentiero| Nome del foglio di lavoro.|
| cellOrMethodName| corda| sentiero|Nome della cella o del metodo. (Valore del nome del metodo: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn e cellName.)|
| cartella| corda| domanda| Cartella del documento.|
| Nome di archiviazione| corda| domanda| nome di archiviazione.|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

### **Famiglia Cloud SDK**

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

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

### **Come ottenere una cella specifica**

- [Ottieni dati di celle da un foglio di lavoro](/cells/it/get-cell-data-from-a-worksheet/)
- [Ottieni la prima cella dal foglio di lavoro Excel](/cells/it/get-first-cell-from-excel-worksheet/)
- [Ottieni l'ultima cella del foglio di lavoro Excel](/cells/it/get-last-cell-of-excel-worksheet/)
- [Ottieni MaxRow dal foglio di lavoro Excel](/cells/it/get-maxrow-from-excel-worksheet/)
- [Ottieni MaxDataRow dal foglio di lavoro Excel](/cells/it/get-maxdatarow-from-excel-worksheet/)
- [Ottieni MaxColumn dal foglio di lavoro Excel](/cells/it/get-maxcolumn-from-excel-worksheet/)
- [Ottieni MaxDataColumn dal foglio di lavoro Excel](/cells/it/get-maxdatacolumn-from-excel-worksheet/)
- [Ottieni MinRow dal foglio di lavoro Excel](/cells/it/get-minrow-from-excel-worksheet/)
- [Ottieni MinDataRow dal foglio di lavoro Excel](/cells/it/get-mindatarow-from-excel-worksheet/)
- [Ottieni MinColumn dal foglio di lavoro Excel](/cells/it/get-mincolumn-from-excel-worksheet/)
- [Ottieni MinDataColumn dal foglio di lavoro Excel](/cells/it/get-mindatacolumn-from-excel-worksheet/)
