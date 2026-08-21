---
title: "Agregar una columna vacía a una hoja de cálculo de Excel - API de Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Agregar"
type: docs
url: /es/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "agregar, columna, Excel, API, Aspose.Cells, Cloud, REST, insertar"
description: "Aprenda cómo insertar una nueva columna en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye la sintaxis de la solicitud, un ejemplo con cURL y ejemplos de código con SDK."
weight: 20
ArticleTitle: "Agregar una columna vacía a una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
---

Esta API REST inserta una o más columnas en una hoja de cálculo.

**Prerrequisitos**  
Antes de llamar a este punto final, asegúrese de haber completado los siguientes pasos:

- Obtenga un token de acceso válido de OAuth 2.0 e inclúyalo en el encabezado `Authorization`.  
- Almacene el libro de trabajo objetivo en el almacenamiento seleccionado (predeterminado = "Default") o especifique los parámetros adecuados `folder` y `storageName`.  
- Verifique que el nombre de la hoja de cálculo proporcionado en `sheetName` exista en el libro de trabajo.

## API PutInsertWorksheetColumns

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                           |
|----------------------|---------|-----------|-----------------------------------------------------------------------|
| **name**             | string  | path      | Nombre del archivo del libro de trabajo.                             |
| **sheetName**        | string  | path      | Nombre de la hoja de cálculo.                                        |
| **columnIndex**      | integer | path      | Índice de base cero de la columna donde comienza la inserción.       |
| **totalColumns**     | integer | query     | Número de columnas a insertar.                                       |
| **updateReference**  | boolean | query     | Si es **true**, se actualizan las referencias de celdas para reflejar la inserción. |
| **folder**           | string  | query     | Ruta a la carpeta que contiene el libro de trabajo.                  |
| **storageName**      | string  | query     | Nombre del servicio de almacenamiento.                               |

**Notas**

- El valor de `columnIndex` debe estar entre 0 y el número actual de columnas en la hoja de cálculo. Insertar más allá del rango existente expandirá automáticamente la hoja.  
- Insertar varias columnas (`totalColumns` > 1) desplaza las columnas existentes hacia la derecha.  
- El indicador `updateReference` tiene como valor predeterminado `false`; configúrelo como `true` para actualizar fórmulas y rangos con nombre.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para llamar a los servicios web de Aspose.Cells. El siguiente ejemplo muestra una solicitud completa, incluida la autenticación y el parámetro de ruta correcto.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**Códigos de respuesta**

| Código | Descripción                                          |
|--------|------------------------------------------------------|
| 200    | Columna(s) insertada(s) correctamente.              |
| 400    | Solicitud incorrecta: parámetros faltantes o no válidos. |
| 401    | No autorizado: token inválido o faltante.           |
| 404    | Libro de trabajo o hoja de cálculo no encontrado.   |
| 500    | Error interno del servidor.                         |

**Ejemplos de respuestas de error**

```json
// 400 Bad Request – parámetros faltantes o no válidos
{
  "Code": 400,
  "Message": "Parámetro no válido: totalColumns debe ser un entero positivo."
}

// 401 Unauthorized – token inválido o faltante
{
  "Code": 401,
  "Message": "La autenticación falló. El token de acceso falta o no es válido."
}

// 404 Not Found – el libro de trabajo o la hoja de cálculo no existe
{
  "Code": 404,
  "Message": "Libro de trabajo 'test.xlsx' no encontrado."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "Se produjo un error inesperado en el servidor."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel para que pueda centrarse en la lógica de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}