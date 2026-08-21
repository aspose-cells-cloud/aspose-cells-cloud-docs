---
title: "Aspose.Cells Cloud Excel: API web de movimiento de hojas de cálculo – Cambiar posición de hoja programáticamente"
second_title: "Documentación"
ArticleTitle: "Cómo mover hojas de cálculo en Excel – Reorganizar orden y posición de hojas"
linktitle: "Mover hoja en hoja de cálculo"
type: docs
url: /move-worksheet-in-spreadsheet/
keywords: "API de movimiento de hoja, API de reordenamiento de hojas, API de cambio de orden de hojas, API de gestión de pestañas de Excel, API REST de Aspose Cells, automatización de posicionamiento de hojas, API de organización de libros de trabajo, API de estructura de hoja de cálculo, automatización en la nube de Excel, reordenamiento por lotes de hojas"
description: "Aprenda a mover hojas de cálculo dentro de libros de Excel para reorganizar el orden de las hojas y optimizar la estructura del libro de trabajo. Cambie las posiciones de las hojas, reordene las pestañas para mejorar su flujo de trabajo y automatice la organización de hojas para una gestión profesional de hojas de cálculo."
weight: 100
---

Mueva programáticamente hojas de cálculo dentro de libros de Excel utilizando la API de Aspose.Cells Cloud. Cambie posiciones de hojas, reordene pestañas y optimice la estructura del libro de trabajo mediante llamadas RESTful a la API. Ideal para automatizar la organización de hojas de cálculo y crear diseños estandarizados de libros de trabajo.

## **Mover hoja desde la API de hoja de cálculo**

### API web

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                   |
| :------------------- | :------ | :--------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet          | Archivo | FormData                                 | **Obligatorio**. El archivo de libro de Excel de origen (.xlsx, .xls, etc.) que contiene la hoja de cálculo que se va a reubicar.                             |
| worksheet            | Cadena  | Cadena de consulta                       | **Obligatorio**. El nombre exacto de la hoja de cálculo que se va a mover (por ejemplo, `Resumen`, `DatosCrudos_2024`).                                     |
| position             | Entero  | Cadena de consulta                       | **Obligatorio**. El nuevo índice de posición en base cero para la hoja de cálculo. Por ejemplo, `0` la mueve a la primera posición, `2` la sitúa como tercera hoja. |
| outPath              | Cadena  | Cadena de consulta                       | **Opcional**. La ruta de la carpeta de destino en el almacenamiento en la nube donde se guardará el libro reorganizado. Si es `null` u omite, por defecto usa la carpeta del archivo original. |
| outStorageName       | Cadena  | Cadena de consulta                       | **Obligatorio**. El identificador del nombre del servicio de almacenamiento en la nube configurado (por ejemplo, `TeamDrive`) donde se guardará el archivo de salida. |
| region               | Cadena  | Cadena de consulta                       | **Opcional**. La configuración regional (por ejemplo, `es-MX`) que se aplicará, la cual podría influir en ciertas reglas de formato durante la operación de guardado. |
| password             | Cadena  | Cadena de consulta                       | **Opcional**. La contraseña de descifrado necesaria para abrir y modificar un libro protegido con contraseña. Omítala si el archivo no está cifrado.           |

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

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                                      |
| ------ | ------------------------ | ---------------------------------------------------------------- |
| 200    | Solicitud correcta (OK)  | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido).   |
| 401    | No autorizado            | Token JWT inválido o faltante.                                   |
| 413    | Carga demasiado grande    | El archivo subido excede el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado del servidor.                                   |

## ¿Dónde debemos usar la API de movimiento de hoja en hoja de cálculo?

- **Generación estandarizada de informes**: Después de que los informes mensuales o trimestrales se generen automáticamente, la hoja de cálculo `Resumen` o `Resumen Ejecutivo` se mueve a la parte superior del libro de trabajo para garantizar que las conclusiones principales se presenten al abrir el archivo.
- **Tubería de procesamiento de datos**: Después de procesar hojas de datos crudos de distintas fuentes en el proceso ETL, la hoja `Datos_Procesados`, ya limpiada y transformada, se mueve a una posición lógica en el libro de trabajo (por ejemplo, en el centro), creando una estructura clara del proceso con los datos originales y los resultados del análisis.
- **Entrega de archivos personalizados según preferencias del usuario**: Después de que un usuario seleccione un diseño preferido mediante una interfaz de configuración (por ejemplo, colocar la página con gráficos al inicio), el sistema reordena automáticamente el orden de las hojas en el libro de trabajo según la selección y entrega el archivo personalizado.

## ¿Por qué debería usar la API de movimiento de hoja en hoja de cálculo?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido, y cuenta con documentación completa. En comparación con construir soluciones personalizadas, esto reduce significativamente la carga de trabajo de desarrollo.
- **Reducción de costos laborales**: Disminuye la necesidad de personal dedicado a la consolidación de documentos.
- **Pago por uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente utilice.
- **Costos cero de mantenimiento**: No es necesario mantener servidores, actualizar software ni lidiar con problemas de compatibilidad.

## Cómo usar la API de movimiento de hoja en hoja de cálculo con SDK

### Especificación de la API de movimiento de hoja en hoja de cálculo

La [Especificación de la API de movimiento de hoja en hoja de cálculo](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) proporciona una interfaz de programación accesible públicamente para facilitar interacciones REST directas desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Hoja1&destIndex=0" \
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

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel, permitiéndole mover hojas de cálculo con un código conciso. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.  
Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante distintos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}