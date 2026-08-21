---
title: "Eliminar duplicados"
ArticleTitle: "Eliminar duplicados – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Eliminar duplicados"
type: docs
url: /es/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Eliminar duplicados, API"
description: "Elimina valores duplicados en una hoja de cálculo, un rango o una tabla."
weight: 1000
---

## El método Eliminar duplicados de los servicios web de Aspose.Cells Cloud

Elimina valores duplicados en la hoja de cálculo, el rango o la tabla. Este método escanea el ámbito de destino buscando filas con valores idénticos en las columnas especificadas a verificar. Para cada conjunto de duplicados, se eliminan todas las ocurrencias excepto la primera. La comparación suele ser sensible a mayúsculas y minúsculas y coincide exactamente con el valor de la celda.

### Punto de conexión de la API web

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción |
|----------------------|--------|-------------------------------------|-------------|
| Spreadsheet          | Archivo | FormData                            | Carga el archivo de hoja de cálculo. |
| worksheet            | Cadena  | Consulta                            | Nombre de la hoja de cálculo. (opcional) |
| range                | Cadena  | Consulta                            | Nombre del rango que necesita eliminación de duplicados. (opcional) |
| table                | Cadena  | Consulta                            | Nombre de la tabla que necesita eliminación de duplicados. (opcional) |
| outPath              | Cadena  | Consulta                            | (Opcional) Ruta de la carpeta donde se almacena el libro de cálculo. El valor predeterminado es null. |
| outStorageName       | Cadena  | Consulta                            | Nombre del almacenamiento para el archivo de salida. |
| region               | Cadena  | Consulta                            | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | Cadena  | Consulta                            | Contraseña para abrir el archivo de hoja de cálculo. |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción |
| -------------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Respuesta**

```json
{
  "File": "flujo binario de la hoja de cálculo resultante (por ejemplo, .xlsx)"
}
```

**Códigos de estado de la respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | La hoja de cálculo resultante, con duplicados eliminados, se devuelve como un flujo de archivo. |
| 400 | Solicitud incorrecta | Parámetros de solicitud inválidos o URL mal formada. |
| 401 | No autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 413 | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño permitido. |
| 500 | Error interno del servidor | Se ha producido una anomalia en la hoja de cálculo al obtener datos u otro error del lado del servidor. |

## Cómo usar la función Eliminar duplicados con SDK

### Especificación de Eliminar duplicados

La [especificación de la API Eliminar duplicados](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}
{< tab tabNum="1" >}
```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=es-ES&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "flujo binario de la hoja de cálculo resultante (por ejemplo, .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Utilizar los SDK de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose Cells Cloud utilizando diversos SDK:

```csharp
// Código de ejemplo del SDK para C#
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "es-ES",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Código de ejemplo del SDK para Java
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "es-ES",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Código de ejemplo del SDK para Python
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='es-ES',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Excepción al llamar a TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---