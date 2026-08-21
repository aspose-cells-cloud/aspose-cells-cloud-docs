---
title: "Agregar una imagen a un archivo de Excel"
second_title: "Documentos"
linktitle: "Agregar"
type: docs
url: /es/pictures/add/
aliases: [  /es/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, agregar imagen, API REST"
description: "Utilice la API REST de Aspose.Cells Cloud para agregar una imagen a una hoja de cálculo de Excel. Los SDK para Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift simplifican la integración entre plataformas."
weight: 20
ArticleTitle: "Agregar una imagen a una hoja de cálculo de Excel – API de Aspose.Cells Cloud"
---

Esta API REST agrega una nueva imagen a una hoja de cálculo de Excel.  
**Requisitos previos:** Debe tener un token de autenticación válido de Aspose Cloud, un libro existente almacenado en un almacenamiento admitido y los permisos adecuados para modificar la hoja de cálculo.

## API PutWorksheetAddPicture

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                                    |
|----------------------|---------|-----------|----------------------------------------------------------------------------------------------------------------|
| name                 | string  | path      | Nombre del libro.                                                                                              |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                                                                                  |
| picture              | object  | body      | Objeto de imagen (datos binarios).                                                                             |
| upperLeftRow         | integer | query     | Índice de base cero de la fila superior izquierda donde se colocará la imagen.                                |
| upperLeftColumn      | integer | query     | Índice de base cero de la columna superior izquierda donde se colocará la imagen.                             |
| lowerRightRow        | integer | query     | Índice de base cero de la fila inferior derecha del área de la imagen.                                        |
| lowerRightColumn     | integer | query     | Índice de base cero de la columna inferior derecha del área de la imagen.                                     |
| picturePath          | string  | query     | Ruta al archivo de imagen; si se omite, los datos de la imagen deben suministrarse en el cuerpo de la solicitud. |
| folder               | string  | query     | Carpeta que contiene el libro.                                                                                 |
| storageName          | string  | query     | Nombre del servicio de almacenamiento.                                                                         |

**Nota sobre el cuerpo de la solicitud:** Cuando se omite `picturePath`, envíe los datos binarios de la imagen en el cuerpo de la solicitud utilizando `multipart/form-data`.

### Códigos de estado HTTP

| Código | Significado                 | Descripción                                               |
|--------|-----------------------------|-----------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                            |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño.            |
| 500    | Error interno del servidor  | Error inesperado del servidor.                            |

**Ejemplo de esquema de respuesta 200**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**Nota:** El tamaño máximo de la imagen es de 10 MB; los archivos más grandes se rechazarán con una respuesta `400 Bad Request`.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) define una interfaz de programación pública accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
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

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Nota:** Los formatos de imagen admitidos incluyen PNG, JPEG, BMP y GIF. El tamaño máximo de la imagen es de 10 MB; los archivos más grandes se rechazarán con una respuesta `400 Bad Request`.