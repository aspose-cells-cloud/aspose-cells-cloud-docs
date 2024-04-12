---
title: Ottieni Cells Proprietà
type: docs
url: /it/get-cells-properties/
weight: 130
---
Questo REST API indica come eseguire `get a specific cell` in un file Excel.

## RSETAPI
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Nome del documento.|
| nomefoglio| corda| sentiero| Nome del foglio di lavoro.|
| cellOrMethodName| corda| sentiero|Il nome della cella o del metodo. (Valore del nome del metodo: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn e cellName.)|
| cartella| corda| domanda| Cartella del documento.|
| storageName| corda| domanda| nome dell'archivio.|
 
 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.


- **Come ottenere una cella specifica**

   - [Ottieni i dati della cella da un foglio di lavoro](/cells/it/get-cell-data-from-a-worksheet/)
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
