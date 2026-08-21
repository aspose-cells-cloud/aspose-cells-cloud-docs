---
title: "Agregar un filtro de icono a una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Agregar filtro de icono"
type: docs
url: /es/autofilter/add-icon-filter/
aliases: [  /es/add-an-icon-filter/ , /es/autofilter/add-an-icon-filter/ ]
keywords: "Aspose.Cells Cloud, Excel, Filtro de icono, Filtro automático, API REST"
description: "Aprenda cómo agregar un filtro de icono a una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud, incluyendo detalles de la solicitud, ejemplo con cURL, fragmentos de código con SDK y manejo de errores."
weight: 65
ArticleTitle: "Agregar un filtro de icono a una hoja de cálculo de Excel – Documentación de Aspose.Cells Cloud"
---

## API REST

Esta API REST agrega un **filtro de icono** a una hoja de cálculo de Excel utilizando la **API REST de Aspose.Cells Cloud**.

**Antecedentes:** Un filtro de icono aplica un conjunto visual de iconos a las celdas según sus valores, lo que permite un análisis rápido y visual de las tendencias de los datos. Los casos de uso comunes incluyen resaltar métricas de rendimiento, indicadores de estado o categorizar valores con iconos de semáforo directamente dentro de las hojas de cálculo de Excel.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de solicitud:

| Nombre del parámetro | Tipo    | Ubicación | Descripción |
|----------------------|---------|-----------|-------------|
| name                 | string  | Ruta      | Nombre del libro. |
| sheetName            | string  | Ruta      | Nombre de la hoja de cálculo. |
| range                | string  | Consulta  | Rango de celdas (por ejemplo, `A1:B1`) al que se aplicará el filtro. |
| fieldIndex           | integer | Consulta  | Índice de columna (base cero) que el filtro afecta. |
| iconSetType          | string  | Consulta  | Conjunto de iconos a utilizar. Valores permitidos: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId               | integer | Consulta  | Identificador del icono específico dentro del conjunto de iconos seleccionado. |
| matchBlanks          | boolean | Consulta  | Determina si las celdas en blanco se incluyen (`true` o `false`). |
| refresh              | boolean | Consulta  | Indica si el filtro debe actualizarse tras aplicarse (`true` o `false`). |
| folder               | string  | Consulta  | Carpeta que contiene el libro original. |
| storageName          | string  | Consulta  | Nombre del almacenamiento donde reside el libro. |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado               | Descripción                                            |
|--------|---------------------------|--------------------------------------------------------|
| 200    | OK                        | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta      | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado             | Token JWT inválido o ausente. |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor | Error inesperado del servidor. |
## Cómo usar la API PutWorksheetIconFilter con SDK

### Especificación de la API PutWorksheetIconFilter

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Códigos de estado de respuesta posibles:

| Código | Descripción |
|--------|-------------|
| 200    | Filtro aplicado correctamente. |
| 400    | Solicitud incorrecta: parámetros faltantes o no válidos. |
| 401    | No autorizado: token de autenticación inválido o ausente. |
| 404    | Libro, hoja de cálculo o rango especificado no encontrado. |
| 500    | Error interno del servidor. |
{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Para otras capacidades del filtro automático, consulte la documentación sobre **[Agregar filtro de color](/autofilter/add-color-filter/)**, **[Agregar filtro de fecha](/autofilter/add-date-filter/)** y **[Borrar filtro automático](/autofilter/clear-autofilter/)**.