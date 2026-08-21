---
title: "Aspose.Cells Cloud Web API: Convertir datos de tabla local de Excel a un archivo PDF - Herramienta gratuita en línea"
second_title: "Documentos"
ArticleTitle: "Cómo convertir datos de tabla de hoja de cálculo local a un archivo PDF: Guía paso a paso"
linktitle: "Convertir tabla a PDF"
type: docs
url: /es/convert-table-to-pdf/
keywords: "Aspose.Cells, Excel a PDF, conversión de tablas, API en la nube"
description: "Convierta rápidamente una tabla local de Excel a un archivo PDF mediante la API REST de Aspose.Cells Cloud."
weight: 100
---

Exporte datos de tabla desde un archivo local de Excel a un archivo PDF mediante la API en la nube.

## **API para convertir tabla a PDF**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta/cadena de consulta/cuerpo HTTP | Descripción                                                                 |
| :------------------- | :----- | :---------------------------------- | :-------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData                            | Suba el archivo de hoja de cálculo que se va a convertir.                  |
| worksheet            | String | Query                               | Nombre de la hoja de cálculo.                                              |
| tableName            | String | Query                               | Nombre de la tabla que se va a convertir.                                  |
| outPath              | String | Query                               | (Opcional) Ruta de carpeta donde se guardará el PDF convertido. Por defecto es null. |
| outStorageName       | String | Query                               | Especifique el nombre del almacenamiento de salida.                        |
| fontsLocation        | String | Query                               | Utilice fuentes personalizadas para el PDF.                                |
| region               | String | Query                               | Especifica la configuración regional para la hoja de cálculo.              |
| password             | String | Query                               | Contraseña para acceder al archivo de hoja de cálculo.                     |

### **Respuesta**

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

**Encabezados de respuesta de ejemplo**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**Códigos de estado HTTP**

| Código | Significado            | Descripción                                                  |
| ------ | ---------------------- | ------------------------------------------------------------ |
| 200    | OK (Correcto)          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request (Solicitud incorrecta) | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized (No autorizado) | Token JWT inválido o faltante.                               |
| 413    | Payload Too Large (Carga útil demasiado grande) | El archivo subido supera el límite de tamaño.              |
| 500    | Internal Server Error (Error interno del servidor) | Error inesperado del servidor.                               |

## **¿Dónde debería utilizar la API para convertir tabla a PDF?**

- ** Estados financieros**: convierta balance generales, estados de resultados (tablas específicas) a PDF para documentación lista para auditoría.
- ** Informes de ventas**: transforme paneles de control de ventas o cálculos de comisiones en PDF listos para distribuir.
- ** Métricas operativas**: exporte tablas de KPI y métricas de desempeño como informes formales en PDF.
- ** Datos contractuales**: exporte tablas de precios y acuerdos de nivel de servicio desde hojas de cálculo a PDF como archivos adjuntos.
- ** Registros de auditoría**: conserve tablas de datos financieros como pruebas PDF no editables.
- ** Resúmenes de cartera**: exporte tablas de desempeño de inversiones como estados de cuenta listos para clientes en PDF.
- ** Informes de control de calidad**: exporte tablas de datos de inspección a PDF para registros de cumplimiento.
- ** Resúmenes de inventario**: transforme tablas de niveles de existencia a PDF para revisión por parte de la gerencia.

## ¿Por qué debería utilizar la API para convertir tabla a PDF?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido, y viene con documentación completa. En comparación con la creación de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de trabajo de desarrollo.
- **Rentable**: puede convertir datos de tabla sin cargar previamente el libro, lo que ahorra espacio de almacenamiento y reduce costos.
- **Preserva el formato complejo de Excel** en un formato PDF universalmente accesible.

## ¿Cómo utilizar la API para convertir tabla a PDF con SDK?

### Especificación de la API para convertir tabla a PDF

La [Especificación de la API para convertir tabla a PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) proporciona una interfaz de programación accesible públicamente para realizar interacciones REST directamente desde un navegador web.
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole convertir datos de tabla de hoja de cálculo a un archivo PDF con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}