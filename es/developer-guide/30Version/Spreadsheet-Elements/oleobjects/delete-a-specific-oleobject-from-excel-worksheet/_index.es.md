---
title: "Eliminar un objeto OLE en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Eliminar"
type: docs
url: /oleobjects/delete/
aliases: [/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud, Eliminar, OLE, Objeto, Excel, hoja de cálculo, REST, API, SDK"
description: "Aprenda a eliminar un objeto OLE de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud (v4.0). Incluye el punto de conexión HTTPS, los pasos de autenticación, un ejemplo con cURL, fragmentos de SDK, orientación sobre el manejo de errores y enlaces a pasos siguientes."
weight: 50
ArticleTitle: "Eliminar objeto OLE de una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta página explica cómo eliminar un objeto OLE específico de una hoja de cálculo en un libro de Excel utilizando **Aspose.Cells Cloud**. Un objeto OLE puede ser una imagen vinculada, un gráfico o cualquier objeto incrustado que Excel almacene como una entidad independiente.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                          |
| --------------------- | ------- | --------- | ---------------------------------------------------- |
| name                  | string  | path      | Nombre del libro.                                    |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.                        |
| oleObjectIndex        | integer | path      | Índice del objeto OLE que se va a eliminar.          |
| folder                | string  | query     | Carpeta que contiene el libro. (opcional)            |
| storageName           | string  | query     | Nombre del servicio de almacenamiento. (opcional)    |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar la llamada con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

{{< /tab >}}

{{< /tabs >}}

### Detalles de la respuesta

| Estado HTTP          | Descripción                                                          | JSON de ejemplo                                                    |
| --------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------ |
| **200 OK**            | El objeto OLE se eliminó correctamente.                             | `{ "Code": 200, "Status": "OK" }`                                  |
| **401 Unauthorized**  | Token JWT ausente o no válido.                                       | `{ "Code": 401, "Message": "El token de acceso está ausente o no es válido." }` |
| **404 Not Found**     | El libro, la hoja de cálculo o el índice del objeto OLE especificados no existen. | `{ "Code": 404, "Message": "Índice del objeto OLE fuera de rango." }` |
| **400 Bad Request**   | Faltan parámetros obligatorios o tienen un formato incorrecto.       | `{ "Code": 400, "Message": "Parámetros de la solicitud no válidos." }` |

 maneje estas respuestas en su aplicación verificando el código de estado y mostrando el mensaje adjunto.

## Familia de SDK en la nube
Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}