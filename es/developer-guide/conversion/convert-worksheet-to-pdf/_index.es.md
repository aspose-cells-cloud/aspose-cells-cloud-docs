---
title: "Aspose.Cells Cloud Web API: Convertir una hoja de cálculo local de Excel en un archivo PDF – Herramienta gratuita en línea"
second_title: "Documento"
ArticleTitle: "Cómo convertir una hoja de cálculo local en un archivo PDF: Guía paso a paso"
linktitle: "Convertir hoja en PDF"
type: docs
url: /es/convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel a PDF, conversión de hoja, API REST, conversión en la nube, PDF de hoja de cálculo, punto de conexión de API, generación de PDF"
description: "Utilice la API de Aspose.Cells Cloud para convertir rápidamente y de forma segura una hoja de un archivo local de Excel en un documento PDF."
weight: 100
---

Exporte una hoja de cálculo desde un archivo local de Excel a un archivo [PDF](https://docs.fileformat.com/pdf/) utilizando la API en la nube.

## **API para convertir hoja en PDF**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en tokens JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                 |
| --------------------- | ------ | ----------------------------------- | --------------------------------------------------------------------------- |
| Spreadsheet           | File   | FormData                            | Cargue el archivo de hoja de cálculo.                                       |
| worksheet             | String | Query                               | Nombre de la hoja de cálculo dentro del archivo.                            |
| outPath               | String | Query                               | (Opcional) Ruta de la carpeta donde se almacenará el libro; el valor por defecto es null. |
| outStorageName        | String | Query                               | Nombre del almacenamiento para el archivo de salida.                        |
| fontsLocation         | String | Query                               | Utilice fuentes personalizadas para el PDF.                                 |
| region                | String | Query                               | Defina la configuración regional de la hoja de cálculo.                     |
| password              | String | Query                               | Contraseña necesaria para abrir el archivo de hoja de cálculo.              |

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                           |
| ------ | ----------------------- | --------------------------------------------------------------------- |
| 200    | Correcto                | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT no válido o faltante.                                       |
| 413    | Payload demasiado grande | El archivo cargado supera el límite de tamaño.                      |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                     |

## **¿Dónde debería utilizar la API para convertir hoja en PDF?**

- **Estados financieros**: convierta balances, estados de resultados (tablas específicas) a PDF para documentación lista para auditoría.
- **Informes de ventas**: transforme paneles de control de ventas o cálculos de comisiones en PDF listos para distribuir.
- **Métricas operativas**: exporte tablas de KPI y métricas de desempeño como informes PDF formales.
- **Datos contractuales**: exporte tablas de precios y acuerdos de nivel de servicio desde hojas de cálculo a PDF como archivos adjuntos.
- **Registros de auditoría**: preserve hojas de cálculo financieras como evidencia PDF no editable.
- **Resúmenes de cartera**: exporte tablas de desempeño de inversiones como estados de cuenta PDF listos para clientes.
- **Informes de control de calidad**: exporte hojas de inspección a PDF para registros de cumplimiento.
- **Resúmenes de inventario**: transforme hojas de existencias en PDF para revisión por parte de la gerencia.

## **¿Por qué debería utilizar la API para convertir hoja en PDF?**

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene con documentación completa. Comparado con la construcción de soluciones personalizadas para renderizar gráficos, esto reduce significativamente la carga de trabajo de desarrollo.
- **Rentable**: puede convertir datos de tablas sin tener que cargar previamente el libro, lo que ahorra espacio de almacenamiento y reduce costos.
- **Preservación del formato**: conserva el formato complejo de Excel en un formato PDF universalmente accesible.

## **¿Cómo utilizar la API para convertir hoja en PDF con SDK?**

### Especificación de la API para convertir hoja en PDF

La [Especificación de la API para convertir hoja en PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) proporciona una interfaz de programación públicamente accesible y permite interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiéndole convertir datos de tablas de hojas de cálculo en un archivo PDF con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}