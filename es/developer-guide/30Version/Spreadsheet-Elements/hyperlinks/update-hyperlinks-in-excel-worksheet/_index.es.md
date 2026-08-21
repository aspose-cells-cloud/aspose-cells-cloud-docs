---
title: "Actualizar un hipervínculo en una hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
description: "Aprenda cómo actualizar un hipervínculo en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, esquema del cuerpo de solicitud, ejemplo de cURL, fragmentos de código del SDK, manejo de errores, limitación de tasa y requisitos previos."
keywords:
  - "Aspose.Cells"
  - "actualización de hipervínculo"
  - "API de Excel"
  - "API REST"
  - "hoja de cálculo en la nube"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Actualizar un hipervínculo en una hoja de cálculo de Excel  

**Versión de la API:** v3.0  

La operación **PostWorksheetHyperlink** actualiza un hipervínculo existente en una hoja de cálculo identificada por su índice basado en cero.

---

## Tabla de contenido
1. [Requisitos previos](#requisitos-previos)  
2. [Limitación de tasa](#limitación-de-tasa)  
3. [Punto de conexión](#punto-de-conexión)  
4. [Parámetros](#parámetros)  
   - [Parámetros de ruta](#parámetros-de-ruta)  
   - [Parámetros de consulta](#parámetros-de-consulta)  
   - [Esquema del cuerpo de solicitud](#esquema-del-cuerpo-de-solicitud)  
5. [Respuestas](#respuestas)  
   - [Respuesta correcta](#respuesta-correcta)  
   - [Respuestas de error](#respuestas-de-error)  
6. [Ejemplo con cURL](#ejemplo-con-curl)  
7. [Fragmentos de código del SDK](#fragmentos-de-código-del-sdk)  
8. [Consulte también](#consulte-también)  

---

## Requisitos previos <a name="requisitos-previos"></a>

| Requisito | Descripción |
|-----------|-------------|
| **Autenticación** | Autenticación basada en token JWT. Obtenga un token según se describe en la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Almacenamiento** | El libro debe estar almacenado en un almacenamiento compatible con Aspose Cloud (el valor predeterminado es **Default**). |
| **Permisos** | El token JWT debe tener permisos para leer y escribir en el libro de destino. |
| **Encabezados** | Se requieren `Content-Type: application/json` y `Accept: application/json` en todas las solicitudes. |

---

## Limitación de tasa <a name="limitación-de-tasa"></a>

Aspose.Cells Cloud impone un **límite máximo de 60 solicitudes por minuto por token de acceso**. Exceder este límite devuelve el código HTTP **429 Too Many Requests (Demasiadas solicitudes)**. Implemente una estrategia de reintentos con retroceso exponencial o respete el encabezado `Retry-After` cuando ocurra la limitación.

---

## Punto de conexión <a name="punto-de-conexión"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*Actualiza el hipervínculo identificado por `hyperlinkIndex` en la hoja de cálculo `sheetName` del archivo `name`.*

---

## Parámetros <a name="parámetros"></a>

### Parámetros de ruta <a name="parámetros-de-ruta"></a>

| Nombre            | Tipo   | Obligatorio | Descripción |
|-------------------|--------|-------------|-------------|
| `name`            | string | ✅ | Nombre del archivo de Excel (incluyendo la extensión). |
| `sheetName`       | string | ✅ | Nombre de la hoja de cálculo que contiene el hipervínculo. |
| `hyperlinkIndex`  | integer| ✅ | Índice basado en cero del hipervínculo que se va a actualizar. |

### Parámetros de consulta <a name="parámetros-de-consulta"></a>

| Nombre          | Tipo   | Obligatorio | Descripción |
|-----------------|--------|-------------|-------------|
| `folder`        | string | ❌ | Ruta de la carpeta en el almacenamiento donde reside el libro. |
| `storageName`   | string | ❌ | Nombre del servicio de almacenamiento (por ejemplo, `Default`). |

### Esquema del cuerpo de solicitud <a name="esquema-del-cuerpo-de-solicitud"></a>

El cuerpo de la solicitud debe contener un objeto **`hyperlink`**. Solo es necesario proporcionar los campos que desee cambiar; los campos opcionales omitidos conservarán sus valores actuales.

| Campo              | Tipo   | Obligatorio | Descripción |
|--------------------|--------|-------------|-------------|
| `Address`          | string | ✅ | URL de destino del hipervínculo. |
| `Area`             | object | ✅ | Rango de celdas donde se coloca el hipervínculo. Debe contener `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (todos enteros, basados en cero). |
| `ScreenTip`        | string | ❌ | Sugerencia de pantalla que aparece al pasar el mouse sobre el hipervínculo. |
| `TextToDisplay`    | string | ❌ | Texto que se muestra dentro de la celda. |
| `link`             | object| ❌ | Enlaces hipermédia (`Href`, `Rel`, `Title`, `Type`). Por lo general, se omite en las cargas útiles de solicitud. |

**Definición del objeto `Area`**

| Subcampo          | Tipo   | Obligatorio | Descripción |
|-------------------|--------|-------------|-------------|
| `StartRow`        | integer| ✅ | Índice de fila inicial basado en cero. |
| `StartColumn`     | integer| ✅ | Índice de columna inicial basado en cero. |
| `EndRow`          | integer| ✅ | Índice de fila final basado en cero. |
| `EndColumn`       | integer| ✅ | Índice de columna final basado en cero. |

---

## Respuestas <a name="respuestas"></a>

### Respuesta correcta <a name="respuesta-correcta"></a>

| Campo | Tipo   | Descripción |
|-------|--------|-------------|
| `Code`| integer| Código de estado HTTP (200 para éxito). |
| `Status`| string| Estado textual (`OK`). |
| `Hyperlink`| object (opcional) | Objeto de hipervínculo actualizado, devuelto cuando se solicita el subobjeto `link`. |

**Ejemplo en JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Respuestas de error <a name="respuestas-de-error"></a>

| Código HTTP | Motivo | Cuerpo de ejemplo |
|-------------|--------|-------------------|
| **400** | Solicitud incorrecta: parámetros faltantes o no válidos. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | No autorizado: token JWT faltante o no válido. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | No encontrado: el libro, la hoja de cálculo o el hipervínculo no existen. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | Demasiadas solicitudes: se superó el límite de tasa. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | Error interno del servidor: fallo inesperado del servidor. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Ejemplo con cURL <a name="ejemplo-con-curl"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Respuesta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Consejo:* Guarde la carga útil JSON en un archivo (por ejemplo, `payload.json`) y referencíelo con `--data @payload.json` para una copia y pegado más limpia.

---

## Fragmentos de código del SDK <a name="fragmentos-de-código-del-sdk"></a>

Los siguientes fragmentos muestran cómo invocar **PostWorksheetHyperlink** mediante los SDK oficiales de Aspose.Cells Cloud. Reemplace los valores de marcador de posición (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>`, etc.) con datos reales.

| Lenguaje | Ejemplo |
|----------|--------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*Todos los SDK son de código abierto y se pueden encontrar en el [repositorio de GitHub de Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

---

## Consulte también <a name="consulte-también"></a>

- **Autenticación** – [Primeros pasos con tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Operaciones de almacenamiento** – [Cargar un archivo](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Otras operaciones de hipervínculos** – [Agregar un hipervínculo](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) \| [Eliminar un hipervínculo](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **Especificación OpenAPI** – Definición completa del punto de conexión: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*Documento actualizado por última vez: 2026‑07‑30*