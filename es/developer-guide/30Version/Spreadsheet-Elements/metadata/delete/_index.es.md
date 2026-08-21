---
title: "Eliminar metadatos de archivos de Excel"
second_title: "Documento"
linktitle: "Eliminar sin usar almacenamiento"
type: docs
url: /es/metadata/delete/
keywords: "Aspose.Cells, eliminar metadatos, API de Excel, propiedades del libro"
description: "Eliminar metadatos del libro (autor, título, personalizados) mediante la API en la nube Aspose.Cells. Incluye el punto de conexión, autenticación, parámetros y ejemplos con cURL y SDK."
weight: 55
ArticleTitle: "Eliminar metadatos de archivos de Excel – Documentación de Aspose.Cells Cloud"
---

**Visión general**  
La operación *Eliminar metadatos* elimina permanentemente todas las propiedades del libro (estándar y personalizadas) del archivo(s) de Excel cargado(s) y devuelve el(s) archivo(s) procesado(s) en la respuesta.

**Requisitos previos**  
- Un token JWT válido de Aspose.Cells Cloud (obtenible mediante el flujo de autenticación OAuth 2.0).  
- Versión de la API **v3.0** (el punto de conexión utilizado en este ejemplo).  
- Para el uso de SDKs, instale el SDK de Aspose.Cells Cloud adecuado para su lenguaje (por ejemplo, mediante NuGet, Maven, npm, pip, CPAN o módulos de Go).

Esta API REST elimina **metadatos** de uno o más archivos de Excel. Elimina propiedades del libro como autor, título y datos personalizados, y devuelve los archivos limpios.

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                  |
| -------------------- | ------ | --------- | ------------------------------------------------------------ |
| file                 | archivo | formData  | Archivo de Excel para cargar y eliminarle los **metadatos** |
| type                 | string | query     | Tipo de operación; establezca en **all** para eliminar todos los **metadatos** |

La <a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Respuestas de error** pueden incluir:

- **400 Solicitud incorrecta** – archivo faltante o valor `type` no válido.
- **401 No autorizado** – token JWT inválido o faltante.
- **500 Error interno del servidor** – error de procesamiento del lado del servidor.

La API devuelve un objeto JSON que contiene un campo `Error` con detalles para cada caso.

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200 | Correcto | Metadatos eliminados, archivo devuelto |
| 400 | Solicitud incorrecta | Archivo faltante o `type` no válido |
| 401 | No autorizado | JWT inválido o faltante |
| 500 | Error interno del servidor | Fallo en el procesamiento del servidor |

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}