---
title: "Guardar hoja de cálculo en otro formato – API de Aspose.Cells Cloud (v4.0)"
second_title: "Documento"
ArticleTitle: "Cómo guardar una hoja de cálculo en otro formato en almacenamiento remoto: guía paso a paso"
linktitle: "Guardar hoja de cálculo como"
type: docs
url: /save-spreadsheet-as/
keywords: "Aspose Cells, conversión de hojas de cálculo, guardar como, API, XLSX a PDF, almacenamiento en la nube, Excel a PDF, exportación CSV, conversión en la nube"
description: "Aprenda a guardar una hoja de cálculo almacenada en Aspose Cloud en otro formato (XLSX, PDF, CSV, etc.) mediante la API de Aspose.Cells Cloud para guardar hojas de cálculo. Incluye sintaxis de solicitud, parámetros, ejemplo de curl y código del SDK."
weight: 100
---

Guarde una hoja de cálculo en la nube o un archivo de Excel en otro formato dentro del almacenamiento en la nube.

## **API para guardar hoja de cálculo como**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                           |
| :------------------- | :----- | :-------- | :---------------------------------------------------------------------------------------------------- |
| name                 | String | Path      | **Obligatorio.** El nombre del archivo del libro que se va a convertir.                              |
| format               | String | Query     | **Obligatorio.** El formato de salida deseado (por ejemplo, `Xlsx`, `PDF`, `CSV`).                  |
| saveOptionsData      | Class  | Body      | Datos opcionales de opciones de guardado. Si se omite, el valor predeterminado es `null`.            |
| folder               | String | Query     | Ruta de carpeta opcional donde se almacena el libro de origen. Si se omite, el valor predeterminado es `null`. |
| storageName          | String | Query     | Nombre opcional de un almacenamiento personalizado. Si se omite, se utiliza el almacenamiento predeterminado. |
| outPath              | String | Query     | Ruta de salida opcional para el archivo convertido. Si se omite, el valor predeterminado es `null`.  |
| outStorageName       | String | Query     | Nombre opcional del almacenamiento para el archivo de salida.                                        |
| fontsLocation        | String | Query     | Ubicación opcional de fuentes personalizadas.                                                        |
| region               | String | Query     | Configuración opcional de región de la hoja de cálculo.                                              |
| password             | String | Query     | Contraseña opcional para abrir el archivo de hoja de cálculo.                                        |

**Formatos de salida admitidos**

| Formato | Extensión                                        |
| :------ | :----------------------------------------------- |
| Xlsx    | .xlsx                                            |
| Pdf     | .pdf                                             |
| Csv     | .csv                                             |
| Html    | .html                                            |
| Ods     | .ods                                             |
| Xls     | .xls                                             |
| Txt     | .txt                                             |
| Mhtml   | .mhtml                                           |
| Tiff    | .tiff                                            |
| Pptx    | .pptx                                            |
| … (más) | Consulte la especificación de la API para obtener la lista completa (más de 20 formatos) |

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Ejemplo de respuesta de error (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Parámetros de solicitud no válidos."
}
```

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                                       |
| ------ | ------------------------ | ----------------------------------------------------------------- |
| 200    | OK                       | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request              | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized             | Token JWT no válido o ausente.                                    |
| 413    | Payload Too Large        | El archivo cargado supera el límite de tamaño.                   |
| 500    | Internal Server Error    | Error inesperado del servidor.                                    |

## ¿Dónde debería utilizar la API para guardar hoja de cálculo como?

### Sistema empresarial de gestión de documentos

- Guardar automáticamente informes financieros como archivos PDF.
- Realizar copias de seguridad periódicas de datos de ventas en formato CSV.
- Guardar planes de proyecto como archivos de solo lectura para evitar cambios accidentales.

### Procesos de integración de datos y ETL

- Exportar datos del sistema CRM y guardarlos como plantilla estándar de Excel.
- Convertir datos ERP a CSV para importarlos en otros sistemas.
- Guardar datos en bruto como JSON para su transmisión mediante API.

### Escenarios de desarrollo y automatización

- Procesamiento por el lado del servidor para aplicaciones web.
- Sistemas automatizados de generación de informes.
- Plataformas de colaboración en la nube.
- Integración con procesos de aprobación.
- Copias de seguridad y migración de datos.

## ¿Por qué debería utilizar la API para guardar hoja de cálculo como?

- **Amigable para desarrolladores**: Proporciona SDK para múltiples lenguajes con documentación detallada, facilitando la integración.
- **Eficiente en recursos humanos**: Realiza la conversión en el servidor, reduciendo la necesidad de escribir código personalizado para la conversión.
- **Precios basados en uso**: Solo cobra por las llamadas a la API realizadas, sin cargos previos por licencias.
- **Sin mantenimiento de servidor**: El servicio se ejecuta en la nube, eliminando la necesidad de gestionar infraestructura de conversión.
- **Amplia compatibilidad con formatos**: Admite la conversión entre más de 20 formatos de hojas de cálculo.
- **Fidelidad de los datos**: Preserva diseño, fórmulas y estilo durante la conversión.

## ¿Cómo utilizar la API para guardar hoja de cálculo como con SDK?

### Especificación de la API para guardar hoja de cálculo como

La [especificación de la API para guardar hoja de cálculo como](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) define una interfaz de programación accesible públicamente, lo que le permite realizar interacciones REST directamente desde un navegador web.

**Ejemplo con cuerpo de solicitud y curl**

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracte los detalles de bajo nivel y le permite guardar una hoja de cálculo en otro formato con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}