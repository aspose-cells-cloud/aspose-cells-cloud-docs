---
title: "Fusionar múltiples archivos de Excel en un solo libro"
second_title: "Documentos"
linktype: "Fusionar múltiples archivos de Excel"
type: docs
url: /es/merge-multi-files-into-excel/
aliases: [  /es/merge/multi-files/ ]
keywords: "Aspose.Cells Cloud, fusionar múltiples archivos de Excel, API REST, fusión de hojas de cálculo, SDK en la nube"
description: "Aprenda a fusionar varios libros de Excel en un solo archivo utilizando la API REST de Aspose.Cells Cloud (v3.0). Incluye el endpoint HTTPS, el comando cURL, ejemplos de SDK, parámetros requeridos y detalles sobre el manejo de errores."
weight: 32
---

## API REST

Esta API REST fusiona múltiples archivos de Excel en un único libro de Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación   | Descripción                                                                                      | Obligatorio |
|----------------------|---------|-------------|--------------------------------------------------------------------------------------------------|-------------|
| files[]              | archivo | formData    | Uno o más libros de Excel que se fusionarán. Utilice `file1`, `file2`, … en la solicitud.       | Sí          |
| format               | cadena  | query       | Formato de salida deseado (por ejemplo, `xlsx`).                                                 | Sí          |
| mergeToOneSheet      | booleano| query       | Establezca en `true` para combinar todas las hojas de cálculo en una sola hoja; el valor predeterminado es `false`. | No          |

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nombre del archivo fusionado]",
    "Filesize" : [tamaño del archivo],
    "FileContent" : "[CadenaBase64]"
}
```

**Códigos de estado HTTP**

| Código | Significado                  | Descripción                                               |
|--------|------------------------------|-----------------------------------------------------------|
| 200    | Correcto                     | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta         | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                | Token JWT inválido o faltante.                            |
| 413    | Carga demasiado grande        | El archivo cargado excede el límite de tamaño.            |
| 500    | Error interno del servidor   | Error inesperado en el servidor.                          |

## Cómo utilizar la API PostMerge con SDK

### Especificación de la API PostMerge

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <token jwt>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----CadenaBase64--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---