---
title: "Agregar comentario en hoja de cálculo"
description: "Agregue un comentario a una celda específica en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, API en la nube, agregar comentario en hoja de cálculo, Excel, hoja de cálculo, comentario de celda"
weight: 20
api_version: "v3.0"
---

# Agregar comentario en hoja de cálculo

Agregue un comentario a una celda específica en una hoja de cálculo de un libro de Excel utilizando la API REST de Aspose.Cells Cloud.

---

## Requisitos previos / Autenticación

* Se requiere un **token Bearer JWT** para cada solicitud.  
  *Obtenga un token* a través del endpoint **/connect/token** (consulte la [guía de autenticación](/cells/authentication/)).  
* Incluya el token en el encabezado `Authorization`:

```http
Authorization: Bearer <jwt token>
```

* Todas las llamadas deben realizarse mediante **HTTPS** para proteger el token y los datos.

---

## Solicitud HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Parámetros de ruta

| Nombre       | Tipo   | Obligatorio | Descripción |
|--------------|--------|-------------|-------------|
| `name`       | string | ✔️ | Nombre del archivo del libro (por ejemplo, `test.xlsx`). |
| `sheetName`  | string | ✔️ | Nombre de la hoja de cálculo (por ejemplo, `Sheet1`). |
| `cellName`   | string | ✔️ | Dirección de la celda de destino (por ejemplo, `A1`). |

### Parámetros de consulta

| Nombre          | Tipo   | Obligatorio | Descripción |
|-----------------|--------|-------------|-------------|
| `folder`        | string | opcional    | Carpeta que contiene el libro. |
| `storageName`   | string | opcional    | Nombre del servicio de almacenamiento donde se encuentra el archivo. |

### Cuerpo de la solicitud

El cuerpo debe contener un objeto **Comment** en formato JSON.

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Campos del objeto Comment**

| Campo                     | Tipo    | Obligatorio | Descripción |
|---------------------------|---------|-------------|-------------|
| `CellName`                | string  | ✔️ | Dirección de la celda (debe coincidir con el valor de la ruta `{cellName}`). |
| `Author`                  | string  | opcional    | Nombre del autor del comentario. |
| `HtmlNote`                | string  | opcional    | Texto del comentario en formato HTML. |
| `Note`                    | string  | opcional    | Comentario en texto sin formato. |
| `AutoSize`                | boolean | opcional    | Ajustar automáticamente el tamaño del cuadro de comentario. |
| `IsVisible`               | boolean | opcional    | Mostrar el comentario de forma predeterminada. |
| `Width` / `Height`        | number  | opcional    | Tamaño del cuadro de comentario (en puntos). |
| `TextHorizontalAlignment`| string  | opcional    | Alineación horizontal (`Left`, `Center`, `Right`). |
| `TextOrientationType`     | string  | opcional    | Rotación del texto (`NoRotation`, `Rotate90`, …). |
| `TextVerticalAlignment`  | string  | opcional    | Alineación vertical (`Top`, `Center`, `Bottom`). |

---

## Ejemplo con cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## Esquema de respuesta

| Campo   | Tipo   | Descripción |
|---------|--------|-------------|
| `Comment` | object | Objeto de comentario creado (consulte **Campos del objeto Comment** anterior, más metadatos de enlace). |
| `Code`   | integer | Código de estado HTTP devuelto por la API (por ejemplo, `200`). |
| `Status` | string  | Mensaje de estado en texto (por ejemplo, `"OK"`). |

El objeto `Comment` también contiene un subobjeto **link**:

| Subcampo | Tipo   | Descripción |
|----------|--------|-------------|
| `Href`   | string | URL de autoreferencia para el recurso de comentario. |
| `Rel`    | string | Tipo de relación (`self`). |
| `Title`  | string | Título opcional (puede ser `null`). |
| `Type`   | string | Tipo MIME opcional (puede ser `null`). |

---

## Ejemplo de respuesta correcta

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Respuestas de error

| Código HTTP | Descripción | Ejemplo |
|-------------|-------------|---------|
| **400**     | Solicitud incorrecta: parámetros faltantes o no válidos. | `{ "Error": { "Code": "InvalidParameter", "Message": "El parámetro 'cellName' falta o tiene un formato incorrecto." }, "Code": 400, "Status": "Bad Request" }` |
| **401**     | No autorizado: token ausente o no válido. | `{ "Error": { "Code": "InvalidToken", "Message": "La autenticación falló." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**     | No encontrado: el libro, la hoja de cálculo o la celda no existen. | `{ "Error": { "Code": "FileNotFound", "Message": "No se encontró el libro 'test.xlsx'." }, "Code": 404, "Status": "Not Found" }` |
| **500**     | Error interno del servidor: condición inesperada en el servidor. | `{ "Error": { "Code": "ServerError", "Message": "Se produjo un error inesperado." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## Ejemplos con SDK

Los SDK siguientes proporcionan envoltorios listos para usar para esta operación. Reemplace los valores de marcador de posición (`<YOUR_TOKEN>`, `<FILE_NAME>`, etc.) con datos reales.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Configurar cliente de la API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Preparar objeto de comentario
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Consulte también

* **Obtener comentario en hoja de cálculo** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Actualizar comentario en hoja de cálculo** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Eliminar comentario en hoja de cálculo** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Borrar todos los comentarios** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## Notas adicionales

* La ruta del endpoint incluye **v3.0**. Hay disponible una versión más reciente (**v3.1**); actualice la URL base según sea necesario si necesita las características más recientes.  
* Para ver la definición completa de OpenAPI, visite la [referencia de la API de Aspose.Cells Cloud](/cells/#/Worksheets/PutWorksheetComment).  
* Recuerde manejar la limitación de tasa (HTTP 429) y reintentar según las directrices de la API.  

---