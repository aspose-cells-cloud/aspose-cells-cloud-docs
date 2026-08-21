---
---
title: "Eliminar carpeta – Aspose.Cells Cloud API | Eliminar carpetas mediante REST"
description: "Aprenda a eliminar una carpeta (opcionalmente de forma recursiva) del almacenamiento en la nube de Aspose.Cells Cloud utilizando el endpoint DELETE /v4.0/cells/storage/folder/{path}. Incluye sintaxis de solicitud, parámetros, autenticación, código de ejemplo y manejo de errores."
keywords: "Aspose.Cells, eliminar carpeta, almacenamiento en la nube, API, REST, Excel, gestión de archivos"
slug: eliminar-carpeta
date: 2026-07-30
---

# Eliminar carpeta – Aspose.Cells Cloud API

Elimine una carpeta (y opcionalmente todo su contenido) del almacenamiento en la nube de Aspose.Cells Cloud.

---

## Descripción general

La operación **Eliminar carpeta** elimina permanentemente una carpeta de una cuenta de almacenamiento utilizada por Aspose.Cells Cloud.  
Puede eliminar una carpeta vacía o, estableciendo la marca `recursive` en `true`, eliminar la carpeta junto con todos los archivos y subcarpetas que contiene. Este punto de conexión se utiliza comúnmente en scripts de limpieza, flujos de trabajo automatizados o cuando ya no se necesitan directorios temporales.

---

## Solicitud HTTP

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – la ruta completa de la carpeta que se va a eliminar (codificada en URL).

### Cabeceras HTTP obligatorias

| Cabecera          | Valor                              | Descripción                              |
|-------------------|------------------------------------|------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | Token JWT obtenido del servicio de autenticación. |
| `Accept`          | `application/json`                | Formato de respuesta esperado.           |
| `Content-Type`    | `application/json` *(opcional)*   | No es obligatorio para DELETE, pero puede enviarse. |

---

## Autenticación

Aspose.Cells Cloud utiliza **autenticación basada en tokens JWT**.  
Obtenga un token de acceso mediante el [punto de conexión de autenticación](/authentication/) e inclúyalo en la cabecera `Authorization` como se muestra arriba.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Parámetros

| Nombre          | Tipo    | Ubicación | Obligatorio | Descripción                                                                 |
|-----------------|---------|-----------|-------------|-----------------------------------------------------------------------------|
| `path`          | string  | Ruta      | Sí          | Ruta de la carpeta que se va a eliminar (codificada en URL).               |
| `storageName`   | string  | Consulta  | No          | Nombre del almacenamiento que contiene la carpeta. Si se omite, se utiliza el almacenamiento predeterminado. |
| `recursive`     | boolean | Consulta  | No          | `true` → elimina la carpeta **y todo su contenido**. El valor predeterminado es `false`. |

**Ejemplo de cadena de consulta**

```
?storageName=MyStorage&recursive=true
```

---

## Ejemplo de solicitud (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Respuesta

Una solicitud correcta devuelve **HTTP 200 OK** con un objeto JSON vacío:

```json
{}
```

No se proporciona ninguna carga adicional porque el resultado de la operación es binario: la carpeta se elimina o se devuelve un error.

---

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado del servidor. |

Cuando ocurre un error, el cuerpo contiene un objeto JSON con los campos `code` y `message` que describen el problema.

---

## Ejemplos de código con SDK

Los siguientes ejemplos muestran cómo llamar a **Eliminar carpeta** con los SDK oficialmente admitidos. Reemplace `{access_token}` y los valores de los parámetros con los suyos propios.

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configurar cliente de API
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Eliminar carpeta (recursivamente)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// Inicializar cliente de API
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// Configurar
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Eliminar carpeta recursivamente
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Folder deleted.";
} catch (Exception $e) {
    echo 'Exception when calling FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Folder deleted.'
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Folder deleted'))
    .catch(err => console.error('Error:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Folder deleted")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Folder deleted.\n";
};
if ($@) {
    warn "Error deleting folder: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println("Folder deleted")
}
```
</details>

---

## Consulte también

- **[Crear carpeta](/create-folder/)** – Cree una carpeta nueva en el almacenamiento en la nube.  
- **[Copiar carpeta](/copy-folder/)** – Duplicar una carpeta y su contenido.  
- **[Mover carpeta](/move-folder/)** – Trasladar una carpeta a una ruta diferente.  
- **[Especificación OpenAPI]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">Operación DeleteFolder</a> (explorador interactivo de API).

---

## Lista de verificación de SEO y accesibilidad (interna)

- **Título y H1** utilizan el guión largo correcto (`–`) y contienen la palabra clave principal *Eliminar carpeta*.  
- Todos los encabezados siguen una jerarquía lógica (`H1 → H2 → H3`).  
- No quedan artefactos de codificación UTF‑8.  
- Las palabras clave de metadatos se han consolidado en una única lista limpia (u omitidas si se prefiere).  
- Los enlaces externos incluyen `rel="noopener noreferrer"` por seguridad.  
- Los iconos de la interfaz de usuario y las banderas de idioma (si se representan en la página) deben incluir atributos `aria-label`/`alt` (por ejemplo, `aria-label="Español (ES)"`).  
- Se recomiendan etiquetas `<link rel="alternate" hreflang="xx" href="…">` en el encabezado de la página para cada versión lingüística.  

---