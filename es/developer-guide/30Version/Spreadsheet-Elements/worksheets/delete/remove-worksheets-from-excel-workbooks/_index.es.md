---
title: "Eliminar hoja de cálculo"
second_title: "Documentos"
linktype: "Una hoja de cálculo"
type: docs
url: /es/worksheets/delete-worksheet/
aliases: [  /es/remove-worksheets-from-excel-workbooks/ ]
keywords: "Aspose.Cells Cloud, Eliminar hoja de cálculo, Excel, Hoja de cálculo, API REST"
description: "Elimine una hoja de cálculo de un libro de Excel utilizando la API REST de Aspose.Cells Cloud. Compatible con SDK para C#, Java, PHP, Ruby, Node.js, Python, Perl, Go y cURL."
weight: 20
ArticleTitle: "Eliminar hoja de cálculo – Aspose.Cells Cloud API"
---

Esta API REST elimina una hoja de cálculo.  
Prerrequisitos: Para llamar a esta API, debe proporcionar un token de autenticación JWT válido en el encabezado **Authorization** y tener acceso a la ubicación de almacenamiento donde se encuentra el libro.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*Nota: La API utiliza la versión **v3.0**, que es la versión estable actual. Los cambios futuros de versión se anunciarán en las notas de lanzamiento.*

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                |
| --------------------- | ------ | --------- | -------------------------- |
| name                  | string | path      | Nombre del documento.      |
| sheetName             | string | path      | Nombre de la hoja de cálculo. |
| folder                | string | query     | Carpeta del documento.     |
| storageName           | string | query     | Nombre del almacenamiento. |

Respuestas HTTP posibles:

| Código de estado | Descripción                                    |
| ---------------- | ---------------------------------------------- |
| 200 OK           | Hoja de cálculo eliminada correctamente.      |
| 400 Bad Request  | Parámetros de solicitud no válidos.           |
| 401 Unauthorized | Fallo en la autenticación o token ausente.    |
| 404 Not Found    | El libro o la hoja de cálculo especificados no existen. |
| 500 Internal Server Error | Error inesperado del servidor.          |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Todas las solicitudes deben realizarse mediante HTTPS; la API no admite conexiones sin TLS.*

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

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}