---
title: Skaffa Cells Fastighet
type: docs
url: /sv/get-cells-properties/
weight: 130
---
Denna REST API visar hur man `get a specific cell` i en Excel fil.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokument namn.|
| arknamn| sträng| väg| Arbetsbladsnamn.|
| cellOrMethodName| sträng| väg| Cellens eller metodnamnet. (Metodnamnsvärde: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn och cellName.)|
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.


- **Hur man får specifik cell**

   - [Hämta celldata från ett arbetsblad](/cells/sv/get-cell-data-from-a-worksheet/)
   - [Få första cellen från Excel Arbetsblad](/cells/sv/get-first-cell-from-excel-worksheet/)
   - [Hämta sista cellen av Excel arbetsblad](/cells/sv/get-last-cell-of-excel-worksheet/)
   - [Skaffa MaxRow från Excel arbetsblad](/cells/sv/get-maxrow-from-excel-worksheet/)
   - [Hämta MaxDataRow från Excel arbetsblad](/cells/sv/get-maxdatarow-from-excel-worksheet/)
   - [Hämta MaxColumn från Excel arbetsblad](/cells/sv/get-maxcolumn-from-excel-worksheet/)
   - [Hämta MaxDataColumn från Excel arbetsblad](/cells/sv/get-maxdatacolumn-from-excel-worksheet/)
   - [Få MinRow från Excel Arbetsblad](/cells/sv/get-minrow-from-excel-worksheet/)
   - [Hämta MinDataRow från Excel arbetsblad](/cells/sv/get-mindatarow-from-excel-worksheet/)
   - [Få MinColumn från Excel Arbetsblad](/cells/sv/get-mincolumn-from-excel-worksheet/)
   - [Hämta MinDataColumn från Excel arbetsblad](/cells/sv/get-mindatacolumn-from-excel-worksheet/)
