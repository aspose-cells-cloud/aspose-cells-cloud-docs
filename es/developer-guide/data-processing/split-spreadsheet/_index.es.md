---
title: "Aspose.Cells Cloud Split Excel Web API: Dividir Excel localmente en varios archivos y exportar a más de 30 formatos"
second_title: "Documento"
ArticleTitle: "Herramienta de división de Excel: Dividir hoja de cálculo local en archivos en más de 30 formatos"
linktitle: "Dividir hoja de cálculo"
type: docs
url: /es/split-spreadsheet/
keywords: "dividir, excel, aspose cells, API de hoja de cálculo, exportar PDF, CSV, JSON"
description: "Divida un libro de Excel localmente en archivos separados utilizando la API de Aspose.Cells Cloud. Exporte a más de 30 formatos (PDF, CSV, JSON, XLSX, HTML) sin necesidad de cargarlos en la nube."
weight: 100
---

Divida un libro de Excel local en archivos independientes por completo, sin necesidad de almacenamiento en la nube. El resultado admite más de 30 formatos de archivo, como PDF, CSV, JSON, ODS y XPS.

## **API para dividir hojas de cálculo**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo    | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                                                                                                               |
| :------------------- | :------ | :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet          | File    | FormData                            | Archivo de hoja de cálculo local que se va a dividir. Los formatos admitidos incluyen XLSX, XLS, ODS, CSV, etc. El archivo se procesa completamente en el servidor, sin necesidad de almacenamiento en la nube. |
| from                 | Integer | Query                               | Índice inicial (basado en cero) del rango de hojas que se va a dividir (por ejemplo, `0` para la primera hoja).                                                        |
| to                   | Integer | Query                               | Índice final (basado en cero) del rango de hojas que se va a dividir (por ejemplo, `2` dividirá las hojas 0, 1 y 2).                                                     |
| outFormat            | String  | Query                               | Formato de salida para los archivos divididos. Admite más de 30 formatos, como `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`.                                                   |
| outPath              | String  | Query                               | _(Opcional)_ Ruta de carpeta local donde se guardarán los archivos generados tras la división. Si se omite, los archivos se guardarán en una ubicación temporal predeterminada. |
| outStorageName       | String  | Query                               | Identificador de almacenamiento para organizar los archivos de salida. En modo de procesamiento local, normalmente hace referencia a una etiqueta de almacenamiento basada en sesión o definida por el usuario. |
| fontsLocation        | String  | Query                               | _(Opcional)_ Especifica un directorio local o personalizado de fuentes para garantizar una representación precisa del texto al exportar a formatos PDF o imagen.         |
| region               | String  | Query                               | _(Opcional)_ Establece la configuración regional para el formato de números, fechas y monedas en los archivos de salida (por ejemplo, `"en-US"`, `"de-DE"`).           |
| password             | String  | Query                               | _(Opcional)_ Si la hoja de cálculo cargada está protegida con contraseña, proporcione la contraseña para abrir y procesar el archivo.                                   |

## **Respuesta**

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

El archivo se puede descargar directamente o guardarse en la ubicación especificada por `outPath`.

**Detalles de respuesta correcta**

| Código de estado | Content-Type               | Descripción                                |
| ---------------- | -------------------------- | ------------------------------------------ |
| 200 OK           | `application/octet-stream` | Flujo binario del archivo del libro unificado. |

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                        |
| ------ | ----------------------- | ------------------------------------------------------------------ |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Bad Request             | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | Unauthorized            | Token JWT inválido o ausente.                                      |
| 413    | Payload Too Large       | El archivo cargado excede el límite de tamaño.                    |
| 500    | Internal Server Error   | Error inesperado del servidor.                                     |

## ¿Dónde debemos utilizar la API para dividir hojas de cálculo?

- **Distribución de datos por departamentos**: Dividir un libro unificado que contenga datos de varios departamentos en archivos específicos por departamento.
- **Distribución de informes regionales**: Dividir estados de ventas nacionales en archivos de informes regionales independientes.
- **Distribución con enmascaramiento de datos de clientes**: Dividir un libro que contenga información confidencial en un archivo con una vista reducida de los datos del cliente.
- **División periódica de informes**: Dividir automáticamente informes resumen en informes semanales o diarios mensuales.
- **Distribución en múltiples formatos**: Dividir un único archivo de Excel en varias versiones en distintos formatos, como PDF, CSV, JSON, etc., simultáneamente.
- **División basada en plantillas**: Dividir archivos de datos en archivos de salida estandarizados según plantillas predefinidas.
- **Preprocesamiento de fuente de datos**: Dividir el archivo de Excel en un archivo CSV estandarizado antes de cargar los datos en una base de datos.
- **Preparación de datos para API**: Dividir conjuntos de datos grandes en fragmentos más pequeños adecuados para transferencia mediante API.

## ¿Por qué debería utilizar la API para dividir hojas de cálculo?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y proporciona una documentación exhaustiva. Comparado con la creación de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Reducción de costos laborales**: Reduce la necesidad de posiciones dedicadas a la consolidación de documentos.
- **Pago por uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Costos cero de mantenimiento**: No es necesario mantener servidores, actualizar software ni lidiar con problemas de compatibilidad.
- **Preserva el formato complejo de Excel** en formato PDF accesible universalmente.

## Cómo utilizar la API para dividir hojas de cálculo con SDK

### Especificación de la API para dividir hojas de cálculo

La [especificación de la API para dividir hojas de cálculo](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) proporciona una interfaz de programación públicamente accesible para realizar interacciones REST directamente desde un navegador web.
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

Utilizar los SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole dividir la hoja de cálculo en archivos independientes con un código reducido.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo invocar los servicios web de Aspose.Cells mediante distintos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}