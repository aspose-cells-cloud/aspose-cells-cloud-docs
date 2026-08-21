---
title: "Renombrar hoja de cálculo en Excel – API de Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Cómo renombrar hojas en Excel – Cambiar nombres de hojas"
linktype: "Rename Worksheet in Spreadsheet"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "renombrar hoja de cálculo, Aspose.Cells Cloud, API de Excel, hoja de cálculo, SDK, API REST"
description: "Renombre fácilmente hojas de cálculo de Excel mediante la API de Aspose.Cells Cloud. Aprenda los parámetros necesarios, vea ejemplos con cURL y obtenga código de SDK para C#, Java, Python y más."
weight: 100
---

Renombre programáticamente hojas de cálculo en libros de Excel utilizando la API de Aspose.Cells Cloud. Cambie nombres de hojas, actualice etiquetas de pestañas dinámicamente y automatice la organización de hojas de cálculo mediante llamadas a la API REST. Útil para la estandarización de documentos y la automatización de flujos de trabajo.

## Renombrar nombre de hoja en la API de hoja de cálculo

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**Ejemplo con cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Hoja1&targetName=Informe_T1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@miLibro.xlsx"
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                                                                                     |
| --------------------- | ------ | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**       | File   | FormData  | **Obligatorio**. El archivo del libro de Excel (.xlsx, .xls, etc.) que contiene la hoja de cálculo que se va a renombrar.                                                                                      |
| **sourceName**        | String | Query     | **Obligatorio**. El nombre actual de la hoja de cálculo que desea renombrar.                                                                                                                                   |
| **targetName**        | String | Query     | **Obligatorio**. El nuevo nombre que se asignará a la hoja de cálculo. Debe cumplir con las reglas de nomenclatura de Excel (no puede contener `:`, `\`, `?`, `*`, `[`, `]`) y ser único dentro del libro. |
| **outPath**           | String | Query     | **Opcional**. La ruta de la carpeta de destino en el almacenamiento en la nube donde se guardará el libro renombrado. Si es `null` u omite este parámetro, el servicio guardará el archivo en la misma carpeta que el libro original (o en una ruta predeterminada). |
| **outStorageName**    | String | Query     | **Opcional**. El identificador del nombre del servicio de almacenamiento en la nube configurado (por ejemplo, `ArchiveStorage`). Si se omite, se utiliza el almacenamiento predeterminado.                        |
| **region**            | String | Query     | **Opcional**. La configuración regional (por ejemplo, `es-ES`) que puede influir en la codificación de caracteres o en las convenciones regionales de nomenclatura.                                          |
| **password**          | String | Query     | **Opcional**. La contraseña de descifrado necesaria para abrir y modificar un libro protegido con contraseña. Omítalo si el archivo no está cifrado.                                                          |

**Notas**: Los nombres de hojas están limitados a 31 caracteres y no pueden contener los caracteres `:`, `\`, `?`, `*`, `[` ni `]`.

### Respuesta

Una solicitud correcta devuelve un objeto JSON con información de estado y un enlace al archivo renombrado.

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

| Código | Significado              | Descripción                                                  |
| ------ | ------------------------ | ------------------------------------------------------------ |
| 200    | OK                       | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT no válido o faltante.                              |
| 413    | Carga demasiado grande    | El archivo subido supera el límite de tamaño.               |
| 500    | Error interno del servidor | Error inesperado en el servidor.                            |

## ¿Dónde debemos utilizar la API de Renombrar hoja en hoja de cálculo?

- **Generación de informes y estandarización de marca** – Al generar informes de clientes automáticamente, se renombran las hojas genéricas (por ejemplo, `Hoja1`) con nombres específicos para el cliente (por ejemplo, `AcmeCorp_Informe_T1`) para garantizar una entrega profesional.
- **Estandarización de canalización de procesamiento de datos** – En flujos de trabajo ETL, las hojas exportadas con nombres irregulares se renombran según nombres estandarizados como `Datos_crudos` o `Datos_limpios`, cumpliendo así los requisitos de análisis posteriores.
- **Entrega de contenido multilingüe** – Según la preferencia lingüística del usuario, los nombres de las hojas se localizan (por ejemplo, `数据` o `Datos`) antes de entregar el archivo, ofreciendo una experiencia personalizada.

## ¿Por qué debería utilizar la API de Renombrar hoja en hoja de cálculo?

- **Amigable para desarrolladores** – Proporciona SDK para varios lenguajes con documentación completa, simplificando la integración en comparación con construir una solución personalizada.
- **Reducción del esfuerzo manual** – Automatiza el renombrado de hojas, reduciendo el trabajo manual.
- **Modelo de pago por uso** – Se cobra únicamente por las llamadas a la API, eliminando los costos iniciales de licencia.
- **Sin mantenimiento de servidor** – Al tratarse de un servicio en la nube, elimina la necesidad de alojar y mantener servidores ni aplicar actualizaciones de software.
- **Soporte para automatización** – Facilita la estandarización automatizada de documentos dentro de flujos de trabajo.

## Cómo utilizar la API de Renombrar hoja en hoja de cálculo con SDK

### Especificación OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> detalla una interfaz de programación accesible públicamente, permitiendo interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Hoja1&destName=NuevaHoja" \
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

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. El SDK abstracte los detalles HTTP subyacentes, permitiéndole renombrar hojas con un código mínimo. Consulte el repositorio de GitHub para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}