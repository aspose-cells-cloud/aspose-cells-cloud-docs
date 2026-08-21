---
title: "Agregar varias filas a una hoja de cálculo de Excel"
ArticleTitle: "Agregar varias filas a una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
second_title: "Documentos"
linktitle: "Filas"
type: docs
url: /es/rows/add/rows/
keywords: "Aspose.Cells Cloud, insertar filas, hoja de cálculo de Excel, API REST, SDK, agregar varias filas"
description: "Aprenda a utilizar la API REST de Aspose.Cells Cloud para insertar varias filas en una hoja de cálculo de Excel. Esta guía cubre el punto de conexión, los parámetros de solicitud, ejemplos de comandos cURL y ejemplos de uso del SDK."
weight: 20
---

Esta API REST agrega varias filas nuevas a una hoja de cálculo de Excel.

## API PutInsertWorksheetRows

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                           |
|----------------------|---------|-----------|-----------------------------------------------------------------------|
| name                 | string  | path      | El nombre del libro de cálculo.                                       |
| sheetName            | string  | path      | El nombre de la hoja de cálculo.                                      |
| startrow             | integer | query     | El índice de la primera fila que se va a insertar (**basado en 0**). |
| totalRows            | integer | query     | El número de filas a insertar.                                        |
| updateReference      | boolean | query     | Si se deben actualizar las referencias de celdas tras la inserción (`true` o `false`). |
| folder               | string  | query     | La carpeta que contiene el documento.                                 |
| storageName          | string  | query     | El nombre del almacenamiento.                                         |

**Requisitos previos**  
El libro de cálculo ya debe existir en el almacenamiento (o carpeta) especificado antes de invocar esta operación.

**Autenticación**  
La API requiere un token JWT válido. Inclúyalo en el encabezado `Authorization`, tal como se muestra en el ejemplo de cURL a continuación.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota:** Esta operación `PUT` no requiere un cuerpo de solicitud; se puede enviar un objeto JSON vacío (`{}`) si la biblioteca cliente obliga a incluir un payload.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Códigos de respuesta posibles*  

- **200 OK** – Filas insertadas correctamente.  
- **400 Bad Request** – Parámetros inválidos (por ejemplo, índice de fila negativo).  
- **401 Unauthorized** – Token JWT ausente o inválido.  
- **404 Not Found** – El libro de cálculo o la hoja de cálculo especificados no existen.  
- **500 Internal Server Error** – Error inesperado del servidor.

{{< /tab >}}

{{< /tabs >}}

Para realizar otras operaciones con filas, consulte las páginas relacionadas: **Eliminar filas**, **Obtener filas** y **Copiar filas**.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}