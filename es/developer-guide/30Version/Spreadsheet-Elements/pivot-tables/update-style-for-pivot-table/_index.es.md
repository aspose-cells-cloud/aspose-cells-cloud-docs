---
title: "Actualizar estilo para tabla dinámica"
second_title: "Documento"
linktitle: "Dar formato a todo"
type: docs
url: /es/pivot-tables/format-all/
aliases: [  /es/update-style-for-pivot-table/ ]
keywords: "tabla dinámica, actualizar estilo, Aspose.Cells Cloud, API REST, Excel, hoja de cálculo, API, estilo de tabla dinámica, dar formato a todo"
description: "Aprenda cómo actualizar el estilo de una tabla dinámica completa mediante la API REST de Aspose.Cells Cloud. Incluye detalles de la solicitud, un ejemplo con cURL y fragmentos de código SDK para múltiples lenguajes de programación."
weight: 100
ArticleTitle: "Actualizar estilo para tabla dinámica - Aspose.Cells Cloud API"
---

Esta API REST actualiza el estilo de una tabla dinámica.

## API PostPivotTableStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**Requisitos previos / Autenticación**  
Debe proporcionarse un token de acceso JWT válido en el encabezado `Authorization` (por ejemplo, `Bearer <token JWT>`). Asegúrese de que el token tenga permisos para acceder al libro y la hoja de cálculo especificados.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                     |
|----------------------|---------|-----------|-------------------------------------------------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro.                                                                  |
| sheetName            | string  | path      | Hoja de cálculo que contiene la tabla dinámica.                                                |
| pivotTableIndex      | integer | path      | Índice de base cero de la tabla dinámica que se va a formatear.                                |
| style                | object  | body      | Un DTO de estilo que define el formato que se aplicará.                                        |
| needReCalculate      | boolean | query     | Establezca en **true** para recalcular la tabla dinámica después del formato; el valor predeterminado es **false**. |
| folder               | string  | query     | Carpeta donde se almacena el libro.                                                            |
| storageName          | string  | query     | Nombre del servicio de almacenamiento.                                                         |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                               |
|--------|-----------------------------|-----------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                            |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño.           |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                          |

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar contra la API. El SDK abstracte los detalles de bajo nivel para que pueda centrarse en su lógica de negocio. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

El siguiente ejemplo de código muestra cómo llamar a la API mediante el SDK de Go:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}