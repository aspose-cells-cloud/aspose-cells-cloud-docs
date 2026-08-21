---
title: "Convertir hoja de cálculo a CSV – Documentación de la API de Aspose.Cells Cloud"
second_title: "Documento"
articleTitle: "Cómo convertir una hoja de cálculo de una hoja de Excel a CSV usando la API de Aspose.Cells Cloud"
linktitle: "Convertir hoja de cálculo a CSV"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, conversión a CSV, hoja de cálculo a CSV, API REST, hoja de cálculo en la nube, Excel a CSV"
description: "Aprenda cómo convertir una hoja de cálculo específica de un archivo de Excel a CSV usando la API de Aspose.Cells Cloud (v4.0). Incluye endpoint, parámetros, ejemplo con cURL, código del SDK y manejo de errores."
weight: 100
---

El endpoint **ConvertWorksheetToCsv** transforma una única hoja de cálculo de un archivo local en un documento CSV directamente en los servidores de Aspose.Cells Cloud. Al cargar el archivo fuente y especificar la hoja objetivo, los desarrolladores reciben un flujo binario CSV sin necesidad de almacenar el archivo en el almacenamiento en la nube. Esta API es ideal para automatizar la extracción de datos, integrar datos de hojas de cálculo en sistemas posteriores y reducir la sobrecarga de almacenamiento.

## API para convertir hoja de cálculo a CSV

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio/Opcional | Descripción                                                                                                                                 |
| :------------------- | :----- | :-------- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet          | File   | FormData  | **Obligatorio**      | Archivo binario de la hoja de cálculo fuente (por ejemplo, `.xlsx`, `.xls`). Ejemplo: `myWorkbook.xlsx`.                                    |
| worksheet            | String | Query     | **Obligatorio**      | Nombre de la hoja de cálculo que se va a convertir (distingue mayúsculas/minúsculas). Si se omite, se utiliza la primera hoja. Ejemplo: `Sheet1`. |
| outPath              | String | Query     | Opcional             | Ruta de la carpeta de destino en el almacenamiento en la nube donde se guardará el CSV generado. Si se omite, el CSV se devuelve directamente en el flujo de respuesta. |
| outStorageName       | String | Query     | Opcional             | Nombre del servicio de almacenamiento (por ejemplo, Azure, AWS S3) donde se debe colocar el archivo de salida. Obligatorio solo si se usa `outPath`. |
| fontsLocation        | String | Query     | Opcional             | Ruta a una carpeta personalizada de fuentes en el servidor, lo que permite al motor de conversión usar fuentes no estándar.                 |
| region               | String | Query     | Opcional             | Identificador regional que influye en el formato de números y fechas en el CSV (por ejemplo, `es-ES`, `fr-FR`).                             |
| password             | String | Query     | Opcional             | Contraseña para abrir una hoja de cálculo protegida. Debe coincidir con la contraseña de cifrado del archivo fuente.                         |

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

| Código | Significado            | Descripción                                                         |
| ------ | ---------------------- | ------------------------------------------------------------------- |
| 200    | OK (Correcto)          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Petición incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado          | Token JWT inválido o faltante.                                      |
| 413    | Carga demasiado grande  | El archivo cargado supera el límite de tamaño.                     |
| 500    | Error interno del servidor | Error inesperado del servidor.                                      |

## ¿Cuándo usar la API para convertir hoja de cálculo a CSV?

- **Extracción de datos para pipelines de BI** – Extraer una hoja específica de un informe de Excel e integrar directamente el CSV resultante en Power BI o Tableau sin manipulación intermedia de archivos.
- **Procesamiento automatizado de facturas** – Convertir la hoja que contiene filas de facturas a CSV para una importación rápida en sistemas contables.
- **Integración con sistemas heredados** – Exportar datos de hojas de cálculo a CSV para su uso por aplicaciones más antiguas que solo aceptan archivos de texto delimitado.
- **Generación de informes sobre la marcha** – Generar instantáneas CSV de datos de hojas de cálculo en tiempo real desde un servicio web, devolviendo el archivo al navegador del cliente de inmediato.

## ¿Por qué usar la API para convertir hoja de cálculo a CSV?

- **No se requiere almacenamiento permanente en la nube** – El archivo se transmite directamente al motor de conversión y se descarta tras la conversión, ahorrando ancho de banda y costos de almacenamiento.
- **Ejecución en la nube de alto rendimiento** – La conversión se ejecuta en los servidores optimizados de Aspose, generalmente completándose en menos de 2 segundos para archivos de hasta 100 MB.
- **Control detallado** – Seleccione una única hoja, aplique fuentes personalizadas, formato regional y protección con contraseña en una sola solicitud.
- **Salida coherente multiplataforma** – Garantiza una salida CSV idéntica en .NET, Java, Python y otros SDK que usan el mismo endpoint REST.

## Cómo usar la API para convertir hoja de cálculo a CSV con SDK

### Especificación de la API para convertir hoja de cálculo a CSV

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">Especificación de la API para convertir hoja de cálculo a CSV</a> proporciona una interfaz de programación accesible públicamente para ejecutar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
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

### Uso de los SDK de Aspose.Cells Cloud

El uso del SDK simplifica el desarrollo al ocultar los detalles de bajo nivel, permitiéndole fusionar una hoja de cálculo en otra con código conciso. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells usando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}