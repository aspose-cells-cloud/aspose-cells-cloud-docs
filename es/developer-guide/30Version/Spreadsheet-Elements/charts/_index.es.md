---
title: "Trabajar con gráficos de Excel"
second_title: "Documento"
linktype: "Gráficos"
type: docs
url: /es/charts/
aliases: [  /es/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, gráfico, API, REST, nube, hoja de cálculo"
description: "Aprenda a administrar gráficos de Excel mediante la API de Aspose.Cells Cloud. Guías paso a paso, ejemplos de código y manejo de errores para recuperar, agregar, actualizar, eliminar y convertir gráficos a formatos de imagen."
weight: 100
ArticleTitle: "Trabajar con gráficos de Excel – Documentación de Aspose.Cells Cloud"
---

## Trabajar con gráficos en un archivo de Excel

**Última actualización:** julio de 2026

Los gráficos de Excel son representaciones visuales de datos que ayudan a los usuarios a comprender rápidamente tendencias y patrones.  
La API de Aspose.Cells Cloud permite a los desarrolladores trabajar programáticamente con estos gráficos dentro de libros de Excel almacenados en la nube. Con esta API, puede recuperar gráficos existentes, agregar nuevos, modificar sus propiedades (como títulos, ejes y leyendas), eliminar gráficos no deseados y convertir gráficos a formatos de imagen para informes o procesamiento posterior. Los siguientes enlaces le brindan acceso directo a las páginas detalladas de operación para cada acción relacionada con gráficos admitida.

### Referencia rápida

| Operación | Método HTTP | Endpoint (plantilla) | Documentación |
|-----------|-------------|---------------------|---------------|
| Obtener gráfico | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Obtener un gráfico de una hoja de cálculo](/es/cells/get-chart-from-a-worksheet/) |
| Agregar gráfico | POST | `/cells/{file}/worksheets/{sheet}/charts` | [Agregar un gráfico en una hoja de cálculo](/es/cells/add-a-chart-in-a-worksheet/) |
| Eliminar todos los gráficos | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [Eliminar todos los gráficos de una hoja de cálculo](/es/cells/delete-all-charts-from-a-worksheet/) |
| Eliminar gráfico | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Eliminar un gráfico de una hoja de cálculo](/es/cells/delete-a-chart-from-a-worksheet/) |
| Convertir gráfico a imagen | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [Convertir gráfico a imagen](/es/cells/convert-chart-to-image/) |
| Obtener área del gráfico | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [Obtener el área del gráfico de una hoja de cálculo](/es/cells/get-chart-area-from-a-worksheet/) |
| Obtener formato de relleno | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [Obtener el formato de relleno del área de un gráfico de una hoja de cálculo](/es/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Obtener leyenda | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Obtener la leyenda del gráfico de una hoja de cálculo](/es/cells/get-chart-legend-from-a-worksheet/) |
| Actualizar leyenda | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Actualizar la leyenda del gráfico en una hoja de cálculo](/es/cells/update-chart-legend-in-a-worksheet/) |
| Mostrar leyenda | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [Mostrar la leyenda del gráfico en una hoja de cálculo](/es/cells/show-chart-legend-in-a-worksheet/) |
| Ocultar leyenda | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [Ocultar la leyenda del gráfico en una hoja de cálculo](/es/cells/hide-chart-legend-in-a-worksheet/) |
| Obtener título | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Obtener el título del gráfico de una hoja de cálculo](/es/cells/get-chart-title-from-a-worksheet/) |
| Establecer título | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Establecer el título del gráfico en una hoja de cálculo de Excel](/es/cells/set-chart-title-in-excel-worksheet/) |
| Actualizar título | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Actualizar el título del gráfico en una hoja de cálculo de Excel](/es/cells/update-chart-title-in-excel-worksheet/) |
| Eliminar título | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Eliminar el título del gráfico en una hoja de cálculo](/es/cells/delete-chart-title-in-a-worksheet/) |
| Actualizar propiedades del gráfico | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Actualizar las propiedades del gráfico](/es/cells/charts/properties/update/) |
| Obtener eje de categorías | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Obtener el eje de categorías del gráfico](/es/cells/charts/category-axis/get/) |
| Obtener eje de valores | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Obtener el eje de valores del gráfico](/es/cells/charts/value-axis/get/) |
| Obtener segundo eje de categorías | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Obtener el segundo eje de categorías del gráfico](/es/cells/charts/second-category-axis/get/) |
| Obtener segundo eje de valores | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Obtener el segundo eje de valores del gráfico](/es/cells/charts/second-value-axis/get/) |
| Actualizar eje de categorías | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Actualizar el eje de categorías del gráfico](/es/cells/charts/category-axis/update/) |
| Actualizar eje de valores | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Actualizar el eje de valores del gráfico](/es/cells/charts/value-axis/update/) |
| Actualizar segundo eje de categorías | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Actualizar el segundo eje de categorías del gráfico](/es/cells/charts/second-category-axis/update/) |
| Actualizar segundo eje de valores | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Actualizar el segundo eje de valores del gráfico](/es/cells/charts/second-value-axis/update/) |

- [Obtener un gráfico de una hoja de cálculo](/es/cells/get-chart-from-a-worksheet/)
- [Agregar un gráfico en una hoja de cálculo](/es/cells/add-a-chart-in-a-worksheet/)
- [Eliminar todos los gráficos de una hoja de cálculo](/es/cells/delete-all-charts-from-a-worksheet/)
- [Eliminar un gráfico de una hoja de cálculo](/es/cells/delete-a-chart-from-a-worksheet/)
- [Convertir gráfico a imagen](/es/cells/convert-chart-to-image/)
- [Obtener el área del gráfico de una hoja de cálculo](/es/cells/get-chart-area-from-a-worksheet/)
- [Obtener el formato de relleno del área de un gráfico de una hoja de cálculo](/es/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Obtener la leyenda del gráfico de una hoja de cálculo](/es/cells/get-chart-legend-from-a-worksheet/)
- [Actualizar la leyenda del gráfico en una hoja de cálculo](/es/cells/update-chart-legend-in-a-worksheet/)
- [Mostrar la leyenda del gráfico en una hoja de cálculo](/es/cells/show-chart-legend-in-a-worksheet/)
- [Ocultar la leyenda del gráfico en una hoja de cálculo](/es/cells/hide-chart-legend-in-a-worksheet/)
- [Obtener el título del gráfico de una hoja de cálculo](/es/cells/get-chart-title-from-a-worksheet/)
- [Establecer el título del gráfico en una hoja de cálculo de Excel](/es/cells/set-chart-title-in-excel-worksheet/)
- [Actualizar el título del gráfico en una hoja de cálculo de Excel](/es/cells/update-chart-title-in-excel-worksheet/)
- [Eliminar el título del gráfico en una hoja de cálculo](/es/cells/delete-chart-title-in-a-worksheet/)
- [Actualizar las propiedades del gráfico](/es/cells/charts/properties/update/)
- [Obtener el eje de categorías del gráfico](/es/cells/charts/category-axis/get/)
- [Obtener el eje de valores del gráfico](/es/cells/charts/value-axis/get/)
- [Obtener el segundo eje de categorías del gráfico](/es/cells/charts/second-category-axis/get/)
- [Obtener el segundo eje de valores del gráfico](/es/cells/charts/second-value-axis/get/)
- [Actualizar el eje de categorías del gráfico](/es/cells/charts/category-axis/update/)
- [Actualizar el eje de valores del gráfico](/es/cells/charts/value-axis/update/)
- [Actualizar el segundo eje de categorías del gráfico](/es/cells/charts/second-category-axis/update/)
- [Actualizar el segundo eje de valores del gráfico](/es/cells/charts/second-value-axis/update/)