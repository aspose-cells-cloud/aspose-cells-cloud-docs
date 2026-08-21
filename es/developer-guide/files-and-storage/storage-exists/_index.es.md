---
title: "Verificar si existe un almacenamiento – API de Aspose.Cells Cloud (v4.0)"
second_title: "Documento"
ArticleTitle: "Gestión de archivos de Excel basada en la nube – Verificar existencia de almacenamiento"
linktitle: "¿Existe el almacenamiento?"
type: docs
url: /es/storage-exists/
keywords: "Aspose.Cells, existe almacenamiento, API de almacenamiento en la nube, REST, Excel"
description: "Verifique la existencia de un contenedor de almacenamiento en Aspose.Cells Cloud. Aprenda sobre el punto de conexión GET /v4.0/cells/storage/{storageName}/exist, los parámetros requeridos, el formato de respuesta y vea ejemplos de SDK en C#, Java, Python y más."
weight: 100
---

La API `storageExists` verifica si un almacenamiento especificado existe en el servicio en la nube de Aspose.Cells. Esta funcionalidad es fundamental para garantizar que todas las operaciones que dependen del almacenamiento puedan ejecutarse sin errores.
**Resumen**: El punto de conexión `storageExists` le permite confirmar si un contenedor de almacenamiento específico está disponible en Aspose.Cells Cloud. Utilícelo antes de realizar operaciones relacionadas con archivos para evitar errores en tiempo de ejecución.

## Verificar la existencia de almacenamiento (storageExists)

### API Web

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                     |
| --------------------- | ------ | --------- | ----------------------------------------------- |
| storageName           | String | Path      | El nombre del almacenamiento que se va a verificar. |

### **Respuesta**

```json
{
  "Name": "StorageExist",
  "Description": ["Indica si el almacenamiento especificado existe."],
  "Type": "Clase",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indica si el almacenamiento existe.",
        "Esta propiedad devuelve true si el almacenamiento está presente; de lo contrario, devuelve false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o faltante.                                    |
| 413    | Carga demasiado grande   | El archivo subido excede el límite de tamaño.                     |
| 500    | Error interno del servidor | Error inesperado del servidor.                                    |

## ¿Cómo utilizar la API de verificación de existencia de almacenamiento con SDK?

### Especificación OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente, lo que permite a los desarrolladores interactuar directamente con la API REST desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es el enfoque más eficiente para acelerar el desarrollo. Un SDK abstracta los detalles de implementación de bajo nivel, permitiendo a los desarrolladores centrarse en las tareas de su proyecto. Para obtener una lista completa de los SDK disponibles de Aspose.Cells Cloud, visite el <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">repositorio de GitHub</a>.

Los siguientes ejemplos de código muestran cómo realizar llamadas a las API de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}
---