---
title: Obtener Cells Propiedad
type: docs
url: /es/get-cells-properties/
weight: 130
---
Este REST API indica cómo `get a specific cell` en un archivo Excel.

## RESET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| Nombre del documento.|
| hojaNombre| cadena| camino| Nombre de la hoja de trabajo.|
| cellOrMethodName| cadena| camino| El nombre de la celda o del método. (Valor del nombre del método: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn y cellName).|
| carpeta| cadena| consulta| Carpeta del documento.|
| NombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.


- **Cómo obtener una celda específica**

   - [Obtener datos de celda de una hoja de trabajo](/cells/es/get-cell-data-from-a-worksheet/)
   - [Obtenga la primera celda de la hoja de trabajo Excel](/cells/es/get-first-cell-from-excel-worksheet/)
   - [Obtenga la última celda de la hoja de trabajo Excel](/cells/es/get-last-cell-of-excel-worksheet/)
   - [Obtener MaxRow de Excel Hoja de trabajo](/cells/es/get-maxrow-from-excel-worksheet/)
   - [Obtenga MaxDataRow de la hoja de trabajo Excel](/cells/es/get-maxdatarow-from-excel-worksheet/)
   - [Obtener MaxColumn de Excel Hoja de trabajo](/cells/es/get-maxcolumn-from-excel-worksheet/)
   - [Obtenga MaxDataColumn de la hoja de trabajo Excel](/cells/es/get-maxdatacolumn-from-excel-worksheet/)
   - [Obtener MinRow de Excel Hoja de trabajo](/cells/es/get-minrow-from-excel-worksheet/)
   - [Obtenga MinDataRow de la hoja de trabajo Excel](/cells/es/get-mindatarow-from-excel-worksheet/)
   - [Obtener MinColumn de Excel Hoja de trabajo](/cells/es/get-mincolumn-from-excel-worksheet/)
   - [Obtenga MinDataColumn de la hoja de trabajo Excel](/cells/es/get-mindatacolumn-from-excel-worksheet/)
