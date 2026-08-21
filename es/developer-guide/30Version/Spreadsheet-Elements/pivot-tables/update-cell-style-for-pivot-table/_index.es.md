---
title: "Actualizar el estilo de celda para una tabla dinámica"
second_title: "Document"
linktype: Format
type: docs
url: /pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, estilo de tabla dinámica, API de actualización de estilo de celda, API REST, API de Excel, formateo de hojas de cálculo, SDK en la nube, estilo de celda, tabla dinámica"
description: "Aprenda cómo actualizar el estilo de una celda específica en una tabla dinámica de Aspose.Cells Cloud mediante la API REST. Incluye el punto de conexión, parámetros, autenticación, ejemplo con cURL y fragmento de código del SDK de Go, así como orientación optimizada para SEO."
weight: 90
ArticleTitle: "Actualizar el estilo de celda para una tabla dinámica - Documentación de la API de Aspose.Cells Cloud"
---

Esta API REST actualiza el **estilo** de una celda en una tabla dinámica.

**Requisitos previos / Autenticación**  
Para llamar a este punto de conexión debe disponer de un token de acceso JWT válido de Aspose Cloud. Obtenga el token mediante el flujo OAuth 2.0 descrito en la [Guía de autenticación](/authentication/). Incluya el token en el encabezado de la solicitud:

```http
Authorization: Bearer <jwt token>
```

El token JWT es obligatorio para todas las llamadas a las API de Aspose.Cells Cloud.

## API PostPivotTableCellStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                             |
|----------------------|---------|-----------|---------------------------------------------------------------------------------------------------------|
| name                 | string  | path      | Nombre del documento (obligatorio).                                                                    |
| sheetName            | string  | path      | Nombre de la hoja de cálculo (obligatorio).                                                            |
| pivotTableIndex      | integer | path      | Índice de la tabla dinámica (obligatorio).                                                             |
| column               | integer | query     | Índice de columna de la celda a formatear (basado en cero; obligatorio).                               |
| row                  | integer | query     | Índice de fila de la celda a formatear (basado en cero; obligatorio).                                  |
| style                | object  | body      | DTO de estilo (objeto de transferencia de datos) que define el nuevo estilo de celda.                 |
| needReCalculate      | boolean | query     | Indica si la tabla dinámica debe recalcularse tras aplicar el formato. El valor predeterminado es **false**. |
| folder               | string  | query     | Carpeta donde se almacena el documento (opcional).                                                     |
| storageName          | string  | query     | Nombre del almacenamiento (opcional).                                                                  |
| Method               | string  | N/A       | Método HTTP utilizado para la solicitud (**POST**).                                                     |

La <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
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

{{< /tab >}}

{{< /tabs >}}

**Respuesta**  
En caso de éxito, el servicio devuelve el código HTTP 200 con un cuerpo vacío, lo que indica que el estilo se ha aplicado correctamente. En caso de error, se devuelve una carga útil en formato JSON con un código y un mensaje de error.

| Estado HTTP | Descripción                                                             |
|-------------|-------------------------------------------------------------------------|
| 200         | Estilo aplicado correctamente.                                         |
| 400         | Solicitud incorrecta — por ejemplo, índice de columna/fila no válido.  |
| 401         | No autorizado — token JWT faltante o no válido.                        |
| 404         | No encontrado — el documento, la hoja de cálculo o la tabla dinámica especificados no existen. |
| 500         | Error interno del servidor — condición inesperada.                     |

El cuerpo de la respuesta está vacío en caso de éxito.

Para obtener más información, consulte la documentación de la API **Get Pivot Table**.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstrae los detalles de bajo nivel, lo que le permite centrarse en su lógica de negocio. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

El siguiente ejemplo de código demuestra cómo llamar a los servicios web de Aspose.Cells utilizando el SDK de **Go**:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Actualizar el estilo de celda para una tabla dinámica",
  "description": "Guía para actualizar el estilo de una celda específica en una tabla dinámica de Aspose.Cells Cloud mediante la API REST.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, tabla dinámica, estilo de celda, API REST, SDK de Go",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>