---
title: "Opciones de conversión de libro"
second_title: "Documentos"
linktitle: "Opciones de conversión de libro"
type: docs
url: /es/convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, conversión de Excel, PDF, CSV, API"
description: "Opciones de conversión de libro: configure la conversión de libros de Excel a PDF, CSV, HTML y otros formatos mediante la API de Aspose.Cells Cloud."
weight: 79
ArticleTitle: "Opciones de conversión de libro – API de Aspose.Cells Cloud"
---

# Propiedades de ConvertWorkbookOptions

**Versión de la API:** 23.12 (2024‑03)

`ConvertWorkbookOptions` es el modelo de solicitud utilizado por la API de conversión de Aspose.Cells Cloud para especificar cómo debe transformarse un libro de Excel a otro formato (PDF, CSV, HTML, etc.). Agrupa la información del archivo de origen, el formato de destino, las configuraciones de configuración de página y las opciones de guardado específicas del formato.

| Nombre                              | Tipo        | Descripción                                                                                                   | Notas |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | Origen del archivo de datos: `CloudFileSystem`, `RequestFiles` o `HttpUri`.                                   |       |
| **[FileInfo](/cells/file-info/)**   | **Object**  | Describe el nombre del archivo, su tamaño y el contenido codificado en base64.                                |       |
| **[PageSetup](/cells/page-setup/)** | **Object**  | Propiedades de configuración de página, como márgenes, orientación y escala.                                  |       |
| **SaveOptions**                     | **Object**  | Contenedor para objetos de opciones de guardado específicos por formato (por ejemplo, `PdfSaveOptions`, `HtmlSaveOptions`). |       |
| **ConvertFormat**                   | **string**  | Formato de archivo de destino (por ejemplo, **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF**, etc.).            |       |
| **CheckExcelRestriction**           | **boolean** | Obtiene o establece si se deben aplicar restricciones específicas de Excel (máximo de filas, columnas, longitud de nombre de hoja, etc.). |       |

**Requisitos previos**

- Obtenga un token de acceso válido de OAuth 2.0 para Aspose.Cells Cloud.  
- Asegúrese de que el archivo de origen esté accesible mediante uno de los tipos compatibles de `DataSource`.

**Ejemplo rápido**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Ejemplo.xlsx",
      "FileContent": "<contenido‑en‑base64>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Ejemplo.pdf
```

**Detalles de la solicitud a la API**

La operación de conversión se ejecuta mediante una solicitud **POST** a la siguiente ruta:

```
https://api.aspose.cloud/v3.0/cells/convert
```

Encabezados obligatorios:

| Encabezado            | Valor                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

El cuerpo de la solicitud debe ser una representación JSON de `ConvertWorkbookOptions` (véase el ejemplo anterior). Todas las propiedades son opcionales, salvo que se requieran por el `ConvertFormat` seleccionado.

**Respuesta de la API**

Una conversión correcta devuelve **HTTP 200 OK** (o **202 Accepted** para procesamiento asíncrono), con el archivo convertido transmitido en el cuerpo de la respuesta. Cuando la respuesta se transmite como flujo, el encabezado `Content-Disposition` contiene el nombre de archivo sugerido.

Ejemplo de respuesta JSON para una solicitud asíncrona:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**Códigos de estado**

| Código | Significado                                         |
|--------|-----------------------------------------------------|
| 200    | Conversión completada; archivo devuelto.           |
| 202    | Conversión aceptada; resultado disponible más adelante. |
| 400    | Solicitud incorrecta: faltan o son inválidos los parámetros. |
| 401    | No autorizado: token inválido o ausente.            |
| 403    | Prohibido: permisos insuficientes.                  |
| 500    | Error interno del servidor.                         |

**Notas / Limitaciones**

- La marca `CheckExcelRestriction` aplica límites específicos de Excel, como el número máximo de filas (1 048 576) y columnas (16 384).  
- No todos los formatos de destino admiten todas las propiedades de `SaveOptions`; las opciones no admitidas se ignoran.  
- Al utilizar `HttpUri` como origen de datos, la URL debe ser accesible públicamente sin autenticación.  
- Se han añadido la información del método y la ruta de la API para mejorar la claridad del desarrollador y reducir errores de integración.  

## Propiedades de FileSource

| Nombre de la propiedad | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                                               |
| ---------------------- | ----------------- | -------- | -------- | -------------------- | ------------------------------------------------------------------------- |
| FileSourceType         | String            | true     | false    |                      | Indica el tipo de origen (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath               | String            | true     | false    |                      | Ruta de ubicación del archivo.                                            |

## Propiedades de DbfSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                         |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------- |
| ExportAsString            | Boolean           | true     | false    |                      | Cuando es **true**, exporta valores numéricos como cadenas. |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos DBF.       |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.       |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.        |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.     |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.  |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.     |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.           |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.             |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de DifSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                         |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------- |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos DIF.       |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.       |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.        |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.     |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.  |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.     |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.           |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.             |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de DocxSaveOptions

| Nombre de la propiedad            | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                            |
| --------------------------------- | ----------------- | -------- | -------- | -------------------- | ------------------------------------------------------ |
| DefaultFont                       | String            | true     | false    |                      | Fuente utilizada cuando una fuente de origen no está disponible. |
| CheckWorkbookDefaultFont          | Boolean           | true     | false    |                      | Comprueba si se aplica la fuente predeterminada del libro. |
| CheckFontCompatibility            | Boolean           | true     | false    |                      | Valida la compatibilidad de fuentes para el formato de destino. |
| IsFontSubstitutionCharGranularity | Boolean           | true     | false    |                      | Controla la sustitución de fuentes a nivel de carácter. |
| OnePagePerSheet                   | Boolean           | true     | false    |                      | Fuerza que cada hoja se coloque en una página independiente. |
| AllColumnsInOnePagePerSheet       | Boolean           | true     | false    |                      | Ajusta todas las columnas de una hoja en una sola página. |
| IgnoreError                       | Boolean           | true     | false    |                      | Ignora errores no críticos durante la conversión.     |
| OutputBlankPageWhenNothingToPrint | Boolean           | true     | false    |                      | Genera una página en blanco si no hay nada que representar. |
| PageIndex                         | Integer           | true     | false    |                      | Índice de la primera página a exportar.               |
| PageCount                         | Integer           | true     | false    |                      | Número de páginas a exportar.                         |
| PrintingPageType                  | String            | true     | false    |                      | Especifica el tipo de página para impresión.          |
| GridlineType                      | String            | true     | false    |                      | Determina cómo se renderizan las líneas de cuadrícula. |
| TextCrossType                     | String            | true     | false    |                      | Define el tipo de cruce para el renderizado de texto. |
| DefaultEditLanguage               | String            | true     | false    |                      | Idioma predeterminado para la edición de texto.       |
| EmfRenderSetting                  | String            | true     | false    |                      | Configuración para el renderizado de EMF.             |
| MergeAreas                        | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.              |
| SortExternalNames                 | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.               |
| UpdateSmartArt                    | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| SaveFormat                        | String            | true     | false    |                      | Identificador del formato para archivos DOCX.        |
| CachedFileFolder                  | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.  |
| ClearData                         | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.          |
| CreateDirectory                   | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.           |
| EnableHttpCompression             | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.        |
| RefreshChartCache                 | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                         | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.     |
| ValidateMergedAreas               | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.        |
| CheckExcelRestriction             | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| EncryptDocumentProperties         | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de HtmlSaveOptions

| Nombre de la propiedad          | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                            |
| ------------------------------- | ----------------- | -------- | -------- | -------------------- | ------------------------------------------------------ |
| ExportPageHeaders               | Boolean           | true     | false    |                      | Incluye encabezados de página en la salida HTML.      |
| ExportPageFooters               | Boolean           | true     | false    |                      | Incluye pies de página en la salida HTML.             |
| ExportRowColumnHeadings         | Boolean           | true     | false    |                      | Exporta encabezados de filas y columnas.              |
| ShowAllSheets                   | Boolean           | true     | false    |                      | Muestra todas las hojas de cálculo en un solo archivo HTML. |
| ImageOptions                    | Clase             | true     | false    |                      | Configuración que controla el renderizado de imágenes. |
| SaveAsSingleFile                | Boolean           | true     | false    |                      | Guarda todo el libro como un único archivo HTML.      |
| ExportHiddenWorksheet           | Boolean           | true     | false    |                      | Incluye hojas de cálculo ocultas en la exportación.   |
| ExportGridLines                 | Boolean           | true     | false    |                      | Renderiza líneas de cuadrícula en la salida HTML.     |
| PresentationPreference          | Boolean           | true     | false    |                      | Optimiza el HTML para el modo de presentación.        |
| CellCssPrefix                   | String            | true     | false    |                      | Prefijo añadido a los nombres de clases CSS generadas para celdas. |
| TableCssId                      | String            | true     | false    |                      | Atributo ID para la tabla HTML generada.              |
| IsFullPathLink                  | Boolean           | true     | false    |                      | Genera hipervínculos de ruta completa para los recursos. |
| ExportWorksheetCSSSeparately    | Boolean           | true     | false    |                      | Coloca el CSS de cada hoja en un archivo independiente. |
| ExportSimilarBorderStyle        | Boolean           | true     | false    |                      | Fusiona estilos de borde similares para reducir el tamaño del CSS. |
| MergeEmptyTdForcely             | Boolean           | true     | false    |                      | Fuerza la fusión de elementos `<td>` vacíos.          |
| ExportCellCoordinate            | Boolean           | true     | false    |                      | Incluye coordenadas de celda (por ejemplo, A1) en el HTML. |
| ExportExtraHeadings             | Boolean           | true     | false    |                      | Añade filas/columnas de encabezado adicionales si es necesario. |
| ExportHeadings                  | Boolean           | true     | false    |                      | Exporta encabezados de filas y columnas.              |
| ExportFormula                   | Boolean           | true     | false    |                      | Muestra fórmulas en lugar de valores calculados.      |
| AddTooltipText                  | Boolean           | true     | false    |                      | Añade información emergente con comentarios de celda. |
| ExportBogusRowData              | Boolean           | true     | false    |                      | Incluye filas de marcador de posición para datos vacíos. |
| ExcludeUnusedStyles             | Boolean           | true     | false    |                      | Elimina estilos CSS no utilizados.                    |
| ExportDocumentProperties        | Boolean           | true     | false    |                      | Escribe propiedades de documento en etiquetas meta HTML. |
| ExportWorksheetProperties       | Boolean           | true     | false    |                      | Escribe propiedades de hoja en HTML.                  |
| ExportWorkbookProperties        | Boolean           | true     | false    |                      | Escribe propiedades de libro en HTML.                 |
| ExportFrameScriptsAndProperties | Boolean           | true     | false    |                      | Incluye scripts y propiedades para marcos.            |
| AttachedFilesDirectory          | String            | true     | false    |                      | Ruta de directorio para archivos adjuntos.            |
| AttachedFilesUrlPrefix          | String            | true     | false    |                      | Prefijo de URL para archivos adjuntos.                |
| Encoding                        | String            | true     | false    |                      | Codificación de caracteres para el archivo HTML.      |
| ExportActiveWorksheetOnly       | Boolean           | true     | false    |                      | Exporta solo la hoja activa.                          |
| ExportChartImageFormat          | String            | true     | false    |                      | Formato de imagen utilizado para gráficos incrustados. |
| ExportImagesAsBase64            | Boolean           | true     | false    |                      | Codifica imágenes como cadenas en Base64.             |
| HiddenColDisplayType            | String            | true     | false    |                      | Cómo se muestran las columnas ocultas.                |
| HiddenRowDisplayType            | String            | true     | false    |                      | Cómo se muestran las filas ocultas.                   |
| HtmlCrossStringType             | String            | true     | false    |                      | Determina cómo se renderizan los datos de cruce de cadena. |
| IsExpImageToTempDir             | Boolean           | true     | false    |                      | Exporta imágenes a un directorio temporal.            |
| PageTitle                       | String            | true     | false    |                      | Título utilizado para la página HTML generada.        |
| ParseHtmlTagInCell              | Boolean           | true     | false    |                      | Analiza etiquetas HTML presentes en los valores de celda. |
| CellNameAttribute               | String            | true     | false    |                      | Nombre del atributo que contiene la referencia de celda. |
| SaveFormat                      | String            | true     | false    |                      | Identificador del formato para archivos HTML.         |
| CachedFileFolder                | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.  |
| ClearData                       | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.          |
| CreateDirectory                 | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.           |
| EnableHttpCompression           | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.        |
| RefreshChartCache               | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                       | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.     |
| ValidateMergedAreas             | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.        |
| MergeAreas                      | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.              |
| SortExternalNames               | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.               |
| CheckExcelRestriction           | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt                  | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties         | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de ImageSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                         |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------- |
| ChartImageType            | String            | true     | false    |                      | Formato de imagen utilizado para renderizar gráficos. |
| EmbeddedImageNameInSvg    | String            | true     | false    |                      | Nombre asignado a las imágenes incrustadas en la salida SVG. |
| HorizontalResolution      | Integer           | true     | false    |                      | DPI horizontal de la imagen exportada.             |
| ImageFormat               | String            | true     | false    |                      | Formato de imagen de destino (PNG, JPG, etc.).     |
| IsCellAutoFit             | Boolean           | true     | false    |                      | Ajusta automáticamente el contenido de celda al tamaño de la imagen. |
| OnePagePerSheet           | Boolean           | true     | false    |                      | Renderiza cada hoja en una página independiente.   |
| OnlyArea                  | Boolean           | true     | false    |                      | Exporta solo el área definida de la hoja.          |
| PrintingPage              | String            | true     | false    |                      | Diseño de página utilizado para impresión.          |
| PrintWithStatusDialog     | Boolean           | true     | false    |                      | Muestra un diálogo de estado durante la impresión.  |
| Quality                   | Integer           | true     | false    |                      | Calidad de compresión para imágenes JPEG (0‑100).   |
| TiffCompression           | String            | true     | false    |                      | Tipo de compresión para imágenes TIFF.             |
| VerticalResolution        | Integer           | true     | false    |                      | DPI vertical de la imagen exportada.               |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos de imagen.  |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.       |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.        |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.     |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.  |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.     |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.           |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.             |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de JsonSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                              |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | -------------------------------------------------------- |
| ExportArea                | Clase             | true     | false    |                      | Define el área de la hoja a exportar.                   |
| HasHeaderRow              | Boolean           | true     | false    |                      | Indica si la primera fila contiene encabezados de columna. |
| ExportAsString            | Boolean           | true     | false    |                      | Exporta todos los valores como cadenas.                 |
| Indent                    | String            | true     | false    |                      | Cadena utilizada para la sangría (por ejemplo, dos espacios). |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos JSON.           |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.    |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.            |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.             |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.          |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.       |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.          |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.                |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.                 |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de MarkdownSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                                     |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------------------- |
| Encoding                  | String            | true     | false    |                      | Codificación de caracteres para el archivo markdown.           |
| FormatStrategy            | String            | true     | false    |                      | Estrategia utilizada para formatear markdown (por ejemplo, GitHub, CommonMark). |
| LineSeparator             | String            | true     | false    |                      | Carácter(es) de salto de línea a utilizar.                     |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos markdown.              |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.           |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.                   |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.                    |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.                 |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.              |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.                 |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.                       |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.                        |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión.     |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente.      |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida.   |

## Propiedades de OoxmlSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                          |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean           | true     | false    |                      | Incluye nombres de celda en el archivo exportado.   |
| UpdateZoom                | Boolean           | true     | false    |                      | Actualiza el nivel de zoom en el documento de salida. |
| EnableZip64               | Boolean           | true     | false    |                      | Habilita extensiones ZIP64 para archivos grandes.   |
| EmbedOoxmlAsOleObject     | Boolean           | true     | false    |                      | Incrusta OOXML como un objeto OLE.                  |
| CompressionType           | String            | true     | false    |                      | Tipo de compresión aplicada (por ejemplo, Normal, Máxima). |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos OOXML.      |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.        |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.         |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.      |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.   |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.      |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.            |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.             |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de PclSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                         |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------- |
| fontFullName              | String            | true     | false    |                      | Nombre completo de la fuente a utilizar.          |
| fontPclName               | String            | true     | false    |                      | Nombre de fuente específico para PCL.              |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos PCL.       |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.       |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.        |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.     |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.  |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.     |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.           |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.             |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de PDFSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                           |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | ----------------------------------------------------- |
| DisplayDocTitle           | Boolean           | true     | false    |                      | Utiliza el título del documento como título del PDF. |
| ExportDocumentStructure   | Boolean           | true     | false    |                      | Conserva la estructura lógica del documento.         |
| EmfRenderSetting          | String            | true     | false    |                      | Configuración para el renderizado de imágenes EMF.    |
| CustomPropertiesExport    | String            | true     | false    |                      | Controla la exportación de propiedades personalizadas del documento. |
| OptimizationType          | String            | true     | false    |                      | Tipo de optimización de PDF (por ejemplo, Tamaño, Velocidad). |
| Producer                  | String            | true     | false    |                      | Nombre de la aplicación generadora del PDF.         |
| PDFCompression            | String            | true     | false    |                      | Algoritmo de compresión para flujos PDF.            |
| FontEncoding              | String            | true     | false    |                      | Codificación utilizada para fuentes incrustadas.     |
| Watermark                 | Clase             | true     | false    |                      | Configuración de marca de agua aplicada al PDF.      |
| CalculateFormula          | Boolean           | true     | false    |                      | Calcula fórmulas antes de la exportación.           |
| CheckFontCompatibility    | Boolean           | true     | false    |                      | Valida la compatibilidad de fuentes para renderizado PDF. |
| Compliance                | String            | true     | false    |                      | Nivel de cumplimiento PDF/A o PDF/X.                 |
| DefaultFont               | String            | true     | false    |                      | Fuente utilizada cuando una fuente de origen no está disponible. |
| OnePagePerSheet           | Boolean           | true     | false    |                      | Coloca cada hoja en una página PDF independiente.    |
| PrintingPageType          | String            | true     | false    |                      | Especifica el tipo de página para impresión.         |
| SecurityOptions           | Clase             | true     | false    |                      | Configuración de seguridad, como contraseñas y permisos. |
| desiredPPI                | Integer           | true     | false    |                      | Resolución deseada en píxeles por pulgada (PPI).     |
| jpegQuality               | Integer           | true     | false    |                      | Calidad de imagen JPEG (0‑100).                      |
| ImageType                 | String            | true     | false    |                      | Tipo de imagen utilizado para la rasterización.      |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos PDF.         |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.         |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.          |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.       |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.    |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.       |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.             |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.              |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de PptxSaveOptions

| Nombre de la propiedad            | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                             |
| --------------------------------- | ----------------- | -------- | -------- | -------------------- | ------------------------------------------------------- |
| IgnoreHiddenRows                  | Boolean           | true     | false    |                      | Omite filas ocultas durante la exportación.            |
| AdjustFontSizeForRowType          | String            | true     | false    |                      | Controla el ajuste del tamaño de fuente según el tipo de fila. |
| ExportViewType                    | String            | true     | false    |                      | Determina qué vista (diapositiva, notas) exportar.     |
| DefaultFont                       | String            | true     | false    |                      | Fuente utilizada cuando una fuente de origen no está disponible. |
| CheckWorkbookDefaultFont          | Boolean           | true     | false    |                      | Comprueba si se aplica la fuente predeterminada del libro. |
| CheckFontCompatibility            | Boolean           | true     | false    |                      | Valida la compatibilidad de fuentes para el formato de destino. |
| IsFontSubstitutionCharGranularity | Boolean           | true     | false    |                      | Controla la sustitución de fuentes a nivel de carácter. |
| OnePagePerSheet                   | Boolean           | true     | false    |                      | Coloca cada hoja en una diapositiva independiente.     |
| AllColumnsInOnePagePerSheet       | Boolean           | true     | false    |                      | Ajusta todas las columnas de una hoja en una sola diapositiva. |
| IgnoreError                       | Boolean           | true     | false    |                      | Ignora errores no críticos durante la conversión.      |
| OutputBlankPageWhenNothingToPrint | Boolean           | true     | false    |                      | Genera una diapositiva en blanco si no hay nada que representar. |
| PageIndex                         | Integer           | true     | false    |                      | Índice de la primera diapositiva a exportar.           |
| PageCount                         | Integer           | true     | false    |                      | Número de diapositivas a exportar.                     |
| PrintingPageType                  | String            | true     | false    |                      | Especifica el tipo de página para impresión.           |
| GridlineType                      | String            | true     | false    |                      | Determina cómo se renderizan las líneas de cuadrícula. |
| TextCrossType                     | String            | true     | false    |                      | Define el tipo de cruce para el renderizado de texto.  |
| DefaultEditLanguage               | String            | true     | false    |                      | Idioma predeterminado para la edición de texto.        |
| EmfRenderSetting                  | String            | true     | false    |                      | Configuración para el renderizado de EMF.              |
| MergeAreas                        | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.               |
| SortExternalNames                 | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.                |
| UpdateSmartArt                    | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| SaveFormat                        | String            | true     | false    |                      | Identificador del formato para archivos PPTX.          |
| CachedFileFolder                  | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.   |
| ClearData                         | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.           |
| CreateDirectory                   | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.            |
| EnableHttpCompression             | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.         |
| RefreshChartCache                 | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                         | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.      |
| ValidateMergedAreas               | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.         |
| CheckExcelRestriction             | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| EncryptDocumentProperties         | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de SqlScriptSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                               |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------------- |
| CheckIfTableExists        | Boolean           | true     | false    |                      | Comprueba si la tabla de destino ya existe.              |
| ColumnTypeMap             | String            | true     | false    |                      | Mapeo de nombres de columna a tipos de datos SQL.        |
| CheckAllDataForColumnType | Boolean           | true     | false    |                      | Escanea todas las filas para inferir tipos de columna.   |
| AddBlankLineBetweenRows   | Boolean           | true     | false    |                      | Inserta una línea en blanco entre filas generadas.       |
| Separator                 | String            | true     | false    |                      | Cadena utilizada para separar columnas (por ejemplo, coma, tabulador). |
| OperatorType              | String            | true     | false    |                      | Operador SQL utilizado (INSERT, UPDATE, etc.).           |
| PrimaryKey                | Integer           | true     | false    |                      | Índice de columna que actúa como clave principal.        |
| CreateTable               | Boolean           | true     | false    |                      | Genera una sentencia CREATE TABLE.                       |
| IdName                    | String            | true     | false    |                      | Nombre de la columna identificadora.                     |
| StartId                   | Integer           | true     | false    |                      | Valor inicial para IDs autoincrementales.                |
| TableName                 | String            | true     | false    |                      | Nombre de la tabla de base de datos de destino.         |
| ExportAsString            | Boolean           | true     | false    |                      | Exporta todos los valores como cadenas.                  |
| ExportArea                | Clase             | true     | false    |                      | Define el área de la hoja a exportar.                    |
| HasHeaderRow              | Boolean           | true     | false    |                      | Indica si la primera fila contiene encabezados de columna. |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos de script SQL.   |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.     |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.             |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.              |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.           |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.        |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.           |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.                 |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.                  |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de SvgSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                         |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------- |
| SheetIndex                | Integer           | true     | false    |                      | Índice de la hoja a exportar.                       |
| ChartImageType            | String            | true     | false    |                      | Formato de imagen utilizado para renderizar gráficos. |
| EmbeddedImageNameInSvg    | String            | true     | false    |                      | Nombre asignado a las imágenes incrustadas en la salida SVG. |
| HorizontalResolution      | Integer           | true     | false    |                      | DPI horizontal del SVG exportado.                  |
| ImageFormat               | String            | true     | false    |                      | Formato de imagen de destino para elementos rasterizados. |
| IsCellAutoFit             | Boolean           | true     | false    |                      | Ajusta automáticamente el contenido de celda al tamaño del SVG. |
| OnePagePerSheet           | Boolean           | true     | false    |                      | Renderiza cada hoja en una página SVG independiente. |
| OnlyArea                  | Boolean           | true     | false    |                      | Exporta solo el área definida de la hoja.          |
| PrintingPage              | String            | true     | false    |                      | Diseño de página utilizado para impresión.          |
| PrintWithStatusDialog     | Boolean           | true     | false    |                      | Muestra un diálogo de estado durante la impresión.  |
| Quality                   | Integer           | true     | false    |                      | Calidad de compresión para imágenes rasterizadas.   |
| TiffCompression           | String            | true     | false    |                      | Tipo de compresión para imágenes TIFF incrustadas en SVG. |
| VerticalResolution        | Integer           | true     | false    |                      | DPI vertical del SVG exportado.                     |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos SVG.        |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.        |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.         |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.      |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.   |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.      |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.            |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.             |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de TxtSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                                               |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | ------------------------------------------------------------------------- |
| QuoteType                 | String            | true     | false    |                      | Tipo de comillas utilizadas (por ejemplo, dobles, simples).              |
| Separator                 | String            | true     | false    |                      | Carácter separador de columnas (por ejemplo, coma, tabulador).           |
| SeparatorString           | String            | true     | false    |                      | Cadena completa utilizada como separador cuando se necesitan más de un carácter. |
| AlwaysQuoted              | Boolean           | true     | false    |                      | Fuerza que todos los campos estén entrecomillados.                       |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos TXT.                             |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.                     |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.                             |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.                              |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.                           |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar.           |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.                        |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.                           |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.                                 |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.                                  |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión.              |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente.                |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida.             |

## Propiedades de XlsSaveOptions y XlsbSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                         |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------- |
| MatchColor                | Boolean           | true     | false    |                      | Preserva los colores exactos de celda durante la exportación. |
| WpsCompatibility          | Boolean           | true     | false    |                      | Habilita la compatibilidad con WPS Office.         |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos XLS/XLSB.   |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché. |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.       |
| CreateDirectory           | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.        |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.     |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.  |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.     |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.           |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.             |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de XmlSaveOptions

| Nombre de la propiedad    | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                               |
| ------------------------- | ----------------- | -------- | -------- | -------------------- | --------------------------------------------------------- |
| SheetIndexes              | Array             | true     | false    |                      | Lista de índices de hojas a incluir en la exportación.    |
| ExportArea                | Clase             | true     | false    |                      | Define el área de la hoja a exportar.                     |
| HasHeaderRow              | Boolean           | true     | false    |                      | Indica si la primera fila contiene encabezados de columna. |
| XmlMapName                | String            | true     | false    |                      | Nombre del mapa XML aplicado a la hoja.                   |
| SheetNameAsElementName    | Boolean           | true     | false    |                      | Utiliza el nombre de la hoja como nombre del elemento XML. |
| DataAsAttribute           | Boolean           | true     | false    |                      | Exporta datos de celda como atributos XML en lugar de elementos. |
| SaveFormat                | String            | true     | false    |                      | Identificador del formato para archivos XML.              |
| CachedFileFolder          | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.      |
| ClearData                 | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.              |
| CreateDirectory           | String            | true     | false    |                      | Crea el directorio de destino si no existe.               |
| EnableHttpCompression     | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.            |
| RefreshChartCache         | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                 | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.         |
| ValidateMergedAreas       | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.            |
| MergeAreas                | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.                  |
| SortExternalNames         | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.                   |
| CheckExcelRestriction     | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| UpdateSmartArt            | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| EncryptDocumentProperties | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |

## Propiedades de XpsSaveOptions

| Nombre de la propiedad            | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                            |
| --------------------------------- | ----------------- | -------- | -------- | -------------------- | ------------------------------------------------------ |
| DefaultFont                       | String            | true     | false    |                      | Fuente utilizada cuando una fuente de origen no está disponible. |
| CheckWorkbookDefaultFont          | Boolean           | true     | false    |                      | Comprueba si se aplica la fuente predeterminada del libro. |
| CheckFontCompatibility            | Boolean           | true     | false    |                      | Valida la compatibilidad de fuentes para el formato de destino. |
| IsFontSubstitutionCharGranularity | Boolean           | true     | false    |                      | Controla la sustitución de fuentes a nivel de carácter. |
| OnePagePerSheet                   | Boolean           | true     | false    |                      | Coloca cada hoja en una página XPS independiente.     |
| AllColumnsInOnePagePerSheet       | Boolean           | true     | false    |                      | Ajusta todas las columnas de una hoja en una sola página. |
| IgnoreError                       | Boolean           | true     | false    |                      | Ignora errores no críticos durante la conversión.     |
| OutputBlankPageWhenNothingToPrint | Boolean           | true     | false    |                      | Genera una página en blanco si no hay nada que representar. |
| PageIndex                         | Integer           | true     | false    |                      | Índice de la primera página a exportar.               |
| PageCount                         | Integer           | true     | false    |                      | Número de páginas a exportar.                         |
| PrintingPageType                  | String            | true     | false    |                      | Especifica el tipo de página para impresión.          |
| GridlineType                      | String            | true     | false    |                      | Determina cómo se renderizan las líneas de cuadrícula. |
| TextCrossType                     | String            | true     | false    |                      | Define el tipo de cruce para el renderizado de texto. |
| DefaultEditLanguage               | String            | true     | false    |                      | Idioma predeterminado para la edición de texto.       |
| EmfRenderSetting                  | String            | true     | false    |                      | Configuración para el renderizado de EMF.             |
| MergeAreas                        | Boolean           | true     | false    |                      | Fusiona celdas adyacentes si es posible.              |
| SortExternalNames                 | Boolean           | true     | false    |                      | Ordena referencias con nombre externas.               |
| UpdateSmartArt                    | Boolean           | true     | false    |                      | Actualiza los objetos SmartArt a la versión más reciente. |
| SaveFormat                        | String            | true     | false    |                      | Identificador del formato para archivos XPS.          |
| CachedFileFolder                  | String            | true     | false    |                      | Carpeta utilizada para archivos temporales en caché.  |
| ClearData                         | Boolean           | true     | false    |                      | Borra los datos existentes antes de guardar.          |
| CreateDirectory                   | Boolean           | true     | false    |                      | Crea el directorio de destino si no existe.           |
| EnableHttpCompression             | Boolean           | true     | false    |                      | Habilita la compresión HTTP para la respuesta.        |
| RefreshChartCache                 | Boolean           | true     | false    |                      | Actualiza los datos en caché de los gráficos antes de guardar. |
| SortNames                         | Boolean           | true     | false    |                      | Ordena alfabéticamente los intervalos con nombre.     |
| ValidateMergedAreas               | Boolean           | true     | false    |                      | Valida la coherencia de las celdas fusionadas.        |
| CheckExcelRestriction             | Boolean           | true     | false    |                      | Aplica límites específicos de Excel durante la conversión. |
| EncryptDocumentProperties         | Boolean           | true     | false    |                      | Cifra las propiedades del documento en el archivo de salida. |
---