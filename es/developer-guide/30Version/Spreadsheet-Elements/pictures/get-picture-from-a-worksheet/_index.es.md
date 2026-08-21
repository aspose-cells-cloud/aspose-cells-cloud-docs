---
title: "Obtener todas las imágenes en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Obtener todas"
type: docs
url: /pictures/get-all/
aliases: [/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, hoja de cálculo de Excel, API de imágenes, obtener todas las imágenes, API REST, SDK"
description: "Recuperar todos los objetos de imagen de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud."
ArticleTitle: "Obtener todas las imágenes en una hoja de cálculo de Excel - API de Aspose.Cells Cloud"
weight: 10
---

Esta API REST recupera toda la información de imagen de una hoja de cálculo de Excel.

**Requisitos previos**  
Antes de llamar a este punto final, asegúrese de tener:

- Un token de acceso JWT válido de Aspose Cloud.  
- El archivo de Excel de destino cargado en el almacenamiento seleccionado.  
- El nombre correcto del almacenamiento (si utiliza un almacenamiento personalizado).  
- El nombre de la hoja de cálculo que contiene las imágenes.

## API GetWorksheetPictures

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Nota:** Utilice HTTPS (TLS 1.2 o superior) al llamar a la API e incluya un token JWT válido en el encabezado `Authorization`.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                         |
| ------------------- | ------ | --------- | --------------------------------------------------- |
| name                | string | path      | El nombre del archivo de Excel.                     |
| sheetName           | string | path      | El nombre de la hoja de cálculo que contiene imágenes. |
| folder              | string | query     | La ruta de la carpeta donde se almacena el archivo. |
| storageName         | string | query     | El nombre del servicio de almacenamiento.           |

### Respuestas de error

| Código HTTP | Descripción                                                                 |
| ----------- | --------------------------------------------------------------------------- |
| 401         | No autorizado – token faltante o no válido.                                |
| 404         | No encontrado – el archivo, la hoja de cálculo o el índice de salto de página especificados no existen. |
| 400         | Solicitud incorrecta – sintaxis de solicitud mal formada o parámetros no válidos. |
| 500         | Error interno del servidor – se encontró una condición inesperada.         |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Respuesta correcta**: Una llamada correcta devuelve HTTP 200 con una carga útil JSON que contiene un objeto `Pictures` que enumera el enlace de recursos de cada imagen.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

Puede descargar los SDK directamente desde sus respectivos gestores de paquetes (por ejemplo, NuGet para .NET, Maven Central para Java, Composer para PHP, npm para Node.js, PyPI para Python, CPAN para Perl y módulos de Go para Go).

*Consulte también:* Agregar una imagen, Eliminar una imagen, Actualizar las propiedades de una imagen.