---
title: "Copiar columnas en una hoja de cálculo de Excel"
second_title: "Documentos"
linktype: "Copiar"
type: docs
url: /es/columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, copiar columnas, API de Excel, REST, SDK en la nube, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Aprenda a copiar una o más columnas en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye la sintaxis de la solicitud, los parámetros requeridos, detalles de autenticación, manejo de errores y ejemplos de SDK en C#, Java, Python, Ruby, Node.js, Go, Perl y más."
articleTitle: "Copiar columnas en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
weight: 30
---

Esta API REST permite **copiar columnas** en una hoja de cálculo de Excel. La operación **Copiar columnas** le permite duplicar una sola columna o un rango de columnas e insertar la copia en una ubicación específica dentro de la misma hoja de cálculo. Utilice este punto final para copiar columnas de forma eficiente al trabajar con hojas de cálculo grandes, y consulte operaciones relacionadas como [Agregar columna](/es/columns/add/) y [Ocultar columna](/es/columns/hide/) para realizar tareas adicionales de gestión de columnas.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Parámetros de la solicitud

| Nombre del parámetro         | Tipo    | Ubicación | Descripción                                                                               |
| ---------------------------- | ------- | --------- | ----------------------------------------------------------------------------------------- |
| **name**                     | string  | path      | Nombre del libro.                                                                         |
| **sheetName**                | string  | path      | Nombre de la hoja de cálculo.                                                             |
| **sourceColumnIndex**        | integer | query     | Índice de base cero de la columna que se va a copiar.                                     |
| **destinationColumnIndex**   | integer | query     | Índice de base cero donde se insertarán la(s) columna(s) copiada(s).                      |
| **columnNumber**             | integer | query     | Número de columnas consecutivas que se van a copiar.                                      |
| **worksheet**                | string  | query     | _(Opcional)_ Identificador de la hoja de cálculo utilizado cuando el nombre difiere del de la ruta. |
| **folder**                   | string  | query     | Ruta a la carpeta que contiene el libro en el almacenamiento de Aspose Cloud.            |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) define el contrato completo de esta operación.

### Ejemplo con cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### Respuesta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Manejo de errores

La API devuelve códigos de estado HTTP estándar con una carga útil en formato JSON que describe el error.

| Código de estado | Significado                                           | Cuerpo JSON de ejemplo                                            |
| ---------------- | ----------------------------------------------------- | ----------------------------------------------------------------- |
| **400**          | Solicitud incorrecta: parámetros inválidos           | `{ "Code": 400, "Message": "Índice de columna no válido." }`     |
| **401**          | No autorizado: token ausente o inválido               | `{ "Code": 401, "Message": "El token de acceso no es válido o ha expirado." }` |
| **404**          | No encontrado: el libro o la hoja de cálculo no existen | `{ "Code": 404, "Message": "Libro no encontrado." }`             |
| **500**          | Error interno del servidor: condición inesperada      | `{ "Code": 500, "Message": "Se produjo un error inesperado." }`  |

> **Cómo solucionar problemas:** Verifique que el token de acceso esté vigente, que los nombres del libro y la hoja de cálculo sean correctos, y que `sourceColumnIndex`, `destinationColumnIndex` y `columnNumber` estén dentro del rango de columnas de la hoja de cálculo.

## Familia de SDK en la nube

Utilizar un SDK es la forma más eficaz de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "¿Cómo me autentico al llamar a la API de Copiar columnas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Obtenga un token de acceso OAuth2 de Aspose Cloud mediante su ID de cliente y su secreto, e inclúyalo en el encabezado de la solicitud como `Authorization: Bearer <access_token>`."
      }
    },
    {
      "@type": "Question",
      "name": "¿Cuál es la diferencia entre `sourceColumnIndex` y `destinationColumnIndex`?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` es el índice de base cero de la columna que desea copiar. `destinationColumnIndex` es el índice de base cero donde se insertarán la(s) columna(s) copiada(s)."
      }
    },
    {
      "@type": "Question",
      "name": "¿Qué respuesta recibo si la operación de copia falla?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "La API devuelve un código de estado distinto de 200 (por ejemplo, 400 para una solicitud incorrecta, 401 para no autorizado). El cuerpo de la respuesta contiene un objeto JSON con los campos `Code` y `Message` que describen el error."
      }
    }
  ]
}
</script>
---