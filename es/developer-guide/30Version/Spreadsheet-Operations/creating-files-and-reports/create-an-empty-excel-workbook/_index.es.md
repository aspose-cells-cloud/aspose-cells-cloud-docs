---
title: "Crear un libro de Excel vacío"
second_title: "Documentos"
linktype: "Libro vacío"
type: docs
url: /es/create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, libro vacío, API REST, SDK"
description: "Aprenda a crear un libro de Excel vacío utilizando la API REST de Aspose.Cells Cloud. Incluye ejemplos en cURL y SDK."
weight: 20
ArticleTitle: "Crear un libro de Excel vacío mediante la API de Aspose.Cells Cloud"
---

Esta API REST crea un **libro vacío**.

## API PutWorkbookCreate

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de consulta

| Nombre del parámetro | Tipo    | Descripción                                                     |
| -------------------- | ------- | --------------------------------------------------------------- |
| templateFile         | string  | Ruta al libro de plantilla que se usará como base (opcional).  |
| dataFile             | string  | Ruta al archivo de datos para poblar el libro (opcional).      |
| isWriteOver          | boolean | `true` para sobrescribir un archivo existente; `false` en caso contrario. |
| folder               | string  | Carpeta de destino para el libro creado (opcional).            |
| storageName          | string  | Nombre del servicio de almacenamiento a utilizar.              |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción                                   |
| -------------------- | ---- | --------------------------------------------- |
| data                 | file | Contenido binario del archivo de libro a crear. |

### **Respuesta**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Cuando se devuelve                      |
|--------|-----------------------------|-----------------------------------------|
| 200 OK | Libro creado correctamente  | Flujo normal                            |
| 201 Created | Libro creado (respuesta alternativa) | Cuando la API devuelve un estado de creado |
| 400 Bad Request | Parámetros inválidos | Error del lado del cliente              |
| 401 Unauthorized | Token ausente o inválido | Error de autenticación                 |
| 409 Conflict | El archivo existe y `isWriteOver=false` | Conflicto con el archivo existente      |

## Cómo utilizar la API PutWorkbookCreate con SDK

### Especificación de la API PutWorkbookCreate

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) define una interfaz de programación accesible públicamente y le permite llevar a cabo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder a los servicios web de Aspose.Cells. Incluya el encabezado `Authorization` con un token de acceso OAuth2/JWT válido. Para un libro vacío, el cuerpo de la solicitud es opcional; si necesita cargar un archivo, agregue `--data-binary @empty.xlsx` como se muestra a continuación.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Crear un libro vacío llamado newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Omita esta línea para un libro verdaderamente vacío
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

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---