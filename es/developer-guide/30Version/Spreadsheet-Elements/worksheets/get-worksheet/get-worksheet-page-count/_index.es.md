---
title: "Obtener el número de páginas de una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "PageCount"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, API de Excel, número de páginas de hoja de cálculo, REST, SDK en la nube, paginación de Excel"
description: "Recuperar el número de páginas imprimibles en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el formato de solicitud HTTPS, pasos de autenticación, ejemplo de cURL, respuesta JSON completa, códigos de estado y ejemplos de código del SDK."
weight: 10
ArticleTitle: "Obtener el número de páginas de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
---

Esta API REST devuelve el **número de páginas** de una hoja de cálculo.

**Autenticación:** Todos los puntos de conexión de Aspose.Cells Cloud requieren un token Bearer obtenido mediante el flujo OAuth2. Incluya el token en el encabezado `Authorization`, tal como se muestra en el ejemplo de cURL a continuación.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### Parámetros de la solicitud

| Parámetro   | Tipo   | Ubicación | Descripción                                |
| ----------- | ------ | --------- | ------------------------------------------ |
| name        | string | path      | Nombre del documento.                      |
| sheetName   | string | path      | Nombre de la hoja de cálculo.              |
| folder      | string | query     | Carpeta que contiene el documento.         |
| storageName | string | query     | Nombre del almacenamiento.                 |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo invocar la API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Detalles de la respuesta

| Estado HTTP | Significado                                              |
| ----------- | -------------------------------------------------------- |
| **200**     | Correcto – devuelve la carga útil JSON mostrada arriba. |
| **401**     | No autorizado – token faltante o no válido.             |
| **404**     | No encontrado – el archivo o la hoja de cálculo no existe. |
| **500**     | Error interno del servidor – condición inesperada del servidor. |

### Historial de versiones

_Versión de la API **v3.0** (publicada en 2025). Si utiliza una versión más reciente, consulte la documentación actualizada del punto de conexión._

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en la lógica de su negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Notas

- El número de páginas refleja el diseño imprimible, teniendo en cuenta los saltos de página, los márgenes y la escala. Las filas o columnas ocultas pueden afectar el resultado.
- Asegúrese de que la hoja de cálculo de destino exista y de que el archivo esté almacenado en la carpeta y `storageName` especificadas antes de realizar la solicitud.