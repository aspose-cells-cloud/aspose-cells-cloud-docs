---
title: "API web de compresión de Excel de Aspose.Cells Cloud: reduzca el tamaño de archivo de hoja de cálculo programáticamente"
second_title: "Documento"
ArticleTitle: "Cómo comprimir archivos de Excel: reducir tamaño de hoja de cálculo y optimizar rendimiento"
linktitle: "Comprimir hoja de cálculo"
type: docs
url: /es/compress-spreadsheet/
keywords: "compresión de Excel, Aspose.Cells Cloud, reducción de tamaño de hoja de cálculo, API, optimización de libro de trabajo"
description: "Aprenda a comprimir libros de Excel con la API de Aspose.Cells Cloud. Obtenga ejemplos paso a paso, parámetros, autenticación y mejores prácticas."
weight: 100
---

Comprima programáticamente hojas de cálculo de Excel y reduzca el tamaño del archivo con la API de Aspose.Cells Cloud. Optimice el rendimiento del libro de trabajo eliminando datos no utilizados, comprimiendo objetos incrustados y limpiando el formato. Esta API REST permite flujos de trabajo automatizados de compresión y optimización de archivos de Excel.

## **API para comprimir hojas de cálculo**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ruta/Consulta/Cadena/Cuerpo HTTP | Descripción                                                                                                                           |
| --------------------- | ------- | -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet           | Archivo | FormData                         | **Obligatorio.** Archivo de libro de Excel de origen (`.xlsx`, `.xls`, etc.) que se va a comprimir.                                   |
| level                 | Entero  | Consulta                         | **Opcional.** Intensidad de compresión (0 = más rápido/mínima, 9 = más lento/máxima). Si se omite, se aplica un valor predeterminado equilibrado (5). |
| outPath               | Cadena  | Consulta                         | **Opcional.** Ruta de carpeta de destino en su almacenamiento en la nube. Si se omite, el archivo se guarda en la misma carpeta que el libro de origen. |
| outStorageName        | Cadena  | Consulta                         | **Obligatorio.** Identificador del servicio de almacenamiento en la nube configurado (por ejemplo, `CorporateDrive`).                |
| region                | Cadena  | Consulta                         | **Opcional.** Configuración regional (por ejemplo, `de-DE`) que podría afectar el manejo de datos específicos por región.            |
| password              | Cadena  | Consulta                         | **Opcional.** Contraseña para descifrar una hoja de cálculo protegida. Déjelo en blanco si el archivo no está cifrado.                |

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
| 200    | Correcto              | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta  | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado         | Token JWT no válido o faltante.                                   |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                  |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## ¿Dónde debemos utilizar la API para comprimir hojas de cálculo?

- **Distribución automatizada de informes** – Comprima los estados financieros mensuales antes de enviarlos por correo electrónico para garantizar la entrega exitosa y mejorar la experiencia del destinatario.
- **Optimización de carga de archivos de usuario** – Comprima los archivos de Excel cargados en segundo plano para ahorrar espacio en almacenamiento en la nube y reducir los costos de almacenamiento.
- **Procesamiento y migración en canalizaciones de datos** – Comprima los archivos intermedios de Excel generados durante los procesos ETL para acelerar la transferencia por red y reducir la presión sobre el almacenamiento temporal.

## ¿Por qué debería utilizar la API para comprimir hojas de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido con documentación completa.
- **Reducción de costos laborales** – Elimina la necesidad de personal dedicado para consolidar documentos manualmente.
- **Precios por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente realice.
- **Sin mantenimiento de servidores requerido** – No hay servidores que mantener, sin actualizaciones de software ni preocupaciones por compatibilidad.

## Cómo utilizar la API para comprimir hojas de cálculo con SDK

### Especificación de la API para comprimir hojas de cálculo

La [Especificación de la API para comprimir hojas de cálculo](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) proporciona una interfaz accesible públicamente para interacciones REST, lo que permite llamadas directas a la API desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel y le permite comprimir una hoja de cálculo con solo unas pocas líneas de código. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}