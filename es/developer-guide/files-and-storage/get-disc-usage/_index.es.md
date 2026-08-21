---
title: "Aspose.Cells Cloud API: Obtener uso de disco | Métricas de almacenamiento en tiempo real"
second_title: "Documentación"
ArticleTitle: "Solución de gestión de archivos de Excel basada en la nube: Interfaz para recuperar rápidamente el uso de disco en la nube."
linktitle: "Obtener uso de disco"
type: docs
url: /es/get-disk-usage/
keywords: "Aspose Cells, API en la nube, uso de disco, métricas de almacenamiento, Excel, REST"
description: "Obtenga el uso de disco en tiempo real para Aspose.Cells Cloud. Aprenda sobre el endpoint GET /v4.0/cells/storage/disk, la autenticación requerida y una respuesta de ejemplo."
weight: 100
---

La operación **Obtener uso de disco** devuelve métricas de almacenamiento en tiempo real para su cuenta de Aspose.Cells Cloud. Utilice este endpoint para monitorear el espacio de disco consumido y el total disponible.

- Recupera el uso actual del disco para la API de Excel en el entorno de Aspose Cloud.
- Permite a los desarrolladores monitorear cuánto almacenamiento han consumido sus aplicaciones.
- Habilita una gestión proactiva de los límites de almacenamiento y del control de costos.

## API de Excel: GetDiskUsage

### API web

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                   | Obligatorio |
| -------------------- | ------ | --------- | ------------------------------------------------------------- | ----------- |
| storageName          | String | Query     | El nombre del almacén para el cual se desea obtener el uso. | Opcional    |

### **Respuesta**

```json
{
  "Name": "DiskUsage",
  "Description": ["Clase para la información del espacio en disco."],
  "Type": "Clase",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["Cantidad de espacio en disco utilizado por la aplicación."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["Espacio total en disco disponible."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**Códigos de estado HTTP**

| Código | Significado           | Descripción                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta  | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado         | Token JWT inválido o faltante.                                    |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                 |

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer SU_TOKEN_DE_ACCESO"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}

---