---
title: Obtener Cells Propiedad
type: docs
url: /es/get-cells-properties/
weight: 130
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Obtener propiedades Cells
---
Este REST API indica cómo `get a specific cell` en un archivo Excel.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| Nombre del documento.|
| nombreHoja| cadena| camino| Nombre de la hoja de trabajo.|
| cellOrMethodName| cadena| camino|Nombre de la celda o del método. (Valor del nombre del método: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn y cellName).|
| carpeta| cadena| consulta| Carpeta de documentos.|
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

### **Familia de SDK en la nube**

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

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

### **Cómo obtener una celda específica**

- [Obtener datos de celdas de una hoja de cálculo](/cells/es/get-cell-data-from-a-worksheet/)
- [Obtener la primera celda de la hoja de trabajo Excel](/cells/es/get-first-cell-from-excel-worksheet/)
- [Obtener la última celda de la hoja de trabajo Excel](/cells/es/get-last-cell-of-excel-worksheet/)
- [Obtener MaxRow de la hoja de trabajo Excel](/cells/es/get-maxrow-from-excel-worksheet/)
- [Obtener MaxDataRow de la hoja de trabajo Excel](/cells/es/get-maxdatarow-from-excel-worksheet/)
- [Obtener MaxColumn de la hoja de trabajo Excel](/cells/es/get-maxcolumn-from-excel-worksheet/)
- [Obtener MaxDataColumn de la hoja de trabajo Excel](/cells/es/get-maxdatacolumn-from-excel-worksheet/)
- [Obtener MinRow de la hoja de trabajo Excel](/cells/es/get-minrow-from-excel-worksheet/)
- [Obtener MinDataRow de la hoja de trabajo Excel](/cells/es/get-mindatarow-from-excel-worksheet/)
- [Obtener MinColumn de la hoja de trabajo Excel](/cells/es/get-mincolumn-from-excel-worksheet/)
- [Obtener MinDataColumn de la hoja de trabajo Excel](/cells/es/get-mindatacolumn-from-excel-worksheet/)
