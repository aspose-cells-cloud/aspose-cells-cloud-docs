---
title: "Aspose.Cells Cloud Web API: Convertir hoja de cálculo a HTML"
second_title: "Documentación"
ArticleTitle: "Cómo convertir una hoja de cálculo a HTML mediante la API de Aspose.Cells Cloud"
linktype: "Convertir hoja de cálculo a HTML"
type: docs
url: /convert-worksheet-to-html/
description: "Aprenda a convertir una hoja de cálculo de Excel a HTML utilizando la API de Aspose.Cells Cloud: sin necesidad de cargar, fuentes personalizadas, compatibilidad con regiones y manejo de errores."
keywords: "Aspose.Cells, Excel a HTML, conversión de hojas de cálculo, API en la nube"
weight: 100
---

El endpoint **ConvertWorksheetToHtml** lee un libro de Excel desde el sistema de archivos local, extrae la hoja especificada y devuelve el contenido como un archivo HTML. La conversión se ejecuta completamente en los servidores en la nube de Aspose, por lo que no es necesario realizar ninguna carga intermedia ni almacenamiento previo. Ideal para generar vistas listas para la web de los datos de hojas de cálculo, la API admite rutas de salida opcionales, fuentes personalizadas, configuraciones regionales y libros protegidos con contraseña.

## API para convertir hoja de cálculo a HTML

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio / Opcional | Descripción                                                                                                                                                                                                 |
| :------------------- | :----- | :-------- | :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | File   | Obligatorio | FormData               | Archivo binario de Excel que se va a procesar. Debe ser un archivo .xlsx, .xls, .xlsb, etc. válido. Ejemplo: `myWorkbook.xlsx`. El archivo Excel se lee directamente desde el cuerpo de la solicitud; no es necesario cargarlo previamente al almacenamiento en la nube. |
| worksheet            | String | Obligatorio | Query                  | Nombre de la hoja de cálculo que se va a convertir (sensible a mayúsculas). Debe existir en el libro proporcionado. Ejemplo: `Sheet1`.                                                                       |
| outPath              | String | Opcional    | Query                  | Ruta de la carpeta de destino (en el almacenamiento en la nube) donde se guardará el archivo HTML generado. Si se omite, el archivo se devuelve directamente en la respuesta. Ejemplo: `/output/html/`.          |
| outStorageName       | String | Opcional    | Query                  | Nombre del servicio de almacenamiento en la nube que se utilizará para `outPath`. Solo es necesario cuando `outPath` apunta a un almacenamiento no predeterminado.                                           |
| fontsLocation        | String | Opcional    | Query                  | Ruta absoluta a una carpeta que contiene fuentes TrueType/OpenType personalizadas que deben usarse durante la conversión. Permite una representación correcta de caracteres no estándar.                             |
| region               | String | Opcional    | Query                  | Identificador regional que influye en el formato de números y fechas (por ejemplo, `es-ES`, `fr-FR`). Por defecto, utiliza la configuración regional interna del libro.                                        |
| password             | String | Opcional    | Query                  | Contraseña necesaria para abrir un libro protegido. Omítala para archivos no protegidos.                                                                                                                     |

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

| Código | Significado             | Descripción                                                     |
| ------ | ----------------------- | --------------------------------------------------------------- |
| 200    | OK (Correcto)           | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido).   |
| 401    | No autorizado           | Token JWT inválido o ausente.                                   |
| 413    | Carga demasiado grande   | El archivo subido supera el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## ¿Dónde debemos utilizar la API para convertir hoja de cálculo a HTML?

- **Incorporar datos de hojas de cálculo en vivo en un portal web**: convierta una hoja de cálculo de informe financiero a HTML para su visualización directa en navegadores, sin necesidad de complementos de Excel.
- **Generar facturas HTML imprimibles desde una plantilla de Excel**: automatice la creación de páginas de facturas listas para la web a partir de una hoja de cálculo predefinida.
- **Crear fragmentos de documentación**: convierta hojas de especificaciones de diseño en fragmentos HTML que se puedan insertar en manuales técnicos o wikis.
- **Desarrollar paneles de control BI con bajo código**: extraiga datos de hojas de cálculo, conviértalos a HTML y muestrelos dentro de widgets personalizados de paneles de control.

## ¿Por qué debería utilizar la API para convertir hoja de cálculo a HTML?

- **Flujo de trabajo sin carga previa**: convierta archivos locales directamente en la nube, eliminando la necesidad de transferir grandes libros al almacenamiento previamente.
- **Renderizado de alto rendimiento**: la conversión del lado del servidor aprovecha el motor optimizado de Aspose, proporcionando una salida HTML rápida y precisa.
- **Control total sobre la salida**: los parámetros opcionales (fuentes personalizadas, región, contraseña) permiten adaptar el HTML a los requisitos regionales y de marca.
- **Integración sencilla**: una solicitud PUT simple con `multipart/form-data` se integra naturalmente en pipelines CI/CD, microservicios o funciones sin servidor.

## Cómo utilizar la API para convertir hoja de cálculo a HTML con SDK

### Especificación de la API para convertir hoja de cálculo a HTML

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">Especificación de la API para convertir hoja de cálculo a HTML</a> proporciona una interfaz de programación públicamente accesible para ejecutar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificado en Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nombre de archivo opcional"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar los SDK es la forma más rápida de desarrollar, ya que abstraen los detalles de bajo nivel, lo que le permite combinar hojas de cálculo con código conciso.  
Consulte el <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">repositorio GitHub de los SDK de Aspose.Cells Cloud</a> para obtener una lista completa de los SDK disponibles.  
Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}