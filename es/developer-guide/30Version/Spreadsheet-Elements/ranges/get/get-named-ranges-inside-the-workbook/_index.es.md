---
title: "Obtener rangos con nombre en un libro de Excel"
second_title: "Documento"
linktitle: "Nombre"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "rangos con nombre, Excel, Aspose.Cells, API en la nube, hojas de cálculo"
description: "Recuperar rangos con nombre de un libro de Excel mediante la API REST de Aspose.Cells Cloud. Incluye detalles de la solicitud, comandos cURL de ejemplo y ejemplos de SDK para múltiples lenguajes de programación."
ArticleTitle: "Obtener rangos con nombre en un libro de Excel – Aspose.Cells Cloud API"
weight: 10
---

Esta API REST devuelve información sobre los rangos con nombre definidos dentro de las hojas de cálculo.

**Antecedentes** – Un *rango con nombre* es un identificador definido por el usuario que hace referencia a una celda específica o a un bloque de celdas en una hoja de cálculo. Los rangos con nombre simplifican la creación de fórmulas, mejoran la legibilidad y permiten el acceso programático a áreas frecuentemente utilizadas de un libro.

**Requisitos previos** – El acceso a la API de Aspose.Cells Cloud requiere un token de acceso JWT válido. Obtenga el token autenticándose con su ID de cliente y secreto de cliente de Aspose Cloud a través del punto final del token OAuth 2.0. Incluya el token en el encabezado `Authorization: Bearer <jwt token>` de cada solicitud.

## API GetNamedRanges

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación     | Descripción                                          |
| -------------------- | ------ | ------------- | ---------------------------------------------------- |
| name                 | string | Ruta          | El nombre del documento de Excel.                   |
| folder               | string | Cadena de consulta | La carpeta que contiene el documento.             |
| storageName          | string | Cadena de consulta | El nombre del almacenamiento donde reside el documento. |

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                          |
| ------ | -------------------------- | ---------------------------------------------------- |
| 200    | Correcto                   | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT no válido o faltante.                      |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño.      |
| 500    | Error interno del servidor | Error inesperado en el servidor.                     |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) define una interfaz de programación accesible públicamente que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para invocar los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo recuperar rangos con nombre mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Modelo de respuesta**

| Campo           | Tipo    | Descripción                                              |
|-----------------|---------|----------------------------------------------------------|
| `ColumnCount`   | integer | Número de columnas en el rango.                          |
| `ColumnWidth`   | number  | Ancho de cada columna (en puntos).                       |
| `FirstColumn`   | integer | Índice basado en cero de la primera columna del rango.   |
| `FirstRow`      | integer | Índice basado en cero de la primera fila del rango.      |
| `Name`          | string  | Nombre definido por el usuario para el rango.            |
| `RefersTo`      | string  | Fórmula que define la referencia a la celda (por ejemplo, `=Sheet1!$B$10:$H$10`). |
| `RowCount`      | integer | Número de filas en el rango.                             |
| `RowHeight`     | number  | Altura de cada fila (en puntos).                         |
| `Worksheet`     | string  | Nombre de la hoja de cálculo que contiene el rango.      |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar esta funcionalidad. Los SDK manejan los detalles de bajo nivel para que usted se enfoque en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}