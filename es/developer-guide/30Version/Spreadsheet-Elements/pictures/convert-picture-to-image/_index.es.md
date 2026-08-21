---
title: "Aspose.Cells Cloud API – Obtener imagen de hoja de cálculo"
second_title: "Documento"
linktitle: "Obtener"
type: docs
url: /es/pictures/get/
aliases: [  /es/convert-picture-to-image/ ]
keywords: "Aspose.Cells, Obtener imagen, API, Excel, Nube, REST"
description: "Recuperar una imagen específica de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye punto de conexión, parámetros, pasos de autenticación, códigos de respuesta y ejemplos de código."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Obtener imagen de hoja de cálculo"
---

Esta API REST recupera una imagen mediante su índice de base cero desde una hoja de cálculo de Excel.

## API REST

Para llamar a este punto de conexión, debe incluir un token de acceso JWT válido en el encabezado **Authorization**. Los tokens se obtienen mediante el flujo de autenticación de Aspose.Cells Cloud y requieren los alcances adecuados para el acceso a archivos. Para más detalles sobre cómo adquirir un token, consulte la guía general de **Autenticación**.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                                         |
| --------------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------------------- |
| name                  | string  | path      | Nombre del documento de Excel.                                                                                      |
| sheetName             | string  | path      | Nombre de la hoja de cálculo.                                                                                       |
| pictureIndex          | integer | path      | Índice de base cero de la imagen.                                                                                   |
| format                | string  | query     | Formato de exportación deseado (por ejemplo, png, jpg, bmp, gif, tiff). Si se omite, la imagen se devuelve en su formato original. |
| folder                | string  | query     | Carpeta que contiene el documento.                                                                                  |
| storageName           | string  | query     | Nombre del lugar de almacenamiento.                                                                                 |

### Respuestas de error

| Código HTTP | Descripción                                                                   |
| ----------- | ----------------------------------------------------------------------------- |
| 401         | No autorizado – token faltante o no válido.                                   |
| 404         | No encontrado – el archivo, la hoja de cálculo o el índice de salto de página especificados no existen. |
| 400         | Solicitud incorrecta – sintaxis de solicitud mal formada o parámetros no válidos. |
| 500         | Error interno del servidor – se encontró una condición inesperada.            |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# Datos binarios de la imagen (PNG) devueltos en el cuerpo de la respuesta.
# Ejemplo: fragmento codificado en base64
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

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

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}