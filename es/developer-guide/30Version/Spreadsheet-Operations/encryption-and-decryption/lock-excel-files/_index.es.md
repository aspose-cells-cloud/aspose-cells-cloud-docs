---
title: "Bloquear archivos de Excel"
second_title: "Documento"
linktitle: "Bloquear archivos de Excel"
type: docs
url: /es/lock-excel-files/
aliases: [  /es/lock/without-storage/ , /es/lock/ , /es/lock/without-using-storage/ ]
keywords: "Bloquear, Excel, API, Aspose.Cells, Cloud, REST, Libro de trabajo, Hoja de cálculo, SDK"
description: "Aprenda cómo bloquear libros de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye el endpoint HTTPS, autenticación, solicitud cURL, esquema de respuesta y ejemplos de código SDK para C#, Java, Python y más."
ArticleTitle: "Bloquear archivos de Excel – Documentación de la API de Aspose.Cells Cloud"
weight: 70
---

**Versión de la API:** v3.0 (actual)

Esta API REST **bloquea** libros de Excel.

## API PostLock

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Requisitos previos** – La solicitud debe enviarse mediante **HTTPS** e incluir un token válido de OAuth 2.0 Bearer en el encabezado `Authorization`.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación                   | Descripción                                           |
|----------------------|--------|-----------------------------|-------------------------------------------------------|
| file                 | archivo| datos de formulario (cuerpo multipart) | El libro de Excel que se subirá y bloqueará. |
| password             | string | cadena de consulta          | Contraseña para el libro de trabajo (opcional).      |

La <a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo **llamar** a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*Puede descargar un libro de ejemplo — [Sample.xlsx](https://example.com/Sample.xlsx) — para probar la solicitud.*

**Nota:** La API admite archivos de hasta 100 MB; cargas más grandes pueden provocar una respuesta 413 (Payload Too Large).

### **Detalles de la respuesta**

| Campo         | Tipo             | Descripción                                              |
|---------------|------------------|----------------------------------------------------------|
| Filename      | string           | Nombre del libro de trabajo bloqueado devuelto por el servicio. |
| FileSize      | integer          | Tamaño del archivo bloqueado en bytes.                   |
| FileContent   | string (Base64)  | El libro de trabajo bloqueado codificado como una cadena Base64. |

Para recuperar el libro de trabajo bloqueado, decodifique el valor `FileContent` desde Base64 y guárdelo utilizando el `Filename` indicado en la respuesta.

### **Manejo de errores**

– La API devuelve códigos de estado HTTP estándar (por ejemplo, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) junto con un objeto JSON de error que contiene los campos `Code` y `Message`.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}
---