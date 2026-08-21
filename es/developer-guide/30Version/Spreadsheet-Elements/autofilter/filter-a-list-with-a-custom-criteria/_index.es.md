---
title: "Agregar un criterio personalizado en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Agregar filtro personalizado"
type: docs
url: /es/autofilter/add-custom-filter/
aliases: [  /es/filter-a-list-with-a-custom-criteria/ , /es/autofilter/add-a-custom-filter/ ]
keywords: "Excel, filtro personalizado, Aspose.Cells Cloud, API REST, filtro automático, hoja de cálculo, criterio personalizado"
description: "Aprenda a usar la API REST de Aspose.Cells Cloud para agregar un filtro personalizado en una hoja de cálculo de Excel. Incluye detalles de la solicitud, un ejemplo con cURL y fragmentos de código SDK para múltiples lenguajes de programación."
weight: 65
ArticleTitle: "Agregar un criterio personalizado en una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

Esta API REST filtra una lista utilizando un **criterio personalizado**.

## API PutWorksheetCustomFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud:

| Nombre del parámetro | Tipo    | Ubicación                   | Descripción                                                                 |
|----------------------|---------|-----------------------------|-----------------------------------------------------------------------------|
| name                 | string  | path                        | Nombre del archivo de Excel.                                               |
| sheetName            | string  | path                        | Nombre de la hoja de cálculo que contiene los datos que se van a filtrar. |
| range                | string  | query                       | Rango de celdas al que se aplicará el filtro (por ejemplo, `A1:B1`).       |
| fieldIndex           | integer | query                       | Índice de columna basado en cero sobre el que se aplica el filtro.         |
| operatorType1        | string  | query                       | Primer operador de comparación (por ejemplo, `LessOrEqual`, `Equal`).      |
| criteria1            | string  | query                       | Primer valor o expresión de filtro.                                        |
| isAnd                | boolean | query                       | Si es `true`, combina ambos criterios con **Y**; de lo contrario, con **O**. |
| operatorType2        | string  | query                       | Segundo operador de comparación (opcional).                               |
| criteria2            | string  | query                       | Segundo valor o expresión de filtro (opcional).                            |
| matchBlanks          | boolean | query                       | Cuando es `true`, se incluyen las celdas vacías en los resultados del filtro. |
| refresh              | boolean | query                       | Si es `true`, fuerza la actualización de la hoja de cálculo tras aplicar el filtro. |
| folder               | string  | query                       | Ruta de carpeta en el almacenamiento donde se encuentra el archivo.       |
| storageName          | string  | query                       | Nombre del servicio de almacenamiento.                                    |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                               |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.               |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                            |

## Cómo utilizar la API PutWorksheetCustomFilter con SDKs

### Especificación de la API PutWorksheetCustomFilter

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
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

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en la lógica de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Para otras operaciones de AutoFilter, como agregar un filtro estándar o un filtro de fecha, consulte las páginas de documentación relacionadas dentro de la sección AutoFilter.