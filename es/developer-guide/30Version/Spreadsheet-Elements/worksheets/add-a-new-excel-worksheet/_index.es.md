---
title: "Agregar una hoja de cálculo de Excel"
ArticleTitle: "Agregar una hoja de cálculo de Excel - Guía de la API en la nube de Aspose.Cells"
second_title: "Documento"
linktype: "docs"
url: /es/worksheets/add/
aliases: [  /es/add-a-new-excel-worksheet/ ]
keywords: "agregar hoja de cálculo de Excel, Aspose.Cells Cloud, API REST, PUT worksheet, libro de Excel, solicitud de API"
description: "Guía paso a paso para agregar una nueva hoja de cálculo a un libro de Excel mediante la API REST de Aspose.Cells Cloud, incluyendo detalles de la solicitud, un ejemplo con cURL y fragmentos de código de SDK para múltiples lenguajes."
weight: 20
---

Esta API REST agrega una nueva hoja de cálculo a un libro existente.

**Requisitos previos**: Para llamar a este punto final, debe tener un token de autenticación válido de Aspose Cloud, el libro de trabajo objetivo debe haberse cargado en el almacenamiento de Aspose Cloud y debe conocer el nombre del almacenamiento (si utiliza un almacenamiento personalizado).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                           |
|----------------------|---------|-----------|-------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro de trabajo.            |
| sheetName            | string  | path      | Nombre de la nueva hoja de cálculo que se va a crear. |
| position             | integer | query     | Posición de índice base cero donde se inserta la hoja. |
| sheettype            | string  | query     | Tipo de la nueva hoja (por ejemplo, **Chart**, **Dialog**). |
| folder               | string  | query     | Carpeta que contiene el libro de trabajo.            |
| storageName          | string  | query     | Nombre del almacenamiento de Aspose Cloud.           |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**Códigos de estado de respuesta posibles**

| Código de estado | Descripción                                          |
|------------------|------------------------------------------------------|
| 200              | Hoja de cálculo agregada correctamente.             |
| 400              | Solicitud incorrecta: parámetros inválidos.         |
| 401              | No autorizado: token de autenticación faltante o inválido. |
| 404              | No encontrado: el libro de trabajo o la carpeta no existen. |
| 500              | Error interno del servidor: condición inesperada.   |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}