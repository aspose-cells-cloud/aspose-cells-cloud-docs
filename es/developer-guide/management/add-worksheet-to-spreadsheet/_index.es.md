---
title: "Aspose.Cells Cloud Excel Add Worksheet Web API - Insertar nuevas hojas con control de tipo y posición"
second_title: "Documento"
ArticleTitle: "Cómo agregar hojas de cálculo a Excel: Insertar nuevas hojas en ubicaciones específicas"
linktitle: "Agregar hoja de cálculo a hoja de cálculo"
type: docs
url: /es/add-worksheet-to-spreadsheet/
keywords: "excel, agregar hoja de cálculo, aspose cells api, hoja de cálculo, api en la nube, tipo de hoja, posición de hoja"
description: "Aprenda cómo agregar programáticamente una nueva hoja de cálculo, hoja de gráficos o hoja de macros a un libro de Excel usando la API de Aspose.Cells Cloud. Controla el tipo de hoja, nombre y posición de inserción en una única llamada REST."
weight: 100
---

Agregue programáticamente hojas de cálculo a archivos de Excel con control total sobre el tipo y la ubicación de la hoja. Inserte hojas de cálculo estándar, hojas de gráficos o hojas de macros en cualquier posición del libro. Esta operación RESTful permite la gestión y organización automatizadas de libros de Excel.

**Requisitos previos**

- Una cuenta activa de Aspose.Cells Cloud con un token de acceso JWT válido.
- Un nombre de almacenamiento en la nube configurado (por ejemplo, `CompanyOneDrive`) donde se guardará el libro.
- El libro de destino debe ser accesible en el almacenamiento especificado y, si está protegido, se debe proporcionar la contraseña correcta.

| **Tipo de hoja**         | Descripción                                        |
| :----------------------- | :------------------------------------------------- |
| **VB**                   | Módulo de Visual Basic                             |
| **Worksheet**            | Hoja de cálculo regular                            |
| **Chart**                | Hoja de gráficos                                   |
| **BIFF4Macro**           | Hoja de macros BIFF4                               |
| **InternationalMacro**   | Hoja de macros internacional                      |
| **Other**                | Tipo de hoja personalizada o menos común no listada arriba |
| **Dialog**               | Hoja de cálculo de diálogo                         |

## **API Agregar hoja de cálculo a hoja de cálculo**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                                                                                                                                 |
| :------------------- | :------ | :-------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**      | File    | FormData  | **Obligatorio.** El libro de Excel (.xlsx, .xls, etc.) al que se agregará una nueva hoja de cálculo.                                                                                                         |
| **sheetType**        | String  | Query     | **Opcional.** El tipo de hoja a crear. Los valores aceptables son `worksheet` (predeterminado), `chartsheet`, `macrosheet`, `vbmodule` y `dialog`.                                                          |
| **position**         | Integer | Query     | **Opcional.** Índice basado en cero donde se insertará la nueva hoja. `0` inserta antes de la primera hoja; `2` inserta como la tercera hoja. Omita para agregar la hoja al final.                            |
| **sheetName**        | String  | Query     | **Opcional.** Nombre para la nueva hoja de cálculo. Debe ser único dentro del libro. Si se omite, se genera un nombre predeterminado como “SheetX”.                                                            |
| **outPath**          | String  | Query     | **Opcional.** Directorio de destino en el almacenamiento en la nube donde se guardará el libro modificado. Si es `null` o se omite, el libro se guarda en la misma ubicación que el archivo de origen o en una ruta predeterminada. |
| **outStorageName**   | String  | Query     | **Obligatorio.** Identificador del almacenamiento en la nube configurado (por ejemplo, `CompanyOneDrive`) donde se debe escribir el archivo de salida.                                                          |
| **region**           | String  | Query     | **Opcional.** Configuración regional (por ejemplo, `es-ES`) que puede afectar el formato y las reglas regionales en la nueva hoja de cálculo.                                                               |
| **password**         | String  | Query     | **Opcional.** Contraseña para descifrar y modificar un libro protegido con contraseña. Omítala si el archivo no está cifrado.                                                                               |

### Respuesta

En caso de éxito, la API devuelve **HTTP 200 OK** (o **201 Created** cuando se genera un nuevo archivo) con el libro de trabajo actualizado.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                    |
| ------ | ----------------------- | -------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o faltante.                                 |
| 413    | Payload demasiado grande | El archivo cargado excede el límite de tamaño.               |
| 500    | Error interno del servidor | Error inesperado del servidor.                                |

## ¿Dónde debemos usar la API Agregar hoja de cálculo a hoja de cálculo?

- **Generación automatizada de informes** – Crear e insertar dinámicamente hojas mensuales (por ejemplo, `2024‑05`) durante la generación de estados financieros.
- **Inicialización por lotes de plantillas** – Agregar una hoja de análisis dedicada para cada nuevo cliente o proyecto al generar cotizaciones o propuestas de ventas a gran escala.
- **Expansión dinámica de paneles de control** – Insertar nuevas hojas de gráficos en tiempo real a medida que surgen nuevas dimensiones de datos.
- **Cumplimiento y archivado de auditoría** – Agregar automáticamente hojas de recopilación de evidencia durante auditorías anuales, manteniendo cada punto de inspección aislado.
- Para eliminar una hoja, consulte la operación **[Eliminar hoja de cálculo](/delete-worksheet/)**.
- Para mover una hoja, consulte la operación **[Mover hoja de cálculo](/move-worksheet/)**.

## ¿Por qué debería usar la API Agregar hoja de cálculo a hoja de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud proporciona SDK para múltiples lenguajes, reduciendo el esfuerzo de desarrollo y ofreciendo una documentación exhaustiva.
- **Reducción de costos laborales** – Elimina la necesidad de crear hojas de cálculo manualmente y realizar tareas repetitivas de copiar y pegar.
- **Pago por uso** – Solo paga por las llamadas a la API que realmente realice.
- **Sin mantenimiento** – Sin servidores que administrar, sin actualizaciones de software y sin preocupaciones por la compatibilidad.

## Cómo usar la API Agregar hoja de cálculo a hoja de cálculo con SDKs

### Especificación de la API Agregar hoja de cálculo a hoja de cálculo

La [Especificación de la API Agregar hoja de cálculo a hoja de cálculo](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/path/to/Book1.xlsx"
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

### Uso de SDKs de Aspose.Cells Cloud

El uso de un SDK abstracte los detalles de bajo nivel, permitiéndole agregar una hoja de cálculo con un código mínimo. Consulte la lista completa de SDKs en el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo llamar al servicio con diversos SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}