---
title: "Eliminar fondo en un libro de Excel"
second_title: "Documento"
linktitle: "Eliminar"
type: docs
url: /delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells eliminar fondo, API de Excel eliminar fondo, Aspose.Cells Cloud, DELETE /cells background"
description: "Elimine una imagen de fondo de un libro de Excel usando la API de Aspose.Cells Cloud. Aprenda sobre el punto final DELETE, los parámetros requeridos, el ejemplo de cURL y el código del SDK en C#, Java, Python y más."
weight: 170
ArticleTitle: "Eliminar imagen de fondo de un libro de Excel usando la API de Aspose.Cells Cloud"
---

Esta API REST elimina la imagen de fondo de un libro de Excel.

## API DeleteWorkbookBackground

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de consulta**

| Nombre del parámetro | Tipo   | Descripción                                      | Obligatorio |
| -------------------- | ------ | ------------------------------------------------ | ----------- |
| folder               | string | Carpeta que contiene el libro original.          | No          |
| storageName          | string | Nombre del servicio de almacenamiento a utilizar.| No          |

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**Códigos de estado HTTP**

| Código | Significado                | Descripción                                                     |
|--------|----------------------------|-----------------------------------------------------------------|
| 200    | OK                         | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta       | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado              | Token JWT inválido o faltante.                                  |
| 413    | Payload demasiado grande    | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## Cómo usar la API DeleteWorkbookBackground con SDK

### Especificación de la API DeleteWorkbookBackground

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación pública accesible que permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra una solicitud DELETE completa con el encabezado de autenticación requerido; no se requiere cuerpo de solicitud.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}