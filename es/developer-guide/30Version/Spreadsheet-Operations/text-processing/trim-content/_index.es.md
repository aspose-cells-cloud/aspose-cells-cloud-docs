---
title: "Aspose.Cells Trim Content API: Eliminar espacios y saltos de línea de Excel"
second_title: "Documento"
linktype: "Trim Content"
type: docs
url: /spreadsheet-trim-content/
keywords: "Aspose.Cells, API Trim Content, limpieza de datos en Excel, eliminar espacios en Excel, eliminación de saltos de línea, limpieza de datos en hojas de cálculo"
description: "Utilice la API PostTrimContent de Aspose.Cells Cloud para limpiar automáticamente espacios adicionales, saltos de línea y caracteres no deseados de celdas de Excel. Aprenda sobre el punto de conexión, el formato de la solicitud, el código de ejemplo y el manejo de errores."
weight: 100
---

## **API web de Excel: PostTrimContent**

La API **PostTrimContent** procesa y recorta el contenido dentro de un rango especificado en una hoja de cálculo. Elimina espacios adicionales, saltos de línea y otros caracteres innecesarios del contenido de las celdas seleccionadas, lo que la hace útil para limpiar entradas de datos y garantizar un formato coherente en las hojas de cálculo.

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.


### **Descripción de la función**

- **Eficiencia**: Recorta el contenido únicamente dentro del rango designado, ahorrando tiempo y recursos al evitar operaciones innecesarias en toda la hoja de cálculo.
- **Flexibilidad**: Permite a los usuarios definir el rango exacto de celdas que se procesará, adaptándose a diversos conjuntos de datos y requisitos.
- **Integridad de los datos**: Elimina espacios y saltos de línea adicionales, ayudando a mantener datos coherentes y confiables para su análisis e informes.
- **Facilidad de uso**: Integración sencilla con una configuración mínima, adecuada tanto para desarrolladores como para usuarios finales.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo  | Ubicación | Descripción                                                                                     |
| --------------------- | ----- | --------- | ----------------------------------------------------------------------------------------------- |
| trimContentOptions    | Clase | Cuerpo    | Opciones que especifican cómo debe recortarse el contenido (por ejemplo, rango objetivo, modo de recorte). |

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nombre de archivo fusionado]",
    "Filesize" : [tamaño del archivo],
    "FileContent" : "[Cadena en Base64]"
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente. |
| 413    | Payload demasiado grande     | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo utilizar la API PostRemoveCharacters con SDK

### Especificación de la API PostRemoveCharacters

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_Ultima actualización: 2026-03-30_