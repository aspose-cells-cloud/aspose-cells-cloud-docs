---
title: "Trabajar con archivos de Excel: Cálculo de fórmulas, ajuste automático, limpieza de objetos, etc."
second_title: "Documentos"
linktype: "Operaciones comunes de Excel"
type: docs
url: /workbook/
aliases: [/working-with-workbook/]
keywords: "Aspose.Cells, API de Excel, operaciones de libro de cálculo, cálculo de fórmulas, ajuste automático"
description: "Aprenda a trabajar con libros de Excel mediante la API REST de Aspose.Cells Cloud. Guías paso a paso que cubren el cálculo de fórmulas, ajuste automático de filas/columnas, limpieza de objetos y recuperación de metadatos del libro. SDK disponibles para Python, .NET, Java y más."
weight: 20
---

## Trabajar con un libro de Excel

Aspose.Cells Cloud proporciona un conjunto completo de puntos finales REST para gestionar libros de Excel. Las operaciones descritas a continuación permiten crear, recuperar, modificar y analizar libros de forma programática. Los requisitos previos incluyen una clave de API válida y el SDK correspondiente (Python, .NET, Java, etc.) para la versión de Aspose.Cells Cloud que esté utilizando.

- [Cómo calcular fórmulas en un archivo de Excel.](/cells/workbook/calculate-all-formulas/)
- [Cómo crear un archivo de Excel.](/cells/workbook/create/)
- [Cómo obtener un archivo de Excel.](/cells/workbook/get/)
- [Cómo ajustar automáticamente las columnas en un archivo de Excel.](/cells/autofit-columns-on-an-excel-file/)
- [Cómo ajustar automáticamente las filas en un archivo de Excel.](/cells/autofit-rows-on-an-excel-file/)
- [Cómo obtener el número de páginas en un archivo de Excel.](/cells/get-page-count-from-an-excel-file/)
- [Cómo obtener nombres desde un archivo de Excel.](/cells/get-names-from-an-excel-file/)

**Preguntas frecuentes**

**P:** ¿Cómo activo el cálculo de fórmulas tras subir un libro?  
**R:** Llame al punto final `POST /cells/{name}/calculate` (o use el método del SDK `Workbook.calculateAll`). La API recalculará todas las fórmulas y devolverá el libro actualizado.

**P:** ¿Cuál es la mejor manera de ajustar automáticamente todas las columnas en una hoja de cálculo?  
**R:** Utilice el punto final `POST /cells/{name}/worksheets/{sheetName}/autofitcolumns` (o el método del SDK `Worksheet.autoFitColumns`). Esto ajusta el ancho de las columnas según el contenido más largo de las celdas.

**P:** ¿Cómo puedo eliminar todas las formas, gráficos e imágenes de un libro?  
**R:** Llame al punto final `DELETE /cells/{name}/clearobjects` (o al método del SDK `Workbook.clearObjects`). Esto elimina todos los objetos gráficos, preservando los datos de las celdas.

```json
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Operaciones con libros de Excel – Aspose.Cells Cloud",
  "description": "Guías paso a paso para calcular fórmulas, ajustar automáticamente filas/columnas, limpiar objetos y más, utilizando Aspose.Cells Cloud.",
  "breadcrumb": {
    "@type": "ItemList",
    "itemListElement": [
      {
        "@type": "ListItem",
        "position": 1,
        "name": "Inicio",
        "item": "https://docs.aspose.cloud/"
      },
      {
        "@type": "ListItem",
        "position": 2,
        "name": "Cells",
        "item": "https://docs.aspose.cloud/cells/"
      },
      {
        "@type": "ListItem",
        "position": 3,
        "name": "Operaciones con libros",
        "item": "https://docs.aspose.cloud/cells/workbook/"
      }
    ]
  },
  "datePublished": "2026-03-30",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "url": "https://www.aspose.com"
  }
}
```