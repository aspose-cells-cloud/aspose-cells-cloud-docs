---
title: "Actualizar el comentario de una celda en una hoja de cálculo"
type: docs
url: /es/comments/update/
aliases: [  /es/update-a-comment-in-excel-workbook/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, hoja de cálculo, comentario de celda, actualizar comentario de hoja de cálculo, objeto comentario"
description: "Utilice la API REST de Aspose.Cells Cloud para actualizar un comentario en una celda de una hoja de cálculo dentro de un libro de Excel, incluyendo detalles de la solicitud, códigos de respuesta y ejemplos de SDK."
weight: 30
ArticleTitle: "Actualizar el comentario de una celda en una hoja de cálculo – API de Aspose.Cells Cloud"
---

Esta API REST actualiza un comentario en una celda de una hoja de cálculo. Utilice este endpoint para **actualizar un comentario en una hoja de cálculo** en un archivo de Excel.

**Requisitos previos:**  
- Debe incluirse un token de acceso OAuth/JWT válido en el encabezado `Authorization`.  
- El libro debe almacenarse en una ubicación de almacenamiento en la nube compatible (especifique `folder` y opcionalmente `storageName`).

## API PostWorksheetComment

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                           |
| --------------------- | ------ | --------- | --------------------------------------------------------------------- |
| name                  | string | path      | El nombre del documento de Excel.                                    |
| sheetName             | string | path      | El nombre de la hoja de cálculo que contiene la celda.               |
| cellName              | string | path      | La dirección de la celda (por ejemplo, **A1**).                      |
| comment               | object | body      | Un objeto **Comment** que define el comentario que se agregará o actualizará. |
| folder                | string | query     | La carpeta donde se encuentra almacenado el documento.               |
| storageName           | string | query     | El nombre del servicio de almacenamiento.                            |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "este es un comentario",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Códigos de estado de respuesta posibles:

| Código | Descripción                                                   |
|--------|---------------------------------------------------------------|
| 200    | Comentario actualizado correctamente.                        |
| 400    | Solicitud incorrecta: faltan parámetros o son inválidos.     |
| 401    | No autorizado: error de autenticación.                        |
| 404    | No encontrado: el libro, la hoja de cálculo o el comentario no existen. |
| 500    | Error interno del servidor.                                   |

**Notas / Consejos:**  
- La longitud máxima del comentario es de 1024 caracteres.  
- Los caracteres admitidos son UTF‑8; evite los caracteres de control.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar con Aspose.Cells Cloud. Un SDK maneja los detalles de bajo nivel para que usted pueda concentrarse en su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

Operaciones relacionadas:  
- [Obtener comentario de hoja de cálculo](/comments/get/)  
- [Agregar comentario de hoja de cálculo](/comments/add/)  
- [Eliminar comentario de hoja de cálculo](/comments/delete/)