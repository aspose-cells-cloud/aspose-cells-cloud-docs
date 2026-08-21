---
title: "Convertir objeto OLE a imagen – Aspose.Cells Cloud REST API"
description: "Recuperar un objeto OLE incrustado en una hoja de cálculo de Excel y convertirlo a PNG, JPEG, TIFF, GIF, EMF o BMP mediante la API REST de Aspose.Cells Cloud."
keywords:
  - "convertir objeto OLE a imagen"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "conversión de imagen"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# Convertir objeto OLE a imagen

Recuperar un objeto OLE incrustado en una hoja de cálculo y devolverlo en el formato de imagen solicitado.

---

## Requisitos previos

Antes de llamar a este endpoint, asegúrese de cumplir con lo siguiente:

1. **Cuenta de Aspose.Cells Cloud**: regístrese en el [portal de Aspose Cloud](https://dashboard.aspose.cloud/).  
2. **Libro de cálculo cargado en el almacenamiento en la nube**: utilice la API **Cargar archivo** o la interfaz de usuario de Aspose Cloud.  
3. **Token de acceso JWT**: obtenga un token siguiendo la [guía de autenticación](/total/getting-started/rest-api-overview/authenticating-api-requests/).  

---

## Seguridad y autenticación

Todas las API de Aspose.Cells Cloud requieren **autenticación basada en token JWT**. Incluya el token en el encabezado `Authorization`:

```http
Authorization: Bearer <jwt-token>
```

Solo se admiten endpoints HTTPS; nunca utilice `http://`.

---

## Solicitud

### Método HTTP
`GET`

### Endpoint
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Parámetros de ruta

| Nombre          | Tipo   | Obligatorio | Descripción                              |
|-----------------|--------|-------------|------------------------------------------|
| `name`          | string | ✅          | Nombre del archivo del libro de cálculo (por ejemplo, `Book1.xlsx`). |
| `sheetName`     | string | ✅          | Hoja de cálculo que contiene el objeto OLE. |
| `objectNumber`  | integer| ✅          | Índice basado en cero del objeto OLE.    |

### Parámetros de consulta

| Nombre        | Tipo   | Obligatorio | Descripción |
|---------------|--------|-------------|-------------|
| `format`      | string | ❌          | Formato de imagen deseado (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). Si se omite, el valor predeterminado es `png`. |
| `folder`      | string | ❌          | Ruta a la carpeta donde reside el libro de cálculo. |
| `storageName` | string | ❌          | Nombre del servicio de almacenamiento (por ejemplo, `MyCloud`). |

---

## Ejemplo de solicitud (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*Reemplace `<jwt-token>` con un token JWT válido.*

---

## Respuesta

| Estado | Tipo de contenido          | Descripción |
|--------|----------------------------|-------------|
| `200`  | `image/png` (o el formato solicitado) | Datos binarios de la imagen que representa el objeto OLE. |
| `400`  | `application/json`         | Parámetros de solicitud inválidos. |
| `401`  | `application/json`         | Fallo de autenticación (JWT ausente o inválido). |
| `404`  | `application/json`         | No se encontró el libro de cálculo, la hoja de cálculo o el objeto OLE especificados. |
| `500`  | `application/json`         | Error del lado del servidor. |

### Manejo de la carga binaria

La API devuelve bytes de imagen en bruto. Puede:

* **Guardar directamente en un archivo** (ejemplo en Linux/macOS):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **Codificar en Base64** para depuración o incrustación en JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *Ejemplo (truncado) de salida en Base64:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Respuestas de error

| Estado HTTP | Código                   | Mensaje |
|-------------|--------------------------|---------|
| `400`       | `InvalidParameter`       | Uno o más parámetros de solicitud no son válidos. |
| `401`       | `AuthenticationFailed`   | Token JWT ausente o inválido. |
| `404`       | `PropertyNotFound`       | El libro de cálculo, la hoja de cálculo o el objeto OLE solicitados no existen. |
| `500`       | `InternalError`          | Se produjo un error inesperado en el servidor. |

---

## Ejemplos de SDK

Los fragmentos siguientes muestran cómo invocar la operación con los SDK oficiales. Reemplace `YOUR_JWT_TOKEN` y otros marcadores de posición con sus valores reales.

| Lenguaje | Ejemplo |
|----------|---------|
| **C#** | <details><summary>Mostrar código</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: "Embedded_OleObject_Sample_Book1.xlsx",\n    sheetName: "Sheet1",\n    objectNumber: 0,\n    format: "png"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create("oleobject.png");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Mostrar código</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken("YOUR_JWT_TOKEN");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    "Embedded_OleObject_Sample_Book1.xlsx",\n    "Sheet1",\n    0,\n    "png",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream("oleobject.png")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Mostrar código</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = "YOUR_JWT_TOKEN"\nrequest = GetWorksheetOleObjectRequest(\n    name="Embedded_OleObject_Sample_Book1.xlsx",\n    sheet_name="Sheet1",\n    object_number=0,\n    format="png"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Mostrar código</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Mostrar código</summary>```go\npackage main\nimport (\n    "io"\n    "os"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = "YOUR_JWT_TOKEN"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         "Embedded_OleObject_Sample_Book1.xlsx",\n        SheetName:    "Sheet1",\n        ObjectNumber: 0,\n        Format:       "png",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create("oleobject.png")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Mostrar código</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Mostrar código</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Mostrar código</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(La lista completa de SDK está disponible en el [repositorio de GitHub](https://github.com/aspose-cells-cloud).)*

---

## Operaciones relacionadas

- **Agregar objeto OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **Actualizar objeto OLE** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Eliminar objeto OLE** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Obtener lista de objetos OLE** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

Para más detalles, consulte las páginas de referencia correspondientes de la API.

---

## Recursos adicionales

- **Especificación OpenAPI** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Guía de autenticación** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **Repositorios de SDK** – <https://github.com/aspose-cells-cloud>
- **Rendimiento y accesibilidad**: ejecute auditorías con Lighthouse y axe‑core para garantizar tiempos de carga óptimos y cumplimiento con WCAG 2.1 AA.