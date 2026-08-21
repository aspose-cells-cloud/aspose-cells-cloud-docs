---
title: "Eliminar columna de una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
description: "Aprenda cómo eliminar una o varias columnas de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye autenticación, sintaxis de solicitud, parámetros, respuestas, manejo de errores y ejemplos de SDK."
keywords: ["Aspose.Cells", "Eliminar columna", "API de Excel", "REST", "Nube", "Hoja de cálculo", "Columnas"]
date: 2026-07-30
api_version: "v3.0"
---

# Eliminar columna de una hoja de cálculo de Excel

**Punto de conexión**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

Esta operación elimina una única columna o un rango de columnas de una hoja de cálculo. Las referencias a celdas (incluidas las fórmulas) pueden actualizarse automáticamente tras la eliminación.

---

## Tabla de contenidos
1. [Requisitos previos](#requisitos-previos)  
2. [Autenticación](#autenticación)  
3. [URL de solicitud y método HTTP](#url-de-solicitud-y-método-http)  
4. [Parámetros](#parámetros)  
   - [Parámetros de ruta](#parámetros-de-ruta)  
   - [Parámetros de consulta](#parámetros-de-consulta)  
5. [Ejemplo con cURL](#ejemplo-con-curl)  
6. [Respuestas](#respuestas)  
7. [Códigos de error](#códigos-de-error)  
8. [Ejemplos de SDK](#ejemplos-de-sdk)  
9. [Notas adicionales](#notas-adicionales)  

---

## Requisitos previos
- Un **token de acceso JWT** válido obtenido mediante el flujo de autenticación de Aspose Cloud.  
- El libro de cálculo (`{name}`) debe haberse cargado previamente en el almacenamiento de Aspose Cloud (o estar accesible mediante los parámetros de consulta `folder`/`storageName`).  

---

## Autenticación
Todas las solicitudes a Aspose.Cells Cloud requieren autenticación mediante token **Bearer**.

```http
Authorization: Bearer <access_token>
```

Consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) para obtener detalles sobre cómo adquirir un token JWT.

---

## URL de solicitud y método HTTP
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – nombre del archivo del libro de cálculo (por ejemplo, `test.xlsx`).  
- **`{sheetName}`** – nombre de la hoja de cálculo (por ejemplo, `Sheet1`).  
- **`{columnIndex}`** – índice de base cero de la primera columna que se va a eliminar.

---

## Parámetros

| Nombre            | Ubicación | Tipo    | Obligatorio | Descripción |
|-------------------|-----------|---------|-------------|-------------|
| **name**          | path      | string  | ✅ Sí       | Nombre del archivo del libro de cálculo. |
| **sheetName**     | path      | string  | ✅ Sí       | Nombre de la hoja de cálculo. |
| **columnIndex**   | path      | integer | ✅ Sí       | Índice de base cero de la primera columna que se va a eliminar. |
| **startColumn**   | query     | integer | ❌ No       | Índice de base cero donde comienza la eliminación. Si se omite, se utiliza `columnIndex` como valor predeterminado. |
| **totalColumns**  | query     | integer | ❌ No       | Número de columnas que se eliminarán. Si se omite, solo se elimina la columna identificada por `columnIndex`. |
| **updateReference** | query   | boolean | ❌ No       | Cuando es `true`, actualiza las referencias a celdas (incluidas las fórmulas) en todo el libro tras la eliminación. |
| **folder**        | query     | string  | ❌ No       | Ruta de la carpeta que contiene el libro de cálculo. |
| **storageName**   | query     | string  | ❌ No       | Nombre del servicio de almacenamiento de Aspose Cloud. |

> **Nota**: El parámetro `columns` mostrado en la especificación de bajo nivel de la API ha sido reemplazado por los parámetros más expresivos `startColumn` y `totalColumns`. Ambos enfoques se aceptan para mantener la compatibilidad con versiones anteriores.

---

## Ejemplo con cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### Explicación
- Elimina la columna **B** (`columnIndex = 1`) de `Sheet1` en `test.xlsx`.  
- `startColumn=1` y `totalColumns=1` especifican la eliminación de una única columna.  
- `updateReference=true` asegura que las fórmulas y otras referencias se ajusten automáticamente.

---

## Respuestas

| Código HTTP | Descripción | Ejemplo |
|-------------|-------------|---------|
| **200** | Éxito: se eliminaron la(s) columna(s). | `{ "Code": 200, "Status": "OK" }` |
| **400** | Solicitud incorrecta: faltan o son inválidos los parámetros. | `{ "Code": 400, "Message": "Valor no válido para totalColumns." }` |
| **401** | No autorizado: falta o es inválido el token JWT. | `{ "Code": 401, "Message": "Fallo en la autenticación." }` |
| **404** | No encontrado: el libro de cálculo o la hoja de cálculo no existen. | `{ "Code": 404, "Message": "Hoja de cálculo 'Sheet1' no encontrada." }` |
| **500** | Error interno del servidor: condición inesperada en el servidor. | `{ "Code": 500, "Message": "Ocurrió un error inesperado." }` |

El cuerpo de la respuesta sigue el modelo genérico **`CellsCloudResponse`**.

---

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Faltan o son inválidos los parámetros (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Carga demasiado grande       | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |
---

## Ejemplos de SDK

A continuación se presentan fragmentos listos para ejecutar para los SDK más populares. Reemplace los valores de marcador de posición (`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>`, etc.) con sus propios datos.

| Idioma | Ejemplo |
|--------|---------|
| **C#** | <details><summary>Mostrar código</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>Mostrar código</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>Mostrar código</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>Mostrar código</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>Mostrar código</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Error:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>Mostrar código</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>Mostrar código</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>Mostrar código</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*Todos los SDK agregan automáticamente la cabecera `Authorization` requerida cuando se configura el `access_token`.*

---

## Notas adicionales

### Cabeceras de seguridad (recomendadas para producción)
Al servir la página de documentación, incluya las siguientes cabeceras de respuesta HTTP para mejorar la seguridad:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### Consejos de rendimiento
- Cargue los scripts de análisis de terceros (`gtag.js`, `containerize.js`) con el atributo `async` o pospóngalos hasta después de que la página se haya renderizado.  
- Minifique cualquier paquete personalizado de JavaScript/CSS.  
- Precargue iconos SVG pequeños si bloquean el renderizado:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### Mejoras de SEO (JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Eliminar columna de una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud",
  "description": "Aprenda cómo eliminar una o varias columnas de una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Eliminar columna", "Excel", "API REST"]
}
```

Coloque este fragmento dentro de un bloque `<script type="application/ld+json">` en la cabecera HTML.

### Accesibilidad
- Todas las imágenes decorativas usan `alt=""` o están ocultas con `aria-hidden="true"`.  
- La imagen de Open Graph ahora incluye un atributo `alt` en la etiqueta meta para completitud.  

---

## Véase también
- [Especificación OpenAPI para DeleteWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [Resumen de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [SDK de Aspose.Cells Cloud en GitHub](https://github.com/aspose-cells-cloud)  

---
---