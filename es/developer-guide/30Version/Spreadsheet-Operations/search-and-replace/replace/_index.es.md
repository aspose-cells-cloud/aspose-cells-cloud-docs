---
title: "Reemplazar texto en archivos de Excel"
second_title: "Documento"
linktitle: "Reemplazar sin usar almacenamiento"
type: docs
url: /es/replace/
keywords: "reemplazar texto en Excel, Aspose.Cells Cloud, API REST, reemplazo en hojas de cálculo, API, reemplazo de texto en archivos de Excel"
description: "Use la API REST de Aspose.Cells Cloud para reemplazar texto existente por nuevos valores en archivos de Excel. Admite SDK para C#, Java, Python, Node.js, PHP, Ruby, Go y Perl."
weight: 80
---


## API REST

Esta API REST reemplaza datos en archivos de Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación             | Descripción                                           |
|----------------------|--------|-----------------------|-------------------------------------------------------|
| **file**             | archivo | formData (multipart)  | Archivo de Excel que se va a procesar.               |
| **text**             | cadena | query                 | Cadena de texto que se va a reemplazar.              |
| **newtext**          | cadena | query                 | Texto de reemplazo.                                   |
| **password**         | cadena | query                 | Contraseña para un libro de trabajo protegido (opcional). |
| **sheetname**        | cadena | query                 | Nombre de la hoja de cálculo objetivo (opcional).    |

### **Respuesta**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[nombre_del_archivo1]",
      "Filesize" : [tamaño_del_archivo],
      "FileContent" : "[CadenaEnBase64]"
    },
    {
      "Filename" : "[nombre_del_archivo2]",
      "Filesize" : [tamaño_del_archivo],
      "FileContent" : "[CadenaEnBase64]"
    },
    {
      "Filename" : "[nombre_del_archivo3]",
      "Filesize" : [tamaño_del_archivo],
      "FileContent" : "[CadenaEnBase64]"
    }
  ]
}
```

**Códigos de estado HTTP**

| Código | Significado                     | Descripción                                                  |
|--------|----------------------------------|--------------------------------------------------------------|
| 200    | OK                               | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta             | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                    | Token JWT inválido o ausente.                                |
| 413    | Carga útil demasiado grande     | El archivo subido supera el límite de tamaño.               |
| 500    | Error interno del servidor      | Error inesperado en el servidor.                             |

## Cómo usar la API PostReplace con SDK

### Especificación de la API PostReplace

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) define una interfaz de programación pública y accesible, lo que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <token_jwt>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----CadenaEnBase64--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----CadenaEnBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}

---