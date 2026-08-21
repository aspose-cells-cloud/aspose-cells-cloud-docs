---
title: "Aspose.Cells – API de actualización de mayúsculas y minúsculas de palabras"
second_title: "Documentación"
linktype: "en"
type: docs
url: /post-update-word-case/
keywords: "Aspose.Cells, API de actualización de mayúsculas y minúsculas de palabras, conversión de mayúsculas y minúsculas de texto, Excel, CSV, Google Sheets, API REST"
description: "Convierta el formato de mayúsculas y minúsculas del texto en archivos de Excel, CSV o Google Sheets con la API de actualización de mayúsculas y minúsculas de palabras de Aspose.Cells Cloud. Admite conversión a mayúsculas/minúsculas, formato de título y capitalización de la primera letra."
weight: 100
ArticleTitle: "Aspose.Cells – Documentación de la API de actualización de mayúsculas y minúsculas de palabras"
---

**Versión de la API:** 3.0

Gestionar el formato inconsistente de mayúsculas y minúsculas en hojas de cálculo (Excel, Google Sheets, CSV) puede resultar frustrante, especialmente con grandes conjuntos de datos. La **API web PostUpdateWordCase** automatiza las conversiones de formato de mayúsculas y minúsculas del texto, garantizando datos limpios y estandarizados con un esfuerzo mínimo.

## **API web de Excel – API de actualización de mayúsculas y minúsculas de palabras**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en tokens JWT</a>.

### **Descripción de la función**

La API web PostUpdateWordCase aborda el problema común del formato inconsistente de mayúsculas y minúsculas en hojas de cálculo, lo cual puede afectar significativamente el análisis y procesamiento de datos. Esta API automatiza la conversión de mayúsculas y minúsculas, garantizando que sus datos estén limpios, estandarizados y listos para su manipulación o análisis posteriores.

- **Conversión automatizada de mayúsculas y minúsculas**
  - **Mayúsculas a minúsculas** – Convierte todas las letras mayúsculas en minúsculas.
  - **Minúsculas a mayúsculas** – Convierte todas las letras minúsculas en mayúsculas.
  - **Capitalizar primera letra** – Capitaliza la primera letra de cada palabra.
  - **Formato de título** – Convierte el texto a formato de título, donde la primera letra de cada palabra principal se capitaliza.

- **Compatibilidad con múltiples formatos** – La API funciona con una amplia variedad de formatos de hojas de cálculo, incluyendo Excel, OpenOffice, JSON, CSV y otros. Esta versatilidad la hace adecuada para diversas necesidades de procesamiento de datos.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo   | Ubicación      | Descripción                                                                                                               |
| --------------------- | ------ | -------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions`    | objeto | Cuerpo de la solicitud | Opciones que definen la transformación de mayúsculas y minúsculas deseada, como el rango de origen, el tipo de destino y configuraciones adicionales. |

**Esquema de `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // Rango en estilo Excel a procesar (obligatorio)
  "CaseType": "Upper", // Enumeración: Upper, Lower, Capitalize, Title (obligatorio)
  "IgnoreBlank": true // Booleano, opcional – si es true, las celdas en blanco se dejan sin cambios
}
```

**Ejemplo de cuerpo de solicitud**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – El rango de celdas al que se aplicará la conversión de mayúsculas y minúsculas (por ejemplo, `A1:C5`).
- **CaseType** – El tipo de conversión de mayúsculas y minúsculas. Los valores permitidos son `Upper`, `Lower`, `Capitalize` y `Title`.
- **IgnoreBlank** – Si es `true`, se ignoran las celdas en blanco; el valor predeterminado es `false`.

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nombre de archivo fusionado]",
    "Filesize" : [tamaño del archivo],
    "FileContent" : "[CadenaBase64]"
}
```

- **Filename** – Nombre del archivo procesado.
- **FileSize** – Tamaño del archivo en bytes.
- **FileContent** – Contenido del archivo transformado codificado en base64.

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Payload demasiado grande     | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado del servidor. |

## Cómo usar la API PostUpdateWordCase con SDK

### Especificación de la API PostUpdateWordCase

La <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---