---
title: "Eliminar una imagen de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Eliminar"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, API en la nube, eliminar imagen, hoja de cálculo de Excel, REST"
description: "Elimine una imagen de una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Aprenda sobre el punto final DELETE, los parámetros requeridos, la autenticación, los códigos de error y el código de ejemplo."
weight: 50
ArticleTitle: "Eliminar una imagen de una hoja de cálculo de Excel – Aspose.Cells Cloud API"
---

Esta API REST elimina una imagen de una hoja de cálculo de Excel.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Obligatorio | Descripción                                                  |
| -------------------- | ------- | --------- | ----------- | ------------------------------------------------------------ |
| name                 | string  | path      | Sí          | El nombre del archivo del libro.                             |
| sheetName            | string  | path      | Sí          | El nombre de la hoja de cálculo que contiene la imagen.     |
| pictureIndex         | integer | path      | Sí          | El índice de base cero de la imagen que se va a eliminar.   |
| folder               | string  | query     | No          | La carpeta donde se almacena el libro.                       |
| storageName          | string  | query     | No          | El nombre del servicio de almacenamiento (opcional).        |

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar la llamada con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**Cabeceras de ejemplo de respuesta**

| Cabecera       | Valor                         |
|----------------|-------------------------------|
| Content-Type   | application/json              |
| Content-Length | (varía)                       |
| Date           | (fecha del servidor)          |

{{< /tab >}}

{{< /tabs >}}

### Manejo de errores

| Código HTTP | Significado                                                       | Cuerpo de ejemplo de error                                             |
| ----------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------- |
| 200         | Imagen eliminada correctamente.                                   | `{ "Code": 200, "Status": "OK" }`                                       |
| 400         | Solicitud incorrecta: parámetros no válidos.                      | `{ "Code": 400, "Message": "Índice de imagen no válido." }`             |
| 401         | No autorizado: token faltante o no válido.                        | `{ "Code": 401, "Message": "Falta o no es válido el token de acceso." }` |
| 404         | No encontrado: el libro, la hoja de cálculo o la imagen no existen. | `{ "Code": 404, "Message": "Recurso no encontrado." }`                 |
| 500         | Error interno del servidor.                                       | `{ "Code": 500, "Message": "Error inesperado del servidor." }`         |

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK gestiona los detalles de bajo nivel, para que pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}