---
title: Opción Convertir libro de trabajo
second_title: Documen
linktitle: Opción Convertir libro de trabajo
type: docs
url: /es/convert-workbook-options/
keywords: ConvertWorkbookOptions
description: Aspose.Cells Cloud REST API admite la conversión de archivos de Excel a diversos formatos. El SDK es compatible con diversos lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 79
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, JSON, Markdown, Opciones de conversión de libro de trabajo
---
# Propiedades de ConvertWorkbookOptions

Nombre | Tipo | Descripción | Notas
------------ | ------------- | ------------- | -------------
**Fuente de datos** | **Objeto** Fuente del archivo de datos: CloudFileSystem, RequestFiles, HttpUri. |
**[Información del archivo](/celdas/información-del-archivo/)** | **Objeto** | Descripción de la información del archivo. Incluye nombre de archivo, tamaño de archivo y contenido del archivo (cadena base64). |
**[Configuración de página](/celdas/configuración-de-página/)** | **Objeto** | Propiedades de configuración de página. |
**Opciones de guardado** | **Objeto** | Opciones de guardado: DbfSaveOptions, DifSaveOptions, DocxSaveOptions, HtmlSaveOptions, XlsSaveOptions, XlsxSaveOptions, XpsSaveOptions, PngSaveOptions, JpgSaveOptions, GifSaveOptions, EmfSaveOptions, BmpSaveOptions, MdSaveOptions, NumbersSaveOptions, WmfSaveOptions, SvgSaveOptions, TxtSaveOptions, TifSaveOptions, XlsbSaveOptions |
**Convertir formato** | **cadena** | El formato de archivo: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, etc. |
**Comprobar restricción de Excel** | **booleano** | Obtiene y establece el tipo de texto ajustado automáticamente. |

## **Propiedades de fileSource**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Tipo de origen del archivo|Cadena|verdadero| FALSO||Una propiedad denominada FileSourceType del tipo FileSourceType a la que se puede acceder y modificar. (CloudFileSystem/RequestFiles/HttpUri)|
|Ruta de archivo|Cadena|verdadero| FALSO||La ruta de posición del archivo.|

## **Propiedades de DbfSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Exportar como cadena|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de DifSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de DocxSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Fuente predeterminada|Cadena|verdadero| FALSO|||
|Comprobar fuente predeterminada del libro de trabajo|Booleano|verdadero| FALSO|||
|Comprobar compatibilidad de fuentes|Booleano|verdadero| FALSO|||
|IsFontSubstitutionCharGranularity|Booleano|verdadero| FALSO|||
|Una página por hoja|Booleano|verdadero| FALSO|||
|Todas las columnas en una página por hoja|Booleano|verdadero| FALSO|||
|IgnorarError|Booleano|verdadero| FALSO|||
|SalidaPáginaEnBlancoCuandoNoHayNadaQueImprimir|Booleano|verdadero| FALSO|||
|Índice de páginas|Entero|verdadero| FALSO|||
|Número de páginas|Entero|verdadero| FALSO|||
|Tipo de página de impresión|Cadena|verdadero| FALSO|||
|Tipo de línea de cuadrícula|Cadena|verdadero| FALSO|||
|TextoCrossType|Cadena|verdadero| FALSO|||
|Idioma de edición predeterminado|Cadena|verdadero| FALSO|||
|Configuración de renderizado de Emf|Cadena|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de HtmlSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Exportar encabezados de página|Booleano|verdadero| FALSO|||
|Exportar pies de página|Booleano|verdadero| FALSO|||
|Exportar encabezados de fila y columna|Booleano|verdadero| FALSO|||
|Mostrar todas las hojas|Booleano|verdadero| FALSO|||
|Opciones de imagen|Clase|verdadero| FALSO|||
|Guardar como archivo único|Booleano|verdadero| FALSO|||
|Exportar hoja de trabajo oculta|Booleano|verdadero| FALSO|||
|Exportar líneas de cuadrícula|Booleano|verdadero| FALSO|||
|Preferencia de presentación|Booleano|verdadero| FALSO|||
|PrefijoCellCss|Cadena|verdadero| FALSO|||
|ID de CSS de tabla|Cadena|verdadero| FALSO|||
|IsFullPathLink|Booleano|verdadero| FALSO|||
|Exportar hoja de trabajo CSS por separado|Booleano|verdadero| FALSO|||
|Exportar estilo de borde similar|Booleano|verdadero| FALSO|||
|FusionarVacíoTdForzadamente|Booleano|verdadero| FALSO|||
|Exportar coordenadas de celda|Booleano|verdadero| FALSO|||
|Exportar encabezados adicionales|Booleano|verdadero| FALSO|||
|ExportHeadings|Booleano|verdadero| FALSO|||
|Fórmula de exportación|Booleano|verdadero| FALSO|||
|Agregar texto de información sobre herramientas|Booleano|verdadero| FALSO|||
|Exportar datos de filas falsas|Booleano|verdadero| FALSO|||
|Excluir estilos no utilizados|Booleano|verdadero| FALSO|||
|ExportarPropiedadesDeDocumento|Booleano|verdadero| FALSO|||
|ExportarPropiedadesDeLaHojaDeTrabajo|Booleano|verdadero| FALSO|||
|ExportarPropiedades del Libro de Trabajo|Booleano|verdadero| FALSO|||
|Exportar scripts y propiedades de marcos|Booleano|verdadero| FALSO|||
|Directorio de archivos adjuntos|Cadena|verdadero| FALSO|||
|Prefijo de URL de archivos adjuntos|Cadena|verdadero| FALSO|||
|Codificación|Cadena|verdadero| FALSO|||
|ExportarSoloHojaDeTrabajoActiva|Booleano|verdadero| FALSO|||
|Formato de imagen de gráfico de exportación|Cadena|verdadero| FALSO|||
|Exportar imágenes como base 64|Booleano|verdadero| FALSO|||
|Tipo de visualización de columna oculta|Cadena|verdadero| FALSO|||
|Tipo de visualización de fila oculta|Cadena|verdadero| FALSO|||
|Tipo de cadena cruzada HTML|Cadena|verdadero| FALSO|||
|IsExpImageToTempDir|Booleano|verdadero| FALSO|||
|Título de la página|Cadena|verdadero| FALSO|||
|Analizar etiqueta HTML en celda|Booleano|verdadero| FALSO|||
|Atributo CellName|Cadena|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de ImageSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Tipo de imagen del gráfico|Cadena|verdadero| FALSO|||
|Nombre de imagen incrustada en SVG|Cadena|verdadero| FALSO|||
|Resolución horizontal|Entero|verdadero| FALSO|||
|Formato de imagen|Cadena|verdadero| FALSO|||
|IsCellAutoFit|Booleano|verdadero| FALSO|||
|Una página por hoja|Booleano|verdadero| FALSO|||
|OnlyArea|Booleano|verdadero| FALSO|||
|Página de impresión|Cadena|verdadero| FALSO|||
|Cuadro de diálogo Imprimir con estado|Booleano|verdadero| FALSO|||
|Calidad|Entero|verdadero| FALSO|||
|TiffCompresión|Cadena|verdadero| FALSO|||
|Resolución vertical|Entero|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de JsonSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Área de exportación|Clase|verdadero| FALSO|||
|TieneFilaDeEncabezado|Booleano|verdadero| FALSO|||
|Exportar como cadena|Booleano|verdadero| FALSO|||
|Sangrar|Cadena|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de MarkdownSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Codificación|Cadena|verdadero| FALSO|||
|Estrategia de formato|Cadena|verdadero| FALSO|||
|Separador de línea|Cadena|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de OoxmlSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|ExportCellName|Booleano|verdadero| FALSO|||
|ActualizarZoom|Booleano|verdadero| FALSO|||
|HabilitarZip64|Booleano|verdadero| FALSO|||
|Incrustar OoxmlAsOleObject|Booleano|verdadero| FALSO|||
|Tipo de compresión|Cadena|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de PclSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|nombreDeFuenteCompleto|Cadena|verdadero| FALSO|||
|nombrePcl de fuente|Cadena|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de PdfSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Mostrar título del documento|Booleano|verdadero| FALSO|||
|ExportarEstructuraDeDocumento|Booleano|verdadero| FALSO|||
|Configuración de renderizado de Emf|Cadena|verdadero| FALSO|||
|Exportación de propiedades personalizadas|Cadena|verdadero| FALSO|||
|Tipo de optimización|Cadena|verdadero| FALSO|||
|Productor|Cadena|verdadero| FALSO|||
|Compresión de PDF|Cadena|verdadero| FALSO|||
|Codificación de fuentes|Cadena|verdadero| FALSO|||
|Filigrana|Clase|verdadero| FALSO|||
|CalcularFórmula|Booleano|verdadero| FALSO|||
|Comprobar compatibilidad de fuentes|Booleano|verdadero| FALSO|||
|Cumplimiento|Cadena|verdadero| FALSO|||
|Fuente predeterminada|Cadena|verdadero| FALSO|||
|Una página por hoja|Booleano|verdadero| FALSO|||
|Tipo de página de impresión|Cadena|verdadero| FALSO|||
|Opciones de seguridad|Clase|verdadero| FALSO|||
|PPI deseado|Entero|verdadero| FALSO|||
|Calidad jpeg|Entero|verdadero| FALSO|||
|Tipo de imagen|Cadena|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de PptxSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Ignorar filas ocultas|Booleano|verdadero| FALSO|||
|Ajustar tamaño de fuente para tipo de fila|Cadena|verdadero| FALSO|||
|Tipo de vista de exportación|Cadena|verdadero| FALSO|||
|Fuente predeterminada|Cadena|verdadero| FALSO|||
|Comprobar fuente predeterminada del libro de trabajo|Booleano|verdadero| FALSO|||
|Comprobar compatibilidad de fuentes|Booleano|verdadero| FALSO|||
|IsFontSubstitutionCharGranularity|Booleano|verdadero| FALSO|||
|Una página por hoja|Booleano|verdadero| FALSO|||
|Todas las columnas en una página por hoja|Booleano|verdadero| FALSO|||
|IgnorarError|Booleano|verdadero| FALSO|||
|SalidaPáginaEnBlancoCuandoNoHayNadaQueImprimir|Booleano|verdadero| FALSO|||
|Índice de páginas|Entero|verdadero| FALSO|||
|Número de páginas|Entero|verdadero| FALSO|||
|Tipo de página de impresión|Cadena|verdadero| FALSO|||
|Tipo de línea de cuadrícula|Cadena|verdadero| FALSO|||
|TextoCrossType|Cadena|verdadero| FALSO|||
|Idioma de edición predeterminado|Cadena|verdadero| FALSO|||
|Configuración de renderizado de Emf|Cadena|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de SqlScriptSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Comprobar si existe tabla|Booleano|verdadero| FALSO|||
|Mapa de tipos de columnas|Cadena|verdadero| FALSO|||
|Comprobar todos los datos para el tipo de columna|Booleano|verdadero| FALSO|||
|Agregar línea en blanco entre filas|Booleano|verdadero| FALSO|||
|Separador|Cadena|verdadero| FALSO|||
|Tipo de operador|Cadena|verdadero| FALSO|||
|Clave principal|Entero|verdadero| FALSO|||
|Crear tabla|Booleano|verdadero| FALSO|||
|IdNombre|Cadena|verdadero| FALSO|||
|Identificación de inicio|Entero|verdadero| FALSO|||
|Nombre de la tabla|Cadena|verdadero| FALSO|||
|Exportar como cadena|Booleano|verdadero| FALSO|||
|Área de exportación|Clase|verdadero| FALSO|||
|TieneFilaDeEncabezado|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de SvgSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Índice de hoja|Entero|verdadero| FALSO|||
|Tipo de imagen del gráfico|Cadena|verdadero| FALSO|||
|Nombre de imagen incrustada en SVG|Cadena|verdadero| FALSO|||
|Resolución horizontal|Entero|verdadero| FALSO|||
|Formato de imagen|Cadena|verdadero| FALSO|||
|IsCellAutoFit|Booleano|verdadero| FALSO|||
|Una página por hoja|Booleano|verdadero| FALSO|||
|OnlyArea|Booleano|verdadero| FALSO|||
|Página de impresión|Cadena|verdadero| FALSO|||
|Cuadro de diálogo Imprimir con estado|Booleano|verdadero| FALSO|||
|Calidad|Entero|verdadero| FALSO|||
|TiffCompresión|Cadena|verdadero| FALSO|||
|Resolución vertical|Entero|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de TxtSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Tipo de cotización|Cadena|verdadero| FALSO|||
|Separador|Cadena|verdadero| FALSO|||
|Cadena separadora|Cadena|verdadero| FALSO|||
|Siempre citado|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de XlsSaveOptions y XlsbSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|MatchColor|Booleano|verdadero| FALSO|||
|Compatibilidad con Wps|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de XmlSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Índices de hojas|Formación|verdadero| FALSO|||
|Área de exportación|Clase|verdadero| FALSO|||
|TieneFilaDeEncabezado|Booleano|verdadero| FALSO|||
|Nombre del mapa XML|Cadena|verdadero| FALSO|||
|NombreDeHojaComoNombreDeElemento|Booleano|verdadero| FALSO|||
|Datos como atributo|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||

## **Propiedades de XpsSaveOptions**

| Nombre de la propiedad| Tipo de propiedad| Nullable| Sólo lectura| Valor predeterminado| Descripción|
|:- |:- |:- |:- |:- |:- |
|Fuente predeterminada|Cadena|verdadero| FALSO|||
|Comprobar fuente predeterminada del libro de trabajo|Booleano|verdadero| FALSO|||
|Comprobar compatibilidad de fuentes|Booleano|verdadero| FALSO|||
|IsFontSubstitutionCharGranularity|Booleano|verdadero| FALSO|||
|Una página por hoja|Booleano|verdadero| FALSO|||
|Todas las columnas en una página por hoja|Booleano|verdadero| FALSO|||
|IgnorarError|Booleano|verdadero| FALSO|||
|SalidaPáginaEnBlancoCuandoNoHayNadaQueImprimir|Booleano|verdadero| FALSO|||
|Índice de páginas|Entero|verdadero| FALSO|||
|Número de páginas|Entero|verdadero| FALSO|||
|Tipo de página de impresión|Cadena|verdadero| FALSO|||
|Tipo de línea de cuadrícula|Cadena|verdadero| FALSO|||
|TextoCrossType|Cadena|verdadero| FALSO|||
|Idioma de edición predeterminado|Cadena|verdadero| FALSO|||
|Configuración de renderizado de Emf|Cadena|verdadero| FALSO|||
|Áreas de fusión|Booleano|verdadero| FALSO|||
|Ordenar nombres externos|Booleano|verdadero| FALSO|||
|ActualizarSmartArt|Booleano|verdadero| FALSO|||
|Guardar formato|Cadena|verdadero| FALSO|||
|Carpeta de archivos en caché|Cadena|verdadero| FALSO|||
|ClearData|Booleano|verdadero| FALSO|||
|Crear directorio|Booleano|verdadero| FALSO|||
|Habilitar compresión HTTP|Booleano|verdadero| FALSO|||
|Actualizar caché de gráficos|Booleano|verdadero| FALSO|||
|Nombres de clasificación|Booleano|verdadero| FALSO|||
|ValidarÁreasFusionadas|Booleano|verdadero| FALSO|||
|Comprobar restricción de Excel|Booleano|verdadero| FALSO|||
|Propiedades del documento cifrado|Booleano|verdadero| FALSO|||
