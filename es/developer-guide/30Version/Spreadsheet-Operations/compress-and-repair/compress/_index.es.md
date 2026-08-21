---
title: "Comprimir datos en un archivo de Excel"
ArticleTitle: "Comprimir datos en un archivo de Excel – Aspose.Cells Cloud API"
second_title: "Documentos"
linktitle: "Comprimir archivos de Excel"
type: docs
url: /es/compress-excel-files/
aliases: [  /es/compress/ ]
keywords: "comprimir archivo de Excel, Aspose.Cells Cloud, compresión de Excel, compresión de hojas de cálculo, API REST, compresión de archivos"
description: "Comprima archivos de Excel (XLS, XLSX, XLSM, XLSB, ODS) utilizando la API REST de Aspose.Cells Cloud. Configure el nivel de compresión, maneje múltiples archivos e intégrelo mediante SDK."
weight: 39
---

## API PostCompress de los servicios web de Aspose.Cells Cloud

**Requisitos previos:**  
- Se requiere un token JWT válido para la autenticación.  
- Los formatos de archivo compatibles son XLS, XLSX, XLSM, XLSB y ODS.  
- El tamaño máximo permitido por archivo es de 500 MB por solicitud (sujeto a los límites del servicio).

Esta API REST comprime los datos de un archivo de Excel.

- Comprime XLS, XLSX, XLSM, XLSB, ODS
- Comprime rápidamente múltiples archivos de hojas de cálculo de Excel
- Permite elegir el nivel de compresión
- Admite múltiples archivos

### Punto de conexión de la API web

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                          |
|----------------------|---------|-----------------------------------------|------------------------------------------------------|
| file                 | archivo | formData                                | Archivo para cargar                                  |
| CompressLevel        | entero  | query                                   | Nivel de compresión (0‑100); valores más altos indican una compresión más intensa |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo | Descripción                                         |
| ---------------------| ---- | --------------------------------------------------- |
| data                 | archivo | Contenido binario del archivo de libro que se va a comprimir. |

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nombre de archivo combinado]",
    "Filesize" : [tamaño del archivo],
    "FileContent" : "[Base64String]"
}
```

*Nota:* `FileContent` contiene el libro comprimido codificado como una cadena en Base64. La longitud de la cadena corresponde al tamaño del archivo comprimido; puede decodificarla utilizando utilidades estándar de Base64 para recuperar el archivo binario de Excel.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                           |
|--------|-----------------------------|-------------------------------------------------------|
| 200    | Correcto                    | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostCompress con SDK

### Especificación de la API PostCompress

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
# Utilice HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <token jwt>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, lo que le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}