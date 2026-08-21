---
title: "Actualizar una imagen en un archivo de Excel"
second_title: "Documento"
linktitle: "Actualizar"
type: docs
url: /es/pictures/update/
aliases: [  /es/update-a-specific-picture-from-excel-workshee/ ]
keywords: "Aspose.Cells Cloud, Excel, Actualizar imagen, REST API, SDK"
description: "Aprenda cómo actualizar una imagen en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye detalles de la solicitud, un ejemplo con cURL y fragmentos de código SDK para múltiples lenguajes."
ArticleTitle: "Actualizar una imagen en un archivo de Excel mediante la API REST de Aspose.Cells Cloud"
weight: 70
---

Esta API REST actualiza una imagen, identificada por su índice, en una hoja de cálculo de Excel.

**Requisitos previos:** Debe tener un token JWT válido de Aspose Cloud, el archivo de Excel objetivo almacenado en su almacenamiento de Aspose Cloud y utilizar la versión 3.0 o posterior de la API.

## API PostWorksheetPicture

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                  |
| --------------------- | ------- | --------- | ------------------------------------------------------------ |
| name                  | string  | path      | El nombre del documento de Excel.                            |
| sheetName             | string  | path      | El nombre de la hoja de cálculo que contiene la imagen.      |
| pictureIndex          | integer | path      | Índice de base cero de la imagen que se va a actualizar.     |
| picture               | object  | body      | Objeto JSON que describe las propiedades de la imagen a actualizar. |
| folder                | string  | query     | La carpeta donde se almacena el documento.                   |
| storageName           | string  | query     | El nombre del servicio de almacenamiento.                    |

**Nota:** El índice de la imagen es de base cero. Los formatos de imagen admitidos incluyen JPEG, PNG, BMP y GIF. El tamaño máximo de la imagen es de 10 MB.

### Respuestas de error

| Código HTTP | Descripción                                                |
| ----------- | ---------------------------------------------------------- |
| 401         | No autorizado: token ausente o no válido.                  |
| 404         | No encontrado: el archivo, la hoja de cálculo o el índice de imagen especificados no existen. |
| 400         | Solicitud incorrecta: sintaxis de solicitud mal formada o parámetros no válidos. |
| 500         | Error interno del servidor: se encontró una condición inesperada. |

La <a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*Consulte también:* Agregar imagen, Eliminar imagen, Obtener imagen, Borrar imágenes: otras operaciones relacionadas con imágenes en la API de Aspose.Cells Cloud.