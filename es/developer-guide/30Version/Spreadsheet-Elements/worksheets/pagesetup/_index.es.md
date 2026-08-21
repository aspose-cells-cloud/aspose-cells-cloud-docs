---
title: "Configuración de página de hoja de cálculo"
second_title: "Document"
linktitle: "Configuración de página"
type: docs
url: /es/page-setup/
keywords: "Aspose.Cells, pageSetup, worksheet, configuración de impresión, márgenes, orientación, tamaño de papel, encabezado, pie de página, escalado"
description: "Aprenda a configurar el diseño de impresión de una hoja de cálculo de Excel con el objeto PageSetup de Aspose.Cells Cloud. Incluye lista de propiedades, valores predeterminados, intervalos y ejemplos de código para C#, Java y Python."
weight: 20
ArticleTitle: "Configuración de página de hoja de cálculo – Configure el diseño de impresión con Aspose.Cells Cloud"
---

# **PageSetup**

Configuración de página de impresión de Excel

## Información general

El objeto **PageSetup** define las opciones de diseño de impresión para una hoja de cálculo de Excel, como los márgenes, orientación, escalado, encabezados, pies de página y otras configuraciones relacionadas con la impresión. Configurar estas propiedades permite a los desarrolladores generar libros imprimibles que coincidan con la apariencia y paginación deseadas.

A continuación se muestra un breve ejemplo en C# que demuestra cómo establecer propiedades comunes de configuración de página mediante el SDK de Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Inicializar el cliente de la API (reemplace con sus credenciales)
var apiInstance = new CellsApi("SU_ID_DE_CLIENTE", "SU_CLAVE_SECRETA_DE_CLIENTE");

// Definir las configuraciones de PageSetup
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// Aplicar las configuraciones a la primera hoja del libro
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

Este fragmento configura la hoja de cálculo en orientación apaisada, utiliza papel tamaño A4, centra el contenido horizontal y verticalmente, y aplica un factor de escalado del 100 %.

## Propiedades

| Nombre de la propiedad   | Tipo de propiedad | Nullable | ReadOnly | Valor predeterminado | Descripción                                                                   |
| ------------------------ | ----------------- | -------- | -------- | ------------------- | ----------------------------------------------------------------------------- |
| BlackAndWhite            | bool              | false    | false    | false               | Imprime la hoja de cálculo en modo blanco y negro.                           |
| BottomMargin             | float             | true     | false    | 2.54 cm             | Tamaño del margen inferior en centímetros.                                   |
| CenterHorizontally       | bool              | false    | false    | false               | Centra la hoja horizontalmente al imprimirla.                                |
| CenterVertically         | bool              | false    | false    | false               | Centra la hoja verticalmente al imprimirla.                                  |
| FirstPageNumber          | int               | true     | false    | 1                   | Número de página inicial cuando se imprime la hoja.                          |
| FitToPagesTall           | int               | false    | false    | 1                   | Número de páginas de altura a las que se escalará la hoja de cálculo.        |
| FitToPagesWide           | int               | false    | false    | 1                   | Número de páginas de anchura a las que se escalará la hoja de cálculo.       |
| FooterMargin             | float             | true     | false    | 2.54 cm             | Distancia desde la parte inferior de la página hasta el pie de página, en cm.|
| HeaderMargin             | float             | true     | false    | 2.54 cm             | Distancia desde la parte superior de la página hasta el encabezado, en cm.   |
| IsAutoFirstPageNumber    | bool              | false    | false    | false               | Asigna automáticamente el número de la primera página.                      |
| IsHFAlignMargins         | bool              | false    | false    | true                | Si es true, los márgenes del encabezado/pie de página se alinean con los márgenes de página. |
| IsHFDiffFirst            | bool              | false    | false    | false               | Indica que el encabezado/pie de página en la primera página es distinto del resto. |
| IsHFDiffOddEven          | bool              | false    | false    | false               | Indica que el encabezado/pie de página en las páginas impares es distinto del de las pares. |
| IsHFScaleWithDoc         | bool              | false    | false    | false               | Escala el encabezado y el pie de página junto con el documento (Excel 2007+).|
| IsPercentScale           | bool              | false    | false    | true                | Cuando es false, `FitToPagesWide` y `FitToPagesTall` controlan el escalado.  |
| LeftMargin               | float             | true     | false    | 2.54 cm             | Tamaño del margen izquierdo en centímetros.                                  |
| Order                    | string            | true     | false    | "DownThenOver"      | Orden que Excel utiliza para numerar páginas al imprimir una hoja grande.   |
| Orientation              | string            | false    | false    | "Portrait"          | Orientación de página: **Landscape** (apaisado) o **Portrait** (retrato).    |
| PaperSize                | string            | true     | false    | "A4"                | Tamaño de papel utilizado para la impresión.                                 |
| PrintArea                | string            | true     | false    | (ninguno)           | Rango de celdas que se imprimirán (por ejemplo, `"A1:D20"`).                 |
| PrintComments            | string            | true     | false    | "NoComments"        | Cómo se imprimen los comentarios junto con la hoja.                          |
| PrintCopies              | int               | true     | false    | 1                   | Número de copias a imprimir.                                                 |
| PrintDraft               | bool              | false    | false    | false               | Imprime la hoja de cálculo en modo borrador (sin gráficos).                  |
| PrintErrors              | string            | true     | false    | "Display"           | Tipo de error de impresión mostrado.                                         |
| PrintGridlines           | bool              | false    | false    | false               | Imprime las líneas de cuadrícula de celda.                                   |
| PrintHeadings            | bool              | false    | false    | false               | Imprime los encabezados de filas y columnas.                                 |
| PrintQuality             | int               | true     | false    | 600                 | Configuración de calidad de impresión (puntos por pulgada).                  |
| PrintTitleColumns        | string            | true     | false    | (ninguno)           | Columnas que se repetirán en el lado izquierdo de cada página impresa.       |
| PrintTitleRows           | string            | true     | false    | (ninguno)           | Filas que se repetirán en la parte superior de cada página impresa.          |
| RightMargin              | float             | true     | false    | 2.54 cm             | Tamaño del margen derecho en centímetros.                                    |
| TopMargin                | float             | true     | false    | 2.54 cm             | Tamaño del margen superior en centímetros.                                   |
| Zoom                     | int               | false    | false    | 100                 | Factor de escalado en porcentaje (10–400 %).                                 |
| Header                   | object            | true     | false    | (ninguno)           | Configuración del encabezado de página.                                      |
| Footer                   | object            | true     | false    | (ninguno)           | Configuración del pie de página.                                             |

## Objetos relacionados

- **Header** – Configura el encabezado de la hoja de cálculo.  
- **Footer** – Configura el pie de página de la hoja de cálculo.  
- **PrintOptions** – Configuraciones adicionales relacionadas con la impresión, como saltos de página y área de impresión.  
---