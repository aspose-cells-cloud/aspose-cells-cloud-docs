---
title: "API de Descarga de Archivos de Aspose.Cells Cloud – Interfaz para Descarga Rápida de Archivos en la Nube"
second_title: "Documentación"
linktitle: "API de Descarga de Archivos"
type: docs
url: /download-file/
keywords: "Aspose.Cells, API de Descarga de Archivos, almacenamiento en la nube de Excel, API REST, descarga de archivos, PDF, CSV, SDK"
description: "Descargue archivos de Excel, PDF, CSV y otros formatos desde el almacenamiento en la nube de Aspose.Cells Cloud mediante la API de Descarga de Archivos (v4.0). Incluye punto de conexión, parámetros, detalles de autenticación y ejemplos de código."
weight: 100
---

La **API DownloadFile** le permite recuperar archivos almacenados en el almacenamiento en la nube de Aspose.Cells Cloud. Esta API de descarga de archivos es esencial para acceder directamente desde la nube a hojas de cálculo de Excel, PDF, CSV y otros formatos admitidos.

## **API de Excel: Descargar archivo**

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud de la API **DownloadFile**

| Nombre del parámetro | Tipo   | Ubicación (Ruta / Consulta) | Descripción                                                     |
| --------------------- | ------ | --------------------------- | --------------------------------------------------------------- |
| path                  | String | Ruta                        | La ruta virtual al archivo que desea descargar.                |
| storageName           | String | Consulta                    | El nombre del almacenamiento desde el cual se recuperará el archivo. |
| versionId             | String | Consulta                    | El identificador de versión del archivo a descargar, si corresponde. |

### **Respuesta**

La API devuelve un **flujo binario de archivo**. La cabecera `Content-Type` coincide con el formato del archivo (por ejemplo, `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` para XLSX). No se devuelve ninguna carga útil JSON.

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                     |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer SU_TOKEN_DE_ACCESO" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}