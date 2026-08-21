---
title: "Actualizar una validación de hoja de cálculo en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Actualizar"
type: docs
url: /validations/update/
keywords: "Aspose.Cells Cloud, actualización de validación de Excel, API REST, validación de hoja de cálculo, API de Excel"
description: "Cómo actualizar una validación de hoja de cálculo en un archivo de Excel utilizando la API REST de Aspose.Cells Cloud, con ejemplos de cURL y fragmentos de código SDK para múltiples lenguajes de programación."
weight: 10
ArticleTitle: "Actualizar la validación de hoja de cálculo mediante la API de Aspose.Cells Cloud"
---

Esta API REST actualiza una validación de hoja de cálculo por su índice en una hoja de cálculo de Excel.

Antes de llamar a este punto de conexión, obtenga un token de acceso JWT con los alcances adecuados (por ejemplo, `Cells.ReadWrite`). Incluya el token en el encabezado `Authorization` como se muestra en los ejemplos.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                    |
| --------------------- | ------- | --------- | -------------------------------------------------------------- |
| name                  | string  | path      | El nombre del archivo del libro.                               |
| sheetName             | string  | path      | El nombre de la hoja de cálculo que contiene la validación.   |
| validationIndex       | integer | path      | El índice de base cero de la validación que se va a actualizar. |
| validation            | object  | body      | Un objeto JSON que define la configuración actualizada de la validación. |
| folder                | string  | query     | La carpeta en el almacenamiento en la nube donde se encuentra el libro. |
| storageName           | string  | query     | El nombre del servicio de almacenamiento (si se utiliza un almacenamiento personalizado). |

La <a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**Códigos de estado HTTP posibles**

| Código | Significado                              | Descripción |
|--------|------------------------------------------|-------------|
| 200    | OK                                       | La validación se actualizó correctamente. |
| 400    | Solicitud incorrecta                     | La solicitud tiene un formato incorrecto o faltan parámetros obligatorios. |
| 401    | No autorizado                            | El token JWT es inválido o falta. |
| 403    | Prohibido                                | El token no tiene los alcances suficientes. |
| 404    | No encontrado                            | El libro, la hoja de cálculo o el índice de validación especificados no existen. |
| 500    | Error interno del servidor               | Se produjo un error inesperado en el servidor. |

Para obtener más información sobre el manejo de errores, consulte la <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">documentación de errores de Aspose.Cells Cloud</a>.

También puede querer explorar operaciones relacionadas, como agregar una nueva validación o eliminar una existente:

- [Agregar una validación de hoja de cálculo](https://docs.aspose.cloud/cells/validations/add/)
- [Eliminar una validación de hoja de cálculo](https://docs.aspose.cloud/cells/validations/delete/)

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}