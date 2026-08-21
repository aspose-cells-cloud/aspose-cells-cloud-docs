---
title: "Eliminar salto de página horizontal"
ArticleTitle: "Aspose.Cells Cloud – Eliminar salto de página horizontal (API REST)"
second_title: "Documento"
linktype: "Eliminar salto de página horizontal"
type: docs
url: /es/page-breaks/delete-horizontal-page-break/
aliases: [  /es/delete-horizontal-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, Eliminar salto de página horizontal, Hoja de cálculo de Excel, API REST, SDK"
description: "Elimine un salto de página horizontal de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. SDK disponibles para C#, Java, PHP, Ruby, Node.js, Python, Perl y Go."
weight: 50
---

Esta API REST elimina un salto de página **horizontal**.

**Prerrequisitos**: Para llamar a este punto final, debe poseer un token de acceso JWT válido de Aspose Cloud. Obténgalo siguiendo la [guía de autenticación](https://docs.aspose.cloud/cells/authentication/).

## API DeleteHorizontalPageBreak

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*Todas las llamadas a la API deben realizarse mediante **HTTPS**.*

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                       |
| --------------------- | ------- | --------- | ----------------------------------------------------------------- |
| `name`               | string  | path      | Nombre del archivo de Excel (libro de trabajo).                  |
| `sheetName`          | string  | path      | Nombre de la hoja de cálculo que contiene el salto de página.    |
| `index`              | integer | path      | Índice de base cero del salto de página horizontal que se va a eliminar. |
| `folder`             | string  | query     | Ruta de carpeta opcional en el almacenamiento donde se encuentra el archivo. |
| `storageName`        | string  | query     | Nombre opcional del servicio de almacenamiento.                  |

### Respuestas de error

| Código HTTP | Descripción                                                                  |
| ----------- | ---------------------------------------------------------------------------- |
| 401         | No autorizado: token ausente o no válido.                                    |
| 404         | No encontrado: el archivo, hoja de cálculo o índice del salto de página especificados no existen. |
| 400         | Solicitud incorrecta: sintaxis de solicitud mal formada o parámetros no válidos. |
| 500         | Error interno del servidor: se encontró una condición inesperada.            |

**Consulte también:**  
- [Agregar salto de página horizontal](/page-breaks/add-horizontal-page-break/)  
- [Obtener saltos de página horizontales](/page-breaks/get-horizontal-page-breaks/)  
- [Eliminar salto de página vertical](/page-breaks/delete-vertical-page-break/)

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) define una interfaz de programación pública accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar la llamada con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Esquema de respuesta**

| Campo   | Tipo    | Descripción                                         |
|---------|---------|-----------------------------------------------------|
| Code    | integer | Código de estado HTTP (por ejemplo, 200).          |
| Status  | string  | Mensaje de estado textual (por ejemplo, "OK").     |
| Message | string  | Información adicional opcional para casos de error. |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d).*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f).*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152).*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca).*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0).*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1).*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca).*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*Si el ejemplo no se carga correctamente, revíselo en [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

{{< /tab >}}

{{< /tabs >}}