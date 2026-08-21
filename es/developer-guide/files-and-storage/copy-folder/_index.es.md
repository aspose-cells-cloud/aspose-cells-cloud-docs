---
title: "API de Copia de Carpetas de Aspose.Cells Cloud – Copiado Rápido de Carpetas en la Nube"
second_title: "Documento"
ArticleTitle: "Solución de Gestión de Archivos de Excel Basada en la Nube – Explicación Detallada de la Funcionalidad de Copia por Lotes de la API Copiar Carpeta de Aspose.Cells Cloud"
linktitle: "Copiar Carpeta"
type: docs
url: /copy-folder/
keywords: "Copiar Carpeta, Aspose.Cells Cloud, API REST, Almacenamiento en la Nube, Gestión de Hojas de Cálculo"
description: "Aprenda cómo copiar carpetas en el almacenamiento de Aspose.Cells Cloud mediante una única llamada REST. Incluye el endpoint, parámetros, solicitudes de ejemplo, códigos de error y ejemplos de SDK."
weight: 100
---

La API **CopyFolder** duplica una carpeta existente dentro del almacenamiento de Aspose.Cells Cloud. Esto resulta útil para crear copias de seguridad, reorganizar datos o preparar una jerarquía de carpetas para su posterior procesamiento sin necesidad de mover archivos manualmente.

## **API de Excel: Copiar Carpeta**

### API Web

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Seguridad y Autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### La API CopyFolder acepta los siguientes parámetros

| Nombre del Parámetro | Obligatorio | Tipo   | Ubicación (Ruta/Consulta) | Descripción                                                              |
| --------------------- | ----------- | ------ | ------------------------- | ------------------------------------------------------------------------ |
| `srcPath`             | Sí          | Cadena | Ruta                      | La ruta de la carpeta de origen que se va a copiar.                     |
| `destPath`            | Sí          | Cadena | Consulta                  | La ruta donde se creará la nueva carpeta.                               |
| `srcStorageName`      | No          | Cadena | Consulta                  | El nombre del almacenamiento que contiene la carpeta de origen.         |
| `destStorageName`     | No          | Cadena | Consulta                  | El nombre del almacenamiento de destino donde se debe copiar la carpeta. |

### Respuesta de Ejemplo

Una llamada correcta devuelve **HTTP 200** con un cuerpo JSON vacío:

```json
{}
```

**Solicitud cURL de ejemplo**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**Códigos de Estado HTTP**

| Código | Significado            | Descripción                                                     |
| ------ | ---------------------- | --------------------------------------------------------------- |
| 200    | Correcto               | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud Incorrecta   | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No Autorizado          | Token JWT inválido o ausente.                                   |
| 413    | Carga Excesiva         | El archivo subido supera el límite de tamaño permitido.        |
| 500    | Error Interno del Servidor | Error inesperado en el servidor.                              |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

Utilizar un SDK constituye la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}