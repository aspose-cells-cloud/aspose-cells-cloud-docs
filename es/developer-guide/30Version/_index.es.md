---
title: "Guía del desarrollador de Aspose.Cells Cloud 3.0"
ArticleTitle: "Guía del desarrollador de la API REST de Aspose.Cells Cloud 3.0 – Creación, conversión y estilizado de libros de Excel"
second_title: "Documentos"
type: docs
url: /es/developer-guide-3.0/
aliases: [  /es/developer-guide/v3.0/ , /es/developer-guide-v3.0/ ]
keywords: "Aspose.Cells Cloud, API REST de Excel, conversión de libros, API de gráficos, importación de datos, exportación, PDF, CSV, JSON, guía del desarrollador"
description: "Aprenda a utilizar las API REST de Aspose.Cells Cloud 3.0 para la creación, conversión, estilizado, gráficos, tablas y mucho más de libros de Excel. Incluye ejemplos de código y consejos de buenas prácticas."
weight: 150
---

## Trabajo con las API REST de Aspose.Cells Cloud

La **Guía del desarrollador de Aspose.Cells Cloud 3.0** ofrece una visión general concisa y buscable de las operaciones más utilizadas de la API REST para libros y hojas de cálculo de Excel. Está dirigida a desarrolladores que necesitan crear, modificar, convertir y manipular archivos de Excel mediante programación. Utilice las secciones siguientes para localizar la operación que necesita; cada enlace lleva a una página detallada con la sintaxis de la solicitud, los parámetros y ejemplos. Esta página centraliza la referencia de la **API REST de Aspose.Cells Cloud**, facilitando la búsqueda de puntos de conexión relacionados con libros, gestión de gráficos, importación y funciones de exportación.

**Prerrequisitos:** Antes de utilizar las API, asegúrese de tener una cuenta válida de Aspose Cloud, una clave API y un secreto, y los SDKs correspondientes instalados en su entorno de desarrollo.

### Índice

- [Operaciones de archivo](#file-operations)
- [Inicio (Formato de celdas y gestión de filas/columnas)](#home-cell-formatting--rowcolumn-management)
- [Insertar (Gráficos, tablas y objetos OLE)](#insert-charts-tables--ole-objects)
- [Diseño de página (Saltos de página y configuración)](#page-layout-page-breaks--setup)
- [Fórmulas (Cálculo y nombres)](#formulas-calculate--names)
- [Datos (Esquema, filtro e importación)](#data-outline-filter--import)
- [Revisar (Comentarios y protección)](#review-comments--protection)
- [Ver (Controles de ventana y zoom)](#view-window--zoom-controls)

### Resumen rápido de la API

| Grupo de API          | Punto de conexión de ejemplo                           | Acción principal                                               |
| --------------------- | ------------------------------------------------------ | -------------------------------------------------------------- |
| **Crear libro**       | `POST /cells/workbook`                                 | Crear un nuevo libro de Excel vacío                            |
| **Convertir libro**   | `PUT /cells/workbook/convert`                          | Convertir un archivo de Excel a PDF, CSV, JSON, etc.           |
| **Agregar gráfico**   | `POST /cells/worksheets/{sheetName}/charts`            | Insertar un nuevo gráfico en una hoja de cálculo               |
| **Gestionar tablas**  | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | Actualizar o eliminar un objeto de lista (tabla)               |
| **Importar datos**    | `POST /cells/worksheets/{sheetName}/import`            | Importar CSV, JSON, imágenes o matrices en una hoja de cálculo |
| **Calcular fórmulas** | `POST /cells/workbook/calculate`                       | Recalcular todas las fórmulas en un libro                      |
| **Aplicar filtros**   | `POST /cells/worksheets/{sheetName}/filters`           | Agregar o eliminar criterios de filtro automático              |
| **Proteger libro**    | `POST /cells/workbook/protect`                         | Aplicar protección con contraseña a un libro                   |

Estas operaciones de alta frecuencia cubren la funcionalidad principal de la **API REST de Aspose.Cells Cloud para Excel** y enlazan directamente con páginas de documentación detalladas.

Puede descargar una versión en PDF de la tabla de Resumen rápido de la API para referencia sin conexión.

{{< tabs tabTotal="8" tabID="1" tabName1="File" tabName2="Home" tabName3="Insert" tabName4="Page Layout" tabName5="Formulas" tabName6="Data" tabName7="Review" tabName8="View" >}}
{{< tab tabNum="1" >}}

<div class="row">
    <div class="col-md-6">
        <p>Libro: Nuevo, Convertir, Guardar como</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="Crear un libro de Excel vacío mediante API" rel="noopener">Crear un libro de Excel vacío.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="Crear un libro a partir de un archivo de plantilla" rel="noopener">Crear un libro de Excel a partir de un archivo de plantilla.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="Crear un libro a partir de una plantilla de SmartMarker" rel="noopener">Crear un libro de Excel a partir de una plantilla de SmartMarker.</a></li>
            <li><a href="/cells/convert/" title="Convertir un libro de Excel a otro formato" rel="noopener">Convertir un libro de Excel a distintos formatos de archivo.</a></li>
            <li><a href="/cells/saveas-other-formats/" title="Guardar un libro de Excel en otro formato" rel="noopener">Guardar un libro de Excel en distintos formatos de archivo.</a></li>
        </ul>
        <p>Buscar, Reemplazar</p>
        <ul>
            <li><a href="/cells/search/" title="Buscar texto en archivos de Excel" rel="noopener">Buscar texto en archivos de Excel.</a></li>
            <li><a href="/cells/replace/" title="Reemplazar valores en archivos de Excel" rel="noopener">Reemplazar valores antiguos por nuevos en archivos de Excel.</a></li>
        </ul>
        <p>Comprimir</p>
        <ul>
            <li><a href="/cells/compress/" title="Comprimir archivos de Excel" rel="noopener">Comprimir archivos de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Libro: Combinar, Dividir</p>
        <ul>
            <li><a href="/cells/merge/" title="Combinar varios libros de Excel" rel="noopener">Combinar libros de Excel.</a></li>
            <li><a href="/cells/split/" title="Dividir un libro de Excel en archivos independientes" rel="noopener">Dividir libros de Excel.</a></li>
        </ul>
        <p>Marcas de agua</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="Agregar una imagen de fondo a un libro" rel="noopener">Agregar fondo a un libro.</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="Eliminar una imagen de fondo de un libro" rel="noopener">Eliminar fondo de un libro.</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="Establecer un fondo o marca de agua en una hoja de cálculo" rel="noopener">Establecer fondo o marca de agua en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="Eliminar el fondo o la marca de agua de una hoja de cálculo" rel="noopener">Eliminar fondo o marca de agua de una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>Fuentes, estilos, formato condicional y valores de celdas</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="Recuperar un estilo de celda de una hoja de cálculo" rel="noopener">Obtener estilo de celda de una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="Actualizar estilos de varias celdas" rel="noopener">Actualizar estilo de varias celdas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="Cambiar el estilo de una sola celda" rel="noopener">Actualizar estilo de celda en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="Aplicar formato de texto enriquecido a una celda" rel="noopener">Establecer formato de texto enriquecido para una celda en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Borrar contenido y estilos de celdas" rel="noopener">Borrar contenido y estilos de celdas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="Gestionar reglas de formato condicional" rel="noopener">Agregar, eliminar y actualizar formato condicional en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="Establecer el valor de una celda" rel="noopener">Establecer valor de celda en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Fila/Columna: Insertar, Eliminar, Copiar, Ocultar y Ajustar automáticamente</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="Insertar una fila vacía en una hoja de cálculo" rel="noopener">Agregar una fila vacía en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="Eliminar una fila de una hoja de cálculo" rel="noopener">Eliminar una fila de una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="Copiar filas dentro de una hoja de cálculo" rel="noopener">Copiar filas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="Ocultar filas en una hoja de cálculo" rel="noopener">Ocultar filas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="Ajustar automáticamente filas en un libro" rel="noopener">Ajustar automáticamente filas en un libro de Excel.</a></li>
            <li><a href="/cells/columns/add/" title="Insertar una columna vacía en una hoja de cálculo" rel="noopener">Agregar una columna vacía en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/columns/delete/" title="Eliminar una columna de una hoja de cálculo" rel="noopener">Eliminar una columna de una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/columns/copy/" title="Copiar columnas dentro de una hoja de cálculo" rel="noopener">Copiar columnas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/columns/hide/" title="Ocultar columnas en una hoja de cálculo" rel="noopener">Ocultar columnas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/columns/autofit/" title="Ajustar automáticamente columnas en un libro" rel="noopener">Ajustar automáticamente columnas en un libro de Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>Gráfico</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="Agregar un gráfico a una hoja de cálculo" rel="noopener">Agregar un gráfico en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="Eliminar un gráfico de una hoja de cálculo" rel="noopener">Eliminar un gráfico en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="Eliminar todos los gráficos de una hoja de cálculo" rel="noopener">Eliminar todos los gráficos en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="Convertir un gráfico a un archivo de imagen" rel="noopener">Convertir un gráfico a una imagen.</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="Ocultar la leyenda de un gráfico" rel="noopener">Ocultar leyenda de gráfico en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="Actualizar el título de un gráfico" rel="noopener">Actualizar título de gráfico en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="Eliminar el título de un gráfico" rel="noopener">Eliminar título de gráfico en una hoja de cálculo.</a></li>
        </ul>
        <p>Tabla</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Agregar una tabla (objeto de lista) a una hoja de cálculo" rel="noopener">Agregar un objeto de lista en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Actualizar una tabla en una hoja de cálculo" rel="noopener">Actualizar un objeto de lista en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="Convertir una tabla en un rango" rel="noopener">Convertir un objeto de lista en un rango.</a></li>
            <li><a href="/cells/sort-table-data/" title="Ordenar datos dentro de una tabla" rel="noopener">Ordenar datos de tabla.</a></li>
        </ul>
        <p>Objeto OLE</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="Agregar un objeto OLE a una hoja de cálculo" rel="noopener">Agregar objeto OLE en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Actualizar un objeto OLE específico" rel="noopener">Actualizar un objeto OLE específico en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="Convertir un objeto OLE a una imagen" rel="noopener">Convertir objeto OLE a imagen.</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="Eliminar todos los objetos OLE de una hoja de cálculo" rel="noopener">Eliminar todos los objetos OLE en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Eliminar un objeto OLE específico" rel="noopener">Eliminar un objeto OLE específico en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Forma</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="Agregar una forma a una hoja de cálculo" rel="noopener">Agregar una forma en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="Eliminar todas las formas de una hoja de cálculo" rel="noopener">Eliminar todas las formas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="Eliminar una forma por su índice" rel="noopener">Eliminar una forma por índice en una hoja de cálculo de Excel.</a></li>
        </ul>
        <p>Tabla dinámica</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="Agregar una tabla dinámica a una hoja de cálculo" rel="noopener">Agregar una tabla dinámica en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="Eliminar todas las tablas dinámicas de una hoja de cálculo" rel="noopener">Eliminar todas las tablas dinámicas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="Eliminar una tabla dinámica por su índice" rel="noopener">Eliminar una tabla dinámica por índice en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="Actualizar estilo de celda en una tabla dinámica" rel="noopener">Actualizar estilo de celda de una tabla dinámica en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="Actualizar el estilo general de una tabla dinámica" rel="noopener">Actualizar estilo de una tabla dinámica en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="Trabajar con filtros de tablas dinámicas" rel="noopener">Trabajar con filtros de tablas dinámicas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="Ocultar un elemento de campo de tabla dinámica" rel="noopener">Ocultar elementos de campo de tabla dinámica en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/move-pivot-table/" title="Mover una tabla dinámica dentro de una hoja de cálculo" rel="noopener">Mover una tabla dinámica en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>Salto de página</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="Insertar un salto de página horizontal" rel="noopener">Insertar un salto de página horizontal en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="Insertar un salto de página vertical" rel="noopener">Insertar un salto de página vertical en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="Eliminar un salto de página horizontal" rel="noopener">Eliminar un salto de página horizontal en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="Eliminar un salto de página vertical" rel="noopener">Eliminar un salto de página vertical en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Configuración de página</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>Calcular</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="Calcular todas las fórmulas en un libro" rel="noopener">Calcular todas las fórmulas en un libro de Excel.</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="Calcular la fórmula de una celda específica" rel="noopener">Calcular fórmulas de celdas en un libro de Excel.</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="Calcular una fórmula en una hoja de cálculo" rel="noopener">Calcular una fórmula en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Nombre</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>Esquema</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="Agrupar filas en una hoja de cálculo" rel="noopener">Agrupar filas en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="Desagrupar filas en una hoja de cálculo" rel="noopener">Desagrupar filas en una hoja de cálculo de Excel.</a></li>
        </ul>
        <p>Filtro</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="Agregar un filtro a una columna" rel="noopener">Agregar un filtro para una columna en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="Eliminar un filtro de columna" rel="noopener">Eliminar un filtro para una columna en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="Eliminar un filtro de fecha" rel="noopener">Eliminar un filtro de fecha en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="Agregar un filtro por icono" rel="noopener">Agregar un filtro por icono en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="Agregar un filtro de fecha" rel="noopener">Agregar un filtro de fecha en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="Filtrar datos mediante Filtro automático" rel="noopener">Filtrar datos mediante Filtro automático en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="Filtrar los 10 primeros elementos" rel="noopener">Filtrar los 10 primeros elementos de la lista en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="Coincidir todas las celdas en blanco" rel="noopener">Coincidir todas las celdas en blanco de la lista en una hoja de cálculo de Excel.</a></li>
        </ul>
        <p>Ordenar</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="Ordenar datos de la hoja de cálculo" rel="noopener">Ordenar datos en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Importar datos</p>
        <ul>
            <li><a href="/cells/import/" title="Importar datos a archivos de Excel" rel="noopener">Importar datos a archivos de Excel.</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="Importar datos CSV a una hoja de cálculo" rel="noopener">Importar datos CSV a una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/import/picture/" title="Importar una imagen a una hoja de cálculo" rel="noopener">Importar una imagen a una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/import/double-array/" title="Importar una matriz doble a una hoja de cálculo" rel="noopener">Importar una matriz doble a una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/import/integer-array/" title="Importar una matriz entera a una hoja de cálculo" rel="noopener">Importar una matriz entera a una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/import/string-array/" title="Importar una matriz de cadenas a una hoja de cálculo" rel="noopener">Importar una matriz de cadenas a una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/import/with-using-storage/" title="Importar datos utilizando almacenamiento" rel="noopener">Importar datos a una hoja de cálculo de Excel utilizando almacenamiento.</a></li>
            <li><a href="/cells/import/without-using-storage/" title="Importar datos sin utilizar almacenamiento" rel="noopener">Importar datos a una hoja de cálculo de Excel sin utilizar almacenamiento.</a></li>
        </ul>
        <p>Ensamblado</p>
        <ul>
            <li><a href="/cells/assembly/" title="Ensamblar datos en archivos de Excel" rel="noopener">Ensamblar datos en archivos de Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>Comentarios</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Agregar un comentario a una celda" rel="noopener">Agregar un comentario a una celda en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="Actualizar un comentario de celda" rel="noopener">Actualizar un comentario en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="Eliminar todos los comentarios en una hoja de cálculo" rel="noopener">Eliminar todos los comentarios en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Cambios</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="Proteger un libro de Excel" rel="noopener">Proteger un libro de Excel.</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="Quitar protección a un libro de Excel" rel="noopener">Quitar protección a un libro de Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>Ventanas</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="Congelar paneles en una hoja de cálculo" rel="noopener">Congelar paneles en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="Descongelar paneles en una hoja de cálculo" rel="noopener">Descongelar paneles en una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="Ocultar una hoja de cálculo" rel="noopener">Ocultar una hoja de cálculo de Excel.</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="Mostrar una hoja de cálculo" rel="noopener">Mostrar una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Zoom</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="Establecer nivel de zoom de la hoja de cálculo" rel="noopener">Establecer zoom en una hoja de cálculo de Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

## {{< /tabs >}}