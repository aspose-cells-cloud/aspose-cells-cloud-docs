---
title: "Aplicar formato de texto enriquecido a una celda"
type: docs
url: /es/apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, texto enriquecido, formato de celda, API REST, Aspose.Cells Cloud"
description: "Aprenda cómo aplicar formato de texto enriquecido a una celda específica de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, detalles de parámetros, ejemplo con cURL y fragmentos de SDK."
ArticleTitle: "Aplicar formato de texto enriquecido a una celda mediante la API de Aspose.Cells Cloud"
---

Esta API REST aplica **formato de texto enriquecido** a una celda en un archivo de Excel.

**Requisitos previos:** Debe poseer un token JWT válido y el archivo de Excel de destino ya debe existir en la carpeta especificada del almacenamiento antes de invocar esta operación.

**Antecedentes:** El formato de texto enriquecido le permite aplicar múltiples estilos de fuente dentro de una sola celda, lo que permite una presentación más expresiva de los datos en hojas de cálculo de Excel.

## API PostCellCharacters

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación                     | Descripción                                                                 |
|----------------------|--------|-------------------------------|-----------------------------------------------------------------------------|
| name                 | string | path                          | Nombre del archivo de Excel (por ejemplo, `Book1.xlsx`).                   |
| sheetName            | string | path                          | Hoja de cálculo que contiene la celda de destino.                           |
| cellName             | string | path                          | Dirección de la celda a formatear (por ejemplo, `A1`).                      |
| options              | object | body                          | Objeto JSON que define la configuración del formato de texto enriquecido para la celda. |
| folder               | string | query                         | Carpeta en el almacenamiento donde se encuentra el archivo de Excel.       |
| storageName          | string | query                         | Nombre del servicio de almacenamiento (si se utiliza un almacenamiento personalizado). |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Carga demasiado grande       | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostCellCharacters con SDK

### Especificación de la API PostCellCharacters

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

### Uso de los SDK de Aspose.Cells Cloud

Usar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*Ejemplo con SDK de C\#*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Ejemplo con SDK de Java*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*Ejemplo con SDK de PHP*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Ejemplo con SDK de Ruby*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Ejemplo con SDK de Node.js*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Ejemplo con SDK de Python*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Ejemplo con SDK de Perl*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Ejemplo con SDK de Go*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}
---