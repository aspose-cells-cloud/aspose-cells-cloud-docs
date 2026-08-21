---
title: "Aspose.Cells Cloud Web API para eliminar hojas de cálculo de Excel: eliminar hojas de libros de trabajo mediante programación"
second_title: "Documento"
ArticleTitle: "Cómo eliminar hojas de cálculo de Excel: eliminar hojas de libros de trabajo"
linktitle: "Eliminar hoja de cálculo de hoja de cálculo"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, API para eliminar hoja de cálculo, eliminación de hojas de Excel, hoja de cálculo en la nube, API REST"
description: "Aprenda cómo eliminar una hoja de cálculo de un archivo de Excel utilizando la API de Aspose.Cells Cloud. Incluye el endpoint, los parámetros, ejemplos de cURL y SDK."
weight: 100
---

Elimine hojas de cálculo de libros de Excel mediante programación con la API de Aspose.Cells Cloud. Elimine con seguridad una o varias hojas, limpie la estructura del libro de trabajo y automatice la optimización de hojas de cálculo. API REST para flujos de trabajo empresariales de gestión y procesamiento de documentos de Excel.

## API para eliminar hoja de cálculo de hoja de cálculo

### API Web

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud:

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                                                                             |
| :------------------- | :----- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet          | Archivo | FormData  | **Obligatorio.** El archivo de libro de Excel de origen (.xlsx, .xls, etc.) del cual se eliminará una hoja de cálculo.                                                                                   |
| sheetName            | Cadena  | Query     | **Obligatorio.** El nombre exacto de la hoja de cálculo que se va a eliminar (por ejemplo, `Hoja1`, `DatosTemporales`).                                                                                 |
| outPath              | Cadena  | Query     | **Opcional.** La ruta de la carpeta de destino en el almacenamiento en la nube donde se guardará el libro modificado. Si se omite o es `null`, el libro se guardará en la misma ubicación que el archivo de origen o en una ruta predeterminada. |
| outStorageName       | Cadena  | Query     | **Opcional.** El identificador del servicio de almacenamiento en la nube (por ejemplo, `ProjectStorage`) donde se escribirá el archivo de salida. Si no se proporciona, se utilizará el almacenamiento predeterminado. |
| region               | Cadena  | Query     | **Opcional.** La configuración regional (por ejemplo, `es-ES`) que podría afectar fórmulas o datos específicos de la región durante la operación de guardado.                                           |
| password             | Cadena  | Query     | **Opcional.** La contraseña necesaria para abrir y modificar una hoja de cálculo protegida con contraseña. Omítala si el archivo no está encriptado.                                                      |

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
| 200    | OK                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta  | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado         | Token JWT no válido o faltante.                                   |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                 |

## ¿Dónde debemos utilizar la API para eliminar hoja de cálculo de hoja de cálculo?

- **Posprocesamiento automatizado de informes** – Tras generar un informe financiero final, elimine automáticamente las hojas intermedias utilizadas para cálculos temporales, manteniendo el archivo final limpio y profesional.
- **Limpieza dinámica de archivos de plantilla** – Cuando los usuarios generen documentos personalizados (por ejemplo, presupuestos) a partir de una plantilla, elimine las páginas opcionales que no hayan sido seleccionadas.
- **Optimización del archivado de flujos de trabajo** – Tras completar un proyecto o auditoría, elimine las hojas de borrador o colaboración, conservando únicamente la versión final para su archivo y cumplimiento normativo.

## ¿Por qué debería utilizar la API para eliminar hoja de cálculo de hoja de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y proporciona documentación exhaustiva.
- **Reducción de costos de mano de obra** – Elimina la necesidad de personal dedicado para consolidar documentos manualmente.
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.
- **Costos cero de mantenimiento** – Sin servidores que mantener, sin actualizaciones de software y sin preocupaciones por compatibilidad.

## Cómo utilizar la API para eliminar hoja de cálculo de hoja de cálculo con SDK

### Especificación de la API para eliminar hoja de cálculo de hoja de cálculo

La <a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">Especificación de la API para eliminar hoja de cálculo de hoja de cálculo</a> define una interfaz de programación accesible públicamente, lo que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Hoja1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/ruta/al/archivo_de_entrada.xlsx"
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel y le permite eliminar una hoja de cálculo con un código mínimo. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}