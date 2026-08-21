---
title: "Eliminar todas las validaciones de la hoja de cálculo – Aspose.Cells Cloud API"
second_title: "Documentación"
linktitle: "Eliminar"
type: docs
url: /validations/clear/
keywords: "Aspose.Cells Cloud, Eliminar validaciones de hoja de cálculo, Excel, API REST, Validación de hojas de cálculo, API"
description: "Elimine todas las reglas de validación de datos de una hoja de cálculo en un archivo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye pasos de autenticación, detalles de la solicitud, ejemplo de cURL, esquema de respuesta, manejo de errores y fragmentos de SDK."
weight: 10
---

**Requisitos previos**

- Una cuenta válida de Aspose Cloud.
- Un token de acceso JWT obtenido mediante la API de autenticación de Aspose Cloud (`/connect/token`).
- El libro de trabajo debe estar almacenado en su almacenamiento de Aspose Cloud (o bien deben proporcionarse los parámetros de consulta `folder` y/o `storageName` correspondientes).

Esta API REST elimina todas las validaciones de hoja de cálculo de una hoja de Excel.

## API REST

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                           |
|----------------------|--------|-----------|-------------------------------------------------------|
| name                 | string | path      | El nombre del documento de Excel.                    |
| sheetName            | string | path      | El nombre de la hoja de cálculo que contiene las validaciones. |
| folder               | string | query     | La carpeta donde se almacena el documento.           |
| storageName          | string | query     | El nombre del servicio de almacenamiento.            |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API con cURL tras obtener un token JWT.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
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

{{< /tab >}}

{{< /tabs >}}

### Manejo de errores

| Estado HTTP | Significado             | Descripción                                               |
|-------------|-------------------------|-----------------------------------------------------------|
| 400         | Solicitud incorrecta    | La solicitud está mal formada o le faltan parámetros obligatorios. |
| 401         | No autorizado           | El token JWT falta, es inválido o ha caducado.            |
| 404         | No encontrado           | El libro de trabajo o la hoja de cálculo especificados no existen. |
| 500         | Error interno del servidor | Se produjo un error inesperado en el lado del servidor. |

La carga útil del error sigue la misma estructura JSON con los campos `Code` y `Message`, por ejemplo:

```json
{
  "Code": 401,
  "Message": "Token inválido o caducado."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel para que usted pueda centrarse en la lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}

---