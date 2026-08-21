---
title: "API Web de Divisor de Hojas de Cálculo en la Nube de Aspose.Cells: Dividir Libro de Excel en Varios Archivos en +30 Formatos"
second_title: "Documento"
ArticleTitle: "Dividir Archivo de Excel en la Nube para Separar Archivos y Exportar a +30 Formatos"
linktype: "Dividir Hoja de Cálculo Remota en la Nube"
type: docs
url: /split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, dividir libro de Excel, divisor de hojas de cálculo, API en la nube, exportar a PDF, exportar a CSV, exportar a JSON, exportación en múltiples formatos, procesamiento de hojas de cálculo en la nube"
description: "Utilice la API de Aspose.Cells Cloud para dividir un libro de Excel almacenado en el almacenamiento en la nube en hojas de cálculo separadas y exportar cada parte a más de 30 formatos, como PDF, CSV, JSON, XLSX, HTML, ODS y XPS."
weight: 100
---

Divida un libro de Excel grande almacenado en la nube en archivos independientes por hoja y exporte cada uno a más de 30 formatos de salida, como PDF, CSV, JSON, ODS y XPS, utilizando Aspose.Cells Cloud.

## **API para Dividir Hoja de Cálculo Remota**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Seguridad y Autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de Solicitud:**

| Nombre del Parámetro | Tipo   | Ruta / Cadena de Consulta / Cuerpo HTTP | Descripción                                                                                                                           |
| :------------------- | :----- | :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------ |
| name                 | Cadena | Ruta                                    | Nombre del archivo del libro (por ejemplo, `data.xlsx`) que se va a dividir, ubicado en la carpeta especificada del almacenamiento en la nube. |
| folder               | Cadena | Consulta                                | Ruta de la carpeta en el almacenamiento en la nube donde se almacena el libro de origen.                                             |
| from                 | Entero | Consulta                                | Índice inicial (basado en 0) de la hoja de cálculo para la operación de división. Por ejemplo, `0` indica la primera hoja de cálculo.  |
| to                   | Entero | Consulta                                | Índice final (basado en 0) de la hoja de cálculo para la operación de división. Por ejemplo, `2` divide las hojas 0, 1 y 2.            |
| outFormat            | Cadena | Consulta                                | Formato de archivo de salida para los archivos divididos. Los formatos compatibles incluyen `XLSX`, `PDF`, `CSV`, `JSON`, `HTML` y más de 30 más. |
| storageName          | Cadena | Consulta                                | _(Opcional)_ Nombre del almacenamiento en la nube donde reside el libro de origen. Si se omite, se utiliza el almacenamiento en la nube predeterminado. |
| outPath              | Cadena | Consulta                                | _(Opcional)_ Ruta de carpeta en el almacenamiento en la nube donde se guardarán los archivos divididos. Si se omite, los archivos se guardan en la carpeta de origen. |
| outStorageName       | Cadena | Consulta                                | Nombre del almacenamiento en la nube donde se guardarán los archivos divididos resultantes.                                          |
| fontsLocation        | Cadena | Consulta                                | _(Opcional)_ Especifica una ruta personalizada de carpeta en la nube que contiene archivos de fuentes para un renderizado adecuado de texto en salidas PDF o imágenes. |
| region               | Cadena | Consulta                                | _(Opcional)_ Establece la configuración regional para formatear números, fechas y monedas en los archivos de salida (por ejemplo, `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password             | Cadena | Consulta                                | _(Opcional)_ Si el libro de origen está protegido con contraseña, proporcione la contraseña para abrir el archivo.                    |

## **Respuesta**

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

El archivo se puede descargar directamente o guardarse en la ubicación especificada por `outPath`.

**Detalles de respuesta exitosa**

| Código de Estado | Content‑Type               | Descripción                               |
| ---------------- | -------------------------- | ----------------------------------------- |
| 200 OK           | `application/octet-stream` | Flujo binario del archivo del libro unificado. |

**Códigos de estado HTTP**

| Código | Significado               | Descripción                                                     |
| ------ | ------------------------- | --------------------------------------------------------------- |
| 200    | OK                        | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud Incorrecta      | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No Autorizado             | Token JWT inválido o faltante.                                  |
| 413    | Carga de Datos Demasiado Grande | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error Interno del Servidor | Error inesperado del servidor.                                  |

## ¿Dónde debemos utilizar la API para Dividir Hoja de Cálculo Remota?

- **Distribución de Datos por Departamento**: Dividir un libro unificado que contiene datos de varios departamentos en archivos específicos por departamento.
- **Distribución de Informes Regionales**: Dividir informes de ventas nacionales en archivos independientes por región.
- **Distribución con Ocultación de Datos de Clientes**: Dividir un libro que contiene información confidencial en un archivo dedicado para visualización por clientes.
- **División de Informes Periódicos**: Dividir automáticamente informes resumen en informes semanales o diarios mensualmente.
- **Distribución en Múltiples Formatos**: Dividir un solo archivo de Excel en múltiples versiones de formatos, como PDF, CSV, JSON, etc., simultáneamente.
- **División Basada en Plantillas**: Dividir archivos de datos en archivos de salida estandarizados según plantillas predefinidas.
- **Preprocesamiento de Origen de Datos**: Dividir el archivo de Excel en un archivo CSV estandarizado antes de cargar los datos en la base de datos.
- **Preparación de Datos para API**: Dividir grandes conjuntos de datos en fragmentos más pequeños adecuados para transferencia mediante API.
- **Distribución de Datos en Microservicios**: Dividir el archivo de datos central en archivos de datos independientes requeridos por cada microservicio.

## ¿Por qué debería utilizar la API para Dividir Hoja de Cálculo Remota?

- **Amigable para Desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido, y cuenta con una documentación completa. En comparación con la construcción de soluciones personalizadas para renderizado de gráficos, esto reduce significativamente la carga de trabajo de desarrollo.
- **Reducción de Costos de Mano de Obra**: Disminuye la necesidad de cargos dedicados a la consolidación de documentos.
- **Pago por Uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Cero Costos de Mantenimiento**: No es necesario mantener servidores, actualizar software ni lidiar con problemas de compatibilidad.
- **Preserva el formato complejo de Excel** en un formato PDF universalmente accesible.

## Cómo Utilizar la API para Dividir Hoja de Cálculo Remota con SDKs

### Especificación de la API para Dividir Hoja de Cálculo Remota

La [Especificación de la API para Dividir Hoja de Cálculo Remota](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) define una interfaz de programación públicamente accesible y permite interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
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

### Utilizar SDKs de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole dividir la hoja de cálculo almacenada en la nube en archivos independientes con código breve.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDKs de Aspose.Cells Cloud.  
Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}