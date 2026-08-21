---
title: "Aspose.Cells Cloud Web API: Convertir hoja de cálculo a JSON"
second_title: "Documento"
ArticleTitle: "Cómo convertir una hoja de cálculo local a JSON utilizando la API de Aspose.Cells Cloud"
linktitle: "Convertir hoja de cálculo a JSON"
type: docs
url: /es/convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, convertir hoja de cálculo a JSON, API Excel a JSON, API de Aspose.Cells Cloud, API REST, conversión de hojas de cálculo"
description: "Aprenda a convertir archivos Excel locales a JSON mediante la API de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, código de ejemplo y manejo de errores para una integración fluida."
weight: 100
---

El punto de conexión **ConvertSpreadsheetToJson** convierte una hoja de cálculo almacenada en una unidad local en un archivo JSON completamente en el servidor de Aspose.Cells Cloud. Al enviar la hoja de cálculo como `multipart/form-data`, el servicio devuelve un flujo JSON listo para descargar o procesar posteriormente. Esta conversión nativa en la nube elimina la necesidad de cargar primero el archivo al almacenamiento, reduce los costos de almacenamiento y simplifica el flujo de trabajo para aplicaciones que requieren datos de hojas de cálculo en formato JSON para análisis, generación de informes o intercambio de datos.

**Requisitos previos**: Debe tener una cuenta de Aspose Cloud, un token de acceso JWT válido y el SDK o la clave API de Aspose.Cells Cloud configurados.

**Contexto**: Convertir hojas de cálculo a JSON es un paso habitual al integrar datos de Excel con servicios web, bases de datos NoSQL o aplicaciones JavaScript del lado del cliente. La API Convert Spreadsheet to JSON ofrece una conversión rápida del lado del servidor sin necesidad de almacenar el archivo original.

## API para convertir hoja de cálculo a JSON

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo                       | Ubicación | Obligatorio/Opcional | Descripción                                                                                                                                                                     |
| :------------------- | :------------------------- | :-------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet          | File (multipart/form-data) | FormData  | Obligatorio         | Archivo de hoja de cálculo de origen (por ejemplo, .xls, .xlsx, .xlsm). Ejemplo: `curl -F "Spreadsheet=@myfile.xlsx"`                                                           |
| outPath              | String                     | Query     | Opcional            | Ruta de carpeta de destino en el almacenamiento en la nube donde se guardará el archivo JSON convertido. Si se omite, el JSON se devuelve directamente en el flujo de respuesta. Ejemplo: `outPath=/output/`. |
| outStorageName       | String                     | Query     | Opcional            | Nombre del almacenamiento en la nube (por ejemplo, Amazon S3, Azure Blob) donde se debe escribir el archivo de salida. Obligatorio únicamente cuando se usa `outPath` con un almacenamiento no predeterminado. |
| fontsLocation        | String                     | Query     | Opcional            | Ruta a una carpeta personalizada de fuentes en el servidor. Úsela cuando la hoja de cálculo haga referencia a fuentes no disponibles en la biblioteca predeterminada.                                      |
| region               | String                     | Query     | Opcional            | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato de números, fechas y monedas durante la conversión.                                               |
| password             | String                     | Query     | Opcional            | Contraseña para abrir una hoja de cálculo protegida con contraseña. Omítala para archivos no protegidos.                                                                                                  |

### Respuesta

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Códigos de estado HTTP**

| Código | Significado           | Descripción                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK (Correcto)         | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta  | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado         | Token JWT no válido o ausente.                                     |
| 413    | Carga demasiado grande | El archivo subido supera el límite de tamaño.                                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                          |

## ¿Dónde debe utilizarse la API para convertir hoja de cálculo a JSON?

- **Flujos de trabajo de migración de datos** – Convertir informes Excel heredados a JSON para ingerirlos en bases de datos NoSQL modernas o lagos de datos.
- **Aplicaciones móviles o web** – Transformar rápidamente hojas de cálculo subidas por usuarios a JSON para representarlas del lado del cliente sin almacenar el archivo original en la nube.
- **Generación automatizada de informes** – Generar cargas útiles JSON para servicios de análisis descendentes (por ejemplo, Power BI, Tableau) directamente desde entradas de hojas de cálculo.
- **Funciones sin servidor** – Utilizar la API dentro de AWS Lambda o Azure Functions para realizar conversiones sobre la marcha sin gestionar almacenamiento temporal.

## ¿Por qué debería utilizar la API para convertir hoja de cálculo a JSON?

- Conversión nativa en la nube que elimina la necesidad de cargar archivos grandes al almacenamiento antes del procesamiento, reduciendo la latencia y los costos de almacenamiento.
- Flujo de trabajo de una sola solicitud: suba la hoja de cálculo y reciba JSON en la misma llamada HTTP, simplificando la lógica de integración.
- Admite hojas de cálculo protegidas con contraseña y con configuraciones regionales específicas, garantizando una representación precisa de los datos en distintas localizaciones.
- Escalable en la infraestructura de Aspose: maneja libros grandes y fórmulas complejas sin afectar los recursos de su propio servidor.

## Cómo utilizar la API para convertir hoja de cálculo a JSON con SDK

### Especificación de la API para convertir hoja de cálculo a JSON

La [Especificación de la API para convertir hoja de cálculo a JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) proporciona una interfaz de programación accesible públicamente para ejecutar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel y le permite convertir una hoja de cálculo a JSON con unas pocas líneas de código.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.  
Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}