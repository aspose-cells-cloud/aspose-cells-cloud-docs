---
title: "Importar datos sin usar almacenamiento – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Importar datos sin almacenamiento"
type: docs
url: /es/import/without-using-storage/
aliases: [  /es/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, Cloud API, importar datos sin almacenamiento, API de importación de Excel, REST import"
description: "Aprenda cómo importar datos sin usar almacenamiento en un libro de Excel mediante la API de Aspose.Cells Cloud. Incluye formato de solicitud, parámetros, ejemplo de cURL, código del SDK y manejo de errores."
weight: 10
ArticleTitle: "Importar datos sin usar almacenamiento – Aspose.Cells Cloud API"
---

La importación de datos en Excel puede ser compleja, ya que muchos factores influyen en el resultado. Todos estos factores deben considerarse durante el proceso de **importación**. Aspose.Cells Cloud facilita la importación de diversos formatos y tipos de datos en un archivo de Excel con calidad profesional.

Esta API REST importa **datos** en un archivo de Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo          | Ubicación  | Descripción                                                                                                                                     |
| -------------------- | ------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| file                 | archivo       | formData   | El archivo de Excel que se va a cargar.                                                                                                         |
| ImportOption         | ImportOption  | cuerpo JSON | Objeto JSON que define los datos a importar, su tipo (por ejemplo, `IntArray`, `DoubleArray`, `StringArray`) y su ubicación dentro de la hoja de cálculo. |

Los parámetros **ImportOption** se describen en la **referencia de la opción ImportData** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter).

**Requisitos previos:**  
Se debe generar previamente un token JWT válido, y el tamaño del archivo no debe superar el límite del servicio (normalmente 100 MB). Los formatos de archivo admitidos incluyen XLS, XLSX, CSV y ODS. Asegúrese de tener instalado el SDK correspondiente si prefiere el acceso programático.

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente.                                              |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.                             |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                            |

**Notas:**  
Al enviar la solicitud, el encabezado `Content-Type: multipart/form-data` se establece automáticamente mediante la bandera `-F`. Para cargas útiles grandes, considere comprimir los datos antes de la importación e implementar lógica de reintento para errores transitorios.

## Cómo usar la API PostImportData con SDK

### Especificación de la API PostImportData

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*La bandera `-F` establece automáticamente `Content-Type: multipart/form-data`.*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}
---