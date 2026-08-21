---
title: "Aspose.Cells Cloud Web API: Convertir hoja de cálculo a PDF"
second_title: "Documento"
ArticleTitle: "Cómo convertir una hoja de cálculo local a PDF mediante la API de Aspose.Cells Cloud"
linktitle: "Convertir hoja de cálculo a PDF"
type: docs
url: /convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, hoja de cálculo a PDF, conversión de Excel, API en la nube, generación de PDF, API REST, v4.0"
description: "Guía paso a paso para convertir una hoja de cálculo local a PDF mediante la API de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, detalles de respuesta, manejo de errores y casos prácticos de uso."
weight: 100
---

El punto final **ConvertSpreadsheetToPdf** lee un archivo de hoja de cálculo cargado desde una unidad local, lo procesa en el servidor de Aspose.Cells Cloud y devuelve el documento PDF resultante como un flujo binario. Esta conversión nativa en la nube elimina la necesidad de cargar el archivo fuente al almacenamiento, reduce el consumo de recursos y simplifica los flujos de trabajo al entregar el PDF directamente al cliente. Los formatos admitidos dependen de las bibliotecas subyacentes; la API valida la existencia del archivo, los permisos y la integridad de la conversión, lanzando los códigos de error HTTP correspondientes para entradas no válidas o fallos en el procesamiento.

## **API para Convertir Hoja de Cálculo a PDF**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio/Opcional | Descripción                                                                                                                                                                                    |
| :------------------- | :----- | :-------- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData  | Obligatorio          | El archivo de hoja de cálculo fuente (XLS, XLSX, CSV, etc.) que se va a convertir. Debe ser un archivo válido y legible; el tamaño máximo es de 100 MB. Ejemplo: `myWorkbook.xlsx`.          |
| outPath              | String | Query     | Opcional             | Ruta de la carpeta de destino donde se guardará el PDF convertido en el servidor (si desea guardarlo). Si se omite, el archivo se devuelve directamente en la respuesta. Ejemplo: `/output/reports/`. |
| outStorageName       | String | Query     | Opcional             | Nombre del servicio de almacenamiento de destino (por ejemplo, `MyCloudStorage`). Solo es obligatorio cuando se usa `outPath` y el almacenamiento no es el predeterminado.                      |
| fontsLocation        | String | Query     | Opcional             | Ruta a una carpeta personalizada de fuentes en el servidor para garantizar una representación correcta del texto en el PDF. Ejemplo: `/fonts/custom/`.                                          |
| region               | String | Query     | Opcional             | Configuración regional/lingüística de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Query     | Opcional             | Contraseña necesaria para abrir una hoja de cálculo protegida. Omitir si el archivo no está cifrado.                                                                                           |

### **Respuesta**

Respuesta correcta (200 OK)  
Content-Type: application/pdf  
Content‑Disposition: attachment; filename="converted.pdf"  
Content‑Length: `<tamaño en bytes>`

Cuerpo: flujo binario del archivo PDF generado

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Aplicación de filtros correcta; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT no válido o ausente.                                    |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño.                          |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                        |

## ¿Dónde deberíamos utilizar la API para Convertir Hoja de Cálculo a PDF?

- **Tuberías automatizadas de generación de informes** – Convertir informes diarios de Excel generados automáticamente a PDF para su archivo o distribución por correo electrónico, sin intervención manual.
- **Sistemas de gestión de documentos** – Guardar directamente los PDF en un SGD tras la conversión, manteniendo la hoja de cálculo original solo en el lado del cliente.
- **Aplicaciones web con exportación bajo demanda** – Permitir a los usuarios finales descargar una versión PDF de la hoja de cálculo que editan en el navegador, aprovechando la conversión en la nube para preservar el diseño.
- **Cumplimiento normativo** – Generar instantáneas PDF inmutables de hojas de cálculo financieras para auditorías, garantizando que el archivo fuente nunca abandone el entorno del cliente.
- **Flujos de trabajo de conversión entre formatos** – Combinar con otros puntos finales de conversión, como la [API para Convertir Hoja de Cálculo a CSV](/convert-spreadsheet-to-csv/), para crear archivos multiformato.

## ¿Por qué debería utilizar la API para Convertir Hoja de Cálculo a PDF?

- **Flujo de trabajo sin carga previa al almacenamiento** – No es necesario cargar el archivo fuente al almacenamiento en la nube; la conversión ocurre directamente desde el flujo cargado, ahorrando ancho de banda y costos de almacenamiento.
- **Renderizado de alta fidelidad** – Aspose.Cells preserva fórmulas complejas, gráficos y formato al convertir a PDF, igualando la salida de Excel en escritorio.
- **Ejecución escalable en la nube** – Aprovecha la infraestructura en la nube de Aspose para una conversión rápida y fiable, independientemente del hardware del cliente.
- **Interfaz REST sencilla** – Una única solicitud `PUT` con parámetros de consulta opcionales; devuelve un flujo PDF listo para descargar, facilitando la integración en cualquier lenguaje.

## Cómo utilizar la API para Convertir Hoja de Cálculo a PDF con SDK

### Especificación de la API para Convertir Hoja de Cálculo a PDF

La [Especificación de la API para Convertir Hoja de Cálculo a PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) proporciona una interfaz de programación públicamente accesible para ejecutar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

Utilizar el SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiéndole fusionar una hoja de cálculo en otra mediante un código breve. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud. Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}