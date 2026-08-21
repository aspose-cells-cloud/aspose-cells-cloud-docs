---
title: "Exportar objeto OLE – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Objeto OLE"
type: docs
url: /es/export-excel-ole-object/
aliases: [  /es/export/excel-ole-object/ ]
keywords: "Aspose.Cells, objeto OLE, exportación, Excel, API en la nube, PDF, PNG, DOCX, PPTX"
description: "Exporte objetos OLE desde un libro de Excel utilizando Aspose.Cells Cloud API. Aprenda sobre el formato de solicitud, parámetros, ejemplo con cURL y manejo de errores."
weight: 20
ArticleTitle: "Exportar objeto OLE – Aspose.Cells Cloud API"
---

## **API REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de solicitud

| Parámetro       | Ubicación  | Tipo   | Obligatorio | Descripción                                                                    |
| --------------- | --------- | ------ | ----------- | ------------------------------------------------------------------------------ |
| `file`          | Datos del formulario | archivo | Sí          | El libro de Excel (`.xlsx`, `.xls`, etc.) que contiene los objetos OLE.      |
| `outputFormat`  | Consulta     | cadena | Sí          | Formato de destino para los objetos exportados (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`    | Consulta     | cadena | Sí          | Valor fijo `oleobject`.                                                       |


### Respuesta

Una solicitud correcta devuelve un objeto JSON que enumera los archivos exportados:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Códigos de estado HTTP**

| Código | Significado                     | Descripción                                      |
|--------|---------------------------------|--------------------------------------------------|
| 200    | OK                              | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta            | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                   | Token JWT no válido o faltante. |
| 413    | Carga demasiado grande           | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor      | Error inesperado del servidor. |

## Cómo utilizar la API PostExport con SDK

### Especificación de la API PostExport

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### ¿Qué es un objeto OLE?

Un **objeto OLE (Object Linking and Embedding, o vinculación e incrustación de objetos)** incrusta contenido externo —como documentos de Word, diapositivas de PowerPoint, imágenes u otros archivos— dentro de un libro de Excel. Al exportar, el contenido incrustado se extrae y guarda en el formato de salida solicitado.

### Descripción general del punto de conexión

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – Debe establecerse en `oleobject`.
- `format` – Formato de salida deseado (por ejemplo, `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}