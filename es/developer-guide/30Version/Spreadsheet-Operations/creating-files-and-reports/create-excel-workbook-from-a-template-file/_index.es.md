---
title: "Cómo crear un libro de Excel con un archivo de plantilla"
second_title: "Document"
linktitle: "Archivo de plantilla"
type: docs
url: /es/create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, plantilla, API, Aspose.Cells, libro de trabajo, REST, Cloud"
description: "Aprenda cómo generar libros de Excel a partir de archivos de plantilla utilizando la API REST de Aspose.Cells Cloud. Incluye requisitos previos, pasos de autenticación, ejemplos de cURL, detalles sobre manejo de errores y fragmentos de código de SDK."
weight: 30
---

# Cómo crear un libro de Excel con un archivo de plantilla

Cree un nuevo libro de Excel utilizando un archivo de plantilla existente y, opcionalmente, un archivo de datos que proporcione valores para marcadores inteligentes (*Smart-Markers*). La operación se realiza a través del punto de conexión **PUT** `/cells/{name}` de Aspose.Cells Cloud.

---

## Requisitos previos

| Requisito | Descripción |
|-----------|-------------|
| **Cuenta de Aspose.Cells Cloud** | Regístrese en https://dashboard.aspose.cloud/ y obtenga su **Client Id** / **Client Secret**. |
| **Token de acceso JWT** | Genere un token JWT según se describe en la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Archivo de plantilla** | Cargue el archivo de Excel de plantilla (por ejemplo, `Calendar.xlsx`) en su almacenamiento elegido mediante la API **Upload File** o la interfaz de usuario. |
| **Archivo de datos (opcional)** | Un archivo JSON o XML que contiene valores para marcadores inteligentes (por ejemplo, `Sample_Data.xml`). |
| **Almacenamiento compatible** | Almacenamiento predeterminado (`Default`) o un almacenamiento personalizado configurado en su cuenta de Aspose. |

---

## Autenticación

Todas las solicitudes a Aspose.Cells Cloud requieren un **token JWT Bearer** pasado en el encabezado `Authorization`:

```http
Authorization: Bearer {access_token}
```

El token debe obtenerse con anterioridad y, de forma predeterminada, tiene una validez de 1 hora.

---

## Solicitud

### Solicitud HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Componente | Valor |
|------------|-------|
| **Método** | `PUT` |
| **Ruta**   | `/cells/{name}` – `name` es el nombre deseado para el nuevo libro de trabajo (incluyendo la extensión, por ejemplo, `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (cuando se envía un archivo de datos en el cuerpo). |
| **Accept** | `application/json` |

### Parámetro de ruta

| Nombre | Tipo | Obligatorio | Descripción |
|--------|------|-------------|-------------|
| `name` | string | **Sí** | Nombre del libro de trabajo que se creará (por ejemplo, `newworkbook.xlsx`). |

### Parámetros de consulta

| Parámetro | Tipo | Obligatorio | Valor predeterminado | Descripción |
|-----------|------|-------------|----------------------|-------------|
| `templateFile` | string | No | — | Nombre del archivo de plantilla almacenado en la nube. |
| `dataFile` | string | No | — | Nombre del archivo de datos (XML o JSON) almacenado en la nube. |
| `isWriteOver` | boolean | No | `false` | Sobrescribir el archivo de destino si ya existe. Pase `true` o `false` **sin** comillas. |
| `folder` | string | No | — | Ruta de carpeta donde reside la plantilla (y opcionalmente el archivo de datos). |
| `storageName` | string | No | — | Nombre del servicio de almacenamiento que contiene los archivos. |
| `checkExcelRestriction` | boolean | No | `true` | Validar el libro de trabajo frente a las restricciones de Excel antes de su creación. |

### Cuerpo de la solicitud (opcional)

Cuando los datos para los marcadores de posición de marcadores inteligentes se envían directamente en la solicitud, inclúyalos como una parte de archivo multipart con el nombre **`data`**.

| Nombre de la parte | Tipo | Descripción |
|--------------------|------|-------------|
| `data` | file | Archivo XML o JSON que contiene valores para marcadores inteligentes. |

#### Ejemplo de cURL con cuerpo de solicitud

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*Si se utiliza el parámetro de consulta `dataFile` en lugar del cuerpo multipart, omita la bandera `-F`.*

---

## Respuesta

Una llamada exitosa devuelve un código **`200 OK`** (o **`201 Created`** cuando se genera un nuevo archivo) con una carga útil JSON que describe el libro de trabajo creado.

```json
{
    "Code": 200,
    "Status": "OK",
    "File": {
        "Name": "newworkbook.xlsx",
        "Size": 18234,
        "Path": "output/newworkbook.xlsx",
        "Url": "https://api.aspose.cloud/v3.0/storage/file/output/newworkbook.xlsx"
    }
}
```

### Tipos de datos de respuesta

| Propiedad | Tipo | Descripción |
|-----------|------|-------------|
| `Code` | integer | Código de estado similar al HTTP devuelto por la API. |
| `Status` | string | Descripción textual del estado. |
| `File` | object | Detalles del libro de trabajo generado. |
| `File.Name` | string | Nombre del archivo del libro de trabajo creado. |
| `File.Size` | integer | Tamaño en bytes. |
| `File.Path` | string | Ruta relativa dentro del almacenamiento. |
| `File.Url` | string | URL directa para descarga (requiere el mismo token JWT). |

---

**Códigos de estado HTTP**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | OK | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400 | Solicitud incorrecta | Parámetros faltantes o tipo de archivo no válido (por ejemplo, tipo de archivo no admitido). |
| 401 | No autorizado | Token JWT inválido o ausente. |
| 413 | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500 | Error interno del servidor | Error inesperado del servidor. |

---

## Ejemplos de SDK

Los siguientes fragmentos muestran cómo invocar **PutWorkbookCreate** utilizando los SDK oficiales de Aspose.Cells Cloud.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | Nombre del nuevo documento.
var templateFile = "Calendar.xlsx"; // string | Nombre del archivo de plantilla.
var dataFile = "Sample_Data.xml"; // string | Nombre del archivo de datos (opcional).
var isWriteOver = true; // bool? | Sobrescribir si existe.
var folder = "templates"; // string | Carpeta donde residen los archivos.
var storageName = "MyStorage"; // string | Nombre del almacenamiento.

using (var dataStream = File.OpenRead("Sample_Data.xml"))
{
    var response = apiInstance.PutWorkbookCreate(
        name,
        templateFile: templateFile,
        dataFile: dataFile,
        isWriteOver: isWriteOver,
        folder: folder,
        storageName: storageName,
        data: dataStream);
    Console.WriteLine(response);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cloud.cells.api.WorkbookApi;
import com.aspose.cloud.cells.model.*;

import java.io.File;
import java.io.FileInputStream;

WorkbookApi api = new WorkbookApi();
String name = "newworkbook.xlsx";
String templateFile = "Calendar.xlsx";
String dataFile = "Sample_Data.xml";
Boolean isWriteOver = true;
String folder = "templates";
String storageName = "MyStorage";

FileInputStream dataStream = new FileInputStream(new File("Sample_Data.xml"));
CellsCloudResponse response = api.putWorkbookCreate(
        name,
        templateFile,
        dataFile,
        isWriteOver,
        folder,
        storageName,
        dataStream);
System.out.println(response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorkbookApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new WorkbookApi(null, $config);
$name = "newworkbook.xlsx";
$templateFile = "Calendar.xlsx";
$dataFile = "Sample_Data.xml";
$isWriteOver = true;
$folder = "templates";
$storageName = "MyStorage";

$data = fopen("Sample_Data.xml", "r");
$result = $apiInstance->putWorkbookCreate($name, $templateFile, $dataFile, $isWriteOver, $folder, $storageName, $data);
print_r($result);
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::WorkbookApi.new
api.config.access_token = '{access_token}'

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = true
folder = 'templates'
storage_name = 'MyStorage'

File.open('Sample_Data.xml', 'rb') do |data|
  response = api.put_workbook_create(name,
                                     template_file: template_file,
                                     data_file: data_file,
                                     is_write_over: is_write_over,
                                     folder: folder,
                                     storage_name: storage_name,
                                     data: data)
  puts response
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorkbookApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

let config = new Configuration();
config.accessToken = '{access_token}';
config.basePath = 'https://api.aspose.cloud';

let apiInstance = new WorkbookApi(config);

let name = 'newworkbook.xlsx';
let templateFile = 'Calendar.xlsx';
let dataFile = 'Sample_Data.xml';
let isWriteOver = true;
let folder = 'templates';
let storageName = 'MyStorage';

let data = fs.createReadStream('Sample_Data.xml');

apiInstance.putWorkbookCreate(name, templateFile, dataFile, isWriteOver, folder, storageName, data)
    .then(response => console.log(response))
    .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.apis import WorkbookApi
from asposecellscloud.models import CellsCloudResponse

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api_instance = WorkbookApi(asposecellscloud.ApiClient(config))

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = True
folder = 'templates'
storage_name = 'MyStorage'

with open('Sample_Data.xml', 'rb') as data:
    response = api_instance.put_workbook_create(
        name,
        template_file=template_file,
        data_file=data_file,
        is_write_over=is_write_over,
        folder=folder,
        storage_name=storage_name,
        data=data)
    print(response)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorkbookApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::Api::WorkbookApi->new($config);

my $name = 'newworkbook.xlsx';
my $template_file = 'Calendar.xlsx';
my $data_file = 'Sample_Data.xml';
my $is_write_over = 1;
my $folder = 'templates';
my $storage_name = 'MyStorage';

open my $fh, '<:raw', 'Sample_Data.xml' or die $!;
my $response = $api_instance->put_workbook_create(
    name => $name,
    template_file => $template_file,
    data_file => $data_file,
    is_write_over => $is_write_over,
    folder => $folder,
    storage_name => $storage_name,
    data => $fh);
print $response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "os"

    asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorkbookApi(cfg)

    name := "newworkbook.xlsx"
    templateFile := "Calendar.xlsx"
    dataFile := "Sample_Data.xml"
    isWriteOver := true
    folder := "templates"
    storageName := "MyStorage"

    data, _ := os.Open("Sample_Data.xml")
    defer data.Close()

    result, _, err := apiInstance.PutWorkbookCreate(name, &templateFile, &dataFile, &isWriteOver, &folder, &storageName, data)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Printf("Response: %+v\n", result)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Manejo de errores

| Código de estado | Situación | Acción recomendada |
|------------------|-----------|--------------------|
| **400** | Parámetros obligatorios ausentes o tipo de archivo no válido. | Verifique los parámetros de consulta y asegúrese de que los archivos de plantilla y datos existan y sean compatibles (`.xlsx`, `.xml`, `.json`). |
| **401** | Token JWT ausente, caducado o mal formado. | Regenere un nuevo token de acceso utilizando su Client Id/Secret. |
| **413** | El archivo cargado excede el límite de tamaño del servicio (50 MB de forma predeterminada). | Reduzca el tamaño del archivo o divida el libro de trabajo en partes más pequeñas. |
| **500** | Error inesperado del servidor. | Reintente tras un breve retraso; si el problema persiste, póngase en contacto con el soporte de Aspose con el valor del encabezado `Request‑Id`. |

---

## Consulte también

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Guarde un libro de trabajo existente en un formato especificado.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Recupere información del libro de trabajo o descargue el archivo.  
- **[API Upload File](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Cargue archivos de plantilla o datos al almacenamiento en la nube.  

---