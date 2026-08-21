---
title: "Eliminar un gráfico de una hoja de cálculo"
type: docs
url: /charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Eliminar gráfico"
  - "Hoja de cálculo"
  - "Excel"
  - "Cloud SDK"
  - "Eliminación de gráficos"
  - "Referencia de API"
description: "Elimina un gráfico de una hoja de cálculo mediante su índice basado en cero utilizando la API REST de Aspose.Cells Cloud."
ArticleTitle: "Eliminar un gráfico de una hoja de cálculo mediante la API REST de Aspose.Cells Cloud"
---

Esta API REST elimina un gráfico de hoja de cálculo por su índice.

Para operaciones relacionadas, consulte las páginas **[Agregar un gráfico](#)** y **[Obtener gráfico](#)**.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                       |
| -------------------- | ------- | --------- | ------------------------------------------------- |
| name                 | string  | path      | Nombre del libro de trabajo.                     |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                    |
| chartIndex           | integer | path      | Índice basado en cero del gráfico que se va a eliminar. |
| folder               | string  | query     | Carpeta que contiene el libro de trabajo.        |
| storageName          | string  | query     | Nombre del almacenamiento que se utilizará.     |


### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                                |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.                |
| 500    | Error interno del servidor  | Error inesperado del servidor.                                |

## Cómo utilizar la API PutWorksheetAddChart con SDK

### Especificación de la API PutWorksheetAddChart

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
-X DELETE \
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

{{< /tab >}}

{{< /tabs >}}

La API devuelve los siguientes códigos de estado:

| Código | Descripción                                |
|--------|--------------------------------------------|
| 200    | Gráfico eliminado correctamente            |
| 400    | Solicitud incorrecta (por ejemplo, índice no válido) |
| 401    | No autorizado (token JWT ausente o no válido) |
| 404    | Libro de trabajo, hoja de cálculo o gráfico no encontrado |
| 500    | Error del servidor                         |

** Manejo de errores:** Para obtener información detallada sobre los errores, consulte el modelo genérico de errores en la especificación OpenAPI.

### Utilizar SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracte los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}