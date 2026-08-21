---
title: "Actualizar propiedades de hoja de cálculo – Referencia de la API de Aspose.Cells Cloud (v3.0)"
second_title: "Documento"
linktitle: "Actualizar"
type: docs
url: /worksheets/update-properties/
aliases: [/update-excel-worksheet-properties/]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "hoja de cálculo",
    "actualizar propiedades",
    "REST API",
    "nube",
    "v3.0",
  ]
description: "Aprenda cómo actualizar propiedades básicas (por ejemplo, mostrar ceros, visibilidad de la regla) de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud v3.0. Incluye solicitud cURL, ejemplos de SDK, parámetros y manejo de errores."
ArticleTitle: "Actualizar propiedades de hoja de cálculo – Referencia de la API de Aspose.Cells Cloud (v3.0)"
---

Esta API REST actualiza las propiedades básicas de la hoja de cálculo.

## API REST

**Requisitos previos:** Debe tener una cuenta válida de Aspose Cloud, obtener un token de acceso JWT y asegurarse de que el libro de trabajo objetivo esté almacenado en una ubicación compatible. Todas las solicitudes deben realizarse mediante **HTTPS**.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                         |
| --------------------- | ------ | ------------------------------------ | --------------------------------------------------------------------------------------------------- |
| name                  | string | path                                 | Nombre del archivo del libro de trabajo (incluida la extensión).                                    |
| sheetName             | string | path                                 | Nombre de la hoja de cálculo que se va a actualizar.                                                |
| sheet                 | object | body                                 | Objeto JSON que contiene pares clave/valor de propiedades de la hoja de cálculo (por ejemplo, `DisplayZeros`, `IsRulerVisible`). |
| folder                | string | query                                | Ruta de la carpeta en el almacenamiento donde se encuentra el libro de trabajo.                    |
| storageName           | string | query                                | Nombre del almacenamiento que se va a utilizar.                                                     |

El objeto **sheet** se envía en el cuerpo de la solicitud como JSON. Las propiedades modificables incluyen `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible` y otras definidas en la especificación de la API.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) define una interfaz de programación públicamente accesible y permite llevar a cabo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

Códigos de respuesta típicos:

- **200** – Éxito. Se actualizaron las propiedades de la hoja de cálculo.
- **400** – Solicitud inválida (por ejemplo, JSON malformado o parámetro obligatorio ausente).
- **401** – No autorizado: token JWT ausente o no válido.
- **404** – Libro de trabajo o hoja de cálculo no encontrado.
- **500** – Error interno del servidor.

| Código | Significado |
|--------|-------------|
| 200 | Éxito: se actualizaron las propiedades de la hoja de cálculo. |
| 400 | Solicitud incorrecta: JSON malformado o parámetro obligatorio ausente. |
| 401 | No autorizado: token JWT ausente o no válido. |
| 404 | No encontrado: el libro de trabajo o la hoja de cálculo no existe. |
| 500 | Error interno del servidor. |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}