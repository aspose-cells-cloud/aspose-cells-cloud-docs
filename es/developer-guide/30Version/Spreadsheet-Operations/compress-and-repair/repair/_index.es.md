---
title: "Reparar archivos de Excel"
second_title: "Documentos"
type: docs
linktitle: "Reparar archivos de Excel"
url: /repair-excel-files/
keywords: "Aspose Cells, API de reparación de Excel, XLSX corrupto, recuperación de hojas de cálculo, API en la nube"
description: "Utilice la API REST de Aspose.Cells Cloud para reparar archivos de Excel corruptos (XLS, XLSX, XLSM, XLSB, ODS). Suba uno o varios archivos, elija el formato de salida y reciba los archivos reparados en Base64. No se requiere instalación."
weight: 39
---

Esta API REST le permite **reparar** archivos de Excel.

- Repara formatos de hojas de cálculo como XLS, XLSX, XLSM, XLSB, ODS y otros.  
- Admite la carga de varios archivos en una sola solicitud.

Aspose.Cells Cloud Excel Repair recupera datos de archivos de Excel corruptos en línea sin necesidad de instalar nada. Los archivos de Excel corruptos suponen un problema porque no se pueden abrir. Puede probar la aplicación Aspose.Cells Cloud Excel Repair para recuperar datos de tales archivos.

## API REST

El punto final **Reparar archivos de Excel** repara archivos de hojas de cálculo corruptos y devuelve el contenido reparado.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación                     | Descripción |
|----------------------|--------|-------------------------------|-------------|
| file                 | file   | formData (multipart)          | Archivo para subir |
| format               | string | query                         | Formato de salida deseado. Si se omite (null), el formato de salida será el mismo que el del archivo de entrada. |

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nombre de archivo combinado]",
    "Filesize" : [tamaño del archivo],
    "FileContent" : "[CadenaBase64]"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Carga demasiado grande       | El archivo subido supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostRepair con SDK

### Especificación de la API PostRepair

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----CadenaBase64--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----CadenaBase64--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

En caso de éxito, el servicio devuelve HTTP 200 con una carga útil JSON que contiene un array `Files`. En situaciones de error, la API utiliza códigos de estado HTTP estándar:

- **400 Solicitud incorrecta** – Parámetros no válidos o archivo no recuperable.  
- **401 No autorizado** – Token JWT ausente o no válido.  
- **413 Carga demasiado grande** – El archivo subido supera el tamaño permitido.  
- **500 Error interno del servidor** – Fallo inesperado del lado del servidor.

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}