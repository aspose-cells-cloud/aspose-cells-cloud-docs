---
title: "Aspose.Cells Cloud Web API: Convertir hoja de cálculo a CSV"
second_title: "Documentación"
ArticleTitle: "Cómo convertir una hoja de cálculo a CSV mediante la API de Aspose.Cells Cloud"
linktitle: "Convertir hoja de cálculo a CSV"
type: docs
url: /convert-spreadsheet-to-csv/
keywords: "Aspose Cells, conversión CSV, API de Excel, conversión en la nube"
description: "Aprenda a convertir archivos de Excel (XLS, XLSX, XLSM, etc.) a CSV mediante la API de Aspose.Cells Cloud. Incluye pasos de autenticación, ejemplo con cURL, fragmentos de código de SDK y manejo de errores."
weight: 100
---

El endpoint **ConvertSpreadsheetToCsv** recibe un archivo de hoja de cálculo cargado desde una unidad local, procesa la conversión íntegramente en los servidores de Aspose.Cells Cloud y devuelve el archivo CSV resultante como un flujo binario. Esta operación nativa en la nube elimina la necesidad de subir el archivo original al almacenamiento en la nube, reduce los costos de almacenamiento y simplifica el flujo de trabajo para desarrolladores que requieren conversiones rápidas de hojas de cálculo a CSV. Los formatos admitidos dependen de las bibliotecas subyacentes y se requieren permisos adecuados para leer el archivo original. Los errores, como archivos faltantes, solicitudes inválidas o fallos en la conversión, se devuelven con códigos de estado HTTP estándar.

## **API para convertir hoja de cálculo a CSV**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio | Descripción                                                                                                                                                      |
| :------------------- | :----- | :-------- | :---------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData  | Obligatorio | El archivo de hoja de cálculo que se va a convertir. Acepta formatos comunes como .xls, .xlsx, .xlsm. Debe proporcionarse como multipart/form‑data. Ejemplo: `myWorkbook.xlsx`. |
| outPath              | String | Query     | Opcional    | Ruta de la carpeta de destino donde se guardará el CSV convertido. Si se omite, el CSV se devuelve directamente en el cuerpo de la respuesta. Ejemplo: `/output/reports/`.     |
| outStorageName       | String | Query     | Opcional    | Nombre del servicio de almacenamiento en la nube donde se guardará el archivo de salida. Si no se especifica, se utiliza el almacenamiento predeterminado configurado para la cuenta de Aspose.Cells. |
| fontsLocation        | String | Query     | Opcional    | Ruta a una carpeta que contiene fuentes personalizadas necesarias para la hoja de cálculo. Permite representar correctamente celdas que utilizan fuentes no estándar.      |
| region               | String | Query     | Opcional    | Configuración de región/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Influye en el formato numérico, el análisis de fechas y el comportamiento específico de la configuración regional. |
| password             | String | Query     | Opcional    | Contraseña utilizada para abrir hojas de cálculo protegidas con contraseña. Si el archivo está cifrado y se omite o es incorrecta la contraseña, se devuelve un error 400/401. |

### **Respuesta**

En caso de éxito, la API devuelve **HTTP 200** (o **202** para procesamiento asíncrono) con el encabezado `Content-Type: application/octet-stream`. El cuerpo de la respuesta contiene el archivo CSV generado como un flujo binario.

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

| Código | Significado           | Descripción                                                   |
| ------ | --------------------- | ------------------------------------------------------------- |
| 200    | OK                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request           | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized          | Token JWT inválido o faltante.                                |
| 413    | Payload Too Large     | El archivo subido supera el límite de tamaño.                 |
| 500    | Internal Server Error | Error inesperado en el servidor.                              |

## ¿Dónde debería utilizarse la API para convertir hoja de cálculo a CSV?

- **Exportación de datos para sistemas de informes** – Genere extracciones CSV a partir de informes basados en Excel para alimentar herramientas de BI o almacenes de datos, sin necesidad de manipular archivos manualmente.
- **Procesamiento por lotes automatizado** – Convierta grandes cantidades de hojas de cálculo almacenadas localmente a CSV en trabajos del lado del servidor, y envíe directamente los resultados a servicios posteriores.
- **Aplicaciones web con cargas de archivos** – Permita que los usuarios finales suban un archivo de Excel y reciban instantáneamente una versión CSV para su análisis posterior o importación en otras plataformas.
- **Integración con sistemas heredados** – Traduzca formatos heredados de hojas de cálculo a CSV para sistemas que solo aceptan archivos de texto delimitado plano.

## ¿Por qué usar la API para convertir hoja de cálculo a CSV?

- **Arquitectura sin necesidad de cargar al almacenamiento en la nube** – No es necesario almacenar el archivo original en el almacenamiento en la nube; la conversión ocurre directamente desde el flujo cargado, ahorrando tiempo y costos de almacenamiento.
- **Procesamiento en la nube de alto rendimiento** – Aprovecha el motor de conversión optimizado de Aspose.Cells en servidores escalables en la nube, ofreciendo salidas CSV rápidas incluso para libros grandes.
- **Integración sencilla** – Una única solicitud PUT con parámetros de consulta opcionales; devuelve el CSV como un flujo binario listo para descargar, eliminando pasos posteriores de procesamiento.
- **Soporte completo de características** – Maneja archivos protegidos con contraseña, fuentes personalizadas y configuraciones específicas de la región, garantizando conversiones precisas para hojas de cálculo complejas.

## Cómo usar la API para convertir hoja de cálculo a CSV con SDK

### Especificación de la API para convertir hoja de cálculo a CSV

La [Especificación de la API para convertir hoja de cálculo a CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv) proporciona una interfaz de programación accesible públicamente para realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

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

Utilizar los SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole trabajar con hojas de cálculo mediante código conciso. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud. Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}