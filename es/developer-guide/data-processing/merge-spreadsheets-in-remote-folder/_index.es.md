---
title: "Fusionar hojas de cálculo coincidentes en una carpeta remota"
description: "Combina archivos de hojas de cálculo almacenados en el almacenamiento en la nube de Aspose Cloud en un único archivo. Admite más de 30 formatos de salida, como PDF, CSV, JSON, XLSX, ODS, XPS, entre otros."
keywords: "Aspose.Cells, fusionar hojas de cálculo, carpeta remota, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /es/merge-spreadsheets-in-remote-folder/
---

Combina múltiples archivos de hojas de cálculo que residen en una carpeta remota del almacenamiento en la nube de Aspose Cloud en un único archivo de salida. La operación se ejecuta completamente en la nube, eliminando la necesidad de descargar los archivos fuente localmente. Se admiten más de 30 formatos de salida (PDF, CSV, JSON, XLSX, ODS, XPS, …).

## API MergeSpreadsheetsInRemoteFolder

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud <a id="request-parameters"></a>

| Nombre                  | Tipo    | Ubicación | Obligatorio | Descripción                                                                                          |
| ----------------------- | ------- | --------- | ----------- | ---------------------------------------------------------------------------------------------------- |
| **folder**              | string  | query     | **Sí**      | Carpeta del almacenamiento en la nube que contiene las hojas de cálculo fuente.                     |
| **fileMatchExpression** | string  | query     | **Sí**      | Patrón para seleccionar archivos (por ejemplo, `*report*.xlsx`). Admite comodines `*` y `?`.        |
| **outFormat**           | string  | query     | **Sí**      | Formato de salida deseado (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …).                          |
| **mergeInOneSheet**     | boolean | query     | **Sí**      | `true` – todos los datos se fusionan en una única hoja de cálculo. `false` – cada archivo fuente obtiene su propia hoja de cálculo. |
| **storageName**         | string  | query     | No          | Nombre personalizado del almacenamiento; por defecto se usa el almacenamiento principal si se omite. |
| **outPath**             | string  | query     | No          | Carpeta de destino para el archivo fusionado. Si se omite, el archivo se guarda en la carpeta fuente. |
| **outStorageName**      | string  | query     | No          | Nombre del almacenamiento donde se escribirá el archivo fusionado.                                 |
| **fontsLocation**       | string  | query     | No          | Ruta a una carpeta que contiene fuentes personalizadas (necesaria para exportación a PDF/imágenes). |
| **region**              | string  | query     | No          | Configuración regional para el formato de números, fechas y monedas (por ejemplo, `es-ES`, `en-US`). |
| **password**            | string  | query     | No          | Contraseña para abrir cualquier hoja de cálculo fuente protegida.                                   |

## Ejemplo de solicitud (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **Respuesta**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

El archivo se puede descargar directamente desde `FileUrl` o guardarse en la ubicación especificada por `outPath`.

**Detalles de la respuesta correcta**

| Código de estado | Tipo de contenido           | Descripción                                |
| ---------------- | --------------------------- | ------------------------------------------ |
| 200 OK           | `application/octet-stream`  | Flujo binario del archivo del libro fusionado. |
| 202 Accepted     | `application/json`          | JSON que contiene `FileUrl`, `FileName`, etc. |

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                     |
| ------ | ----------------------- | --------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT no válido o ausente.                                  |
| 413    | Carga demasiado grande   | El archivo cargado supera el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                              |

## Cómo usar la API de fusión de hojas de cálculo con SDK

### Especificación OpenAPI

La <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">Especificación OpenAPI</a> proporciona una descripción legible por máquina de la API, lo que permite interacciones REST directas.

Puedes utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

Utilizar los SDK es la forma más rápida de desarrollar, ya que abstractan los detalles de bajo nivel, permitiéndote importar datos en una hoja de cálculo con un código breve. Consulta el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para ver la lista completa de SDK de Aspose.Cells Cloud.

---