---
title: "Coincidir con todas las celdas en blanco en una hoja de cálculo de Excel"
ArticleTitle: "Coincidir con todas las celdas en blanco en una hoja de cálculo de Excel – Guía de la API de Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Coincidir con todas las celdas en blanco"
type: docs
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, celdas en blanco, AutoFilter, API REST, Excel"
description: "Aprenda a utilizar la API REST de Aspose.Cells Cloud para filtrar y coincidir con todas las celdas en blanco en una hoja de cálculo de Excel. Incluye el punto final, los parámetros, los pasos de autenticación, un ejemplo con cURL y fragmentos de código para SDK en C#, Java, Python y más."
weight: 100
---

Esta API REST coincide con todas las **celdas en blanco** en la lista de filtros de una hoja de cálculo de Excel.

**Prerrequisitos:** Antes de llamar a este punto final, asegúrese de tener un token de acceso JWT válido, de que el libro esté cargado en el almacenamiento de Aspose Cloud y de que conozca la carpeta de almacenamiento (si aplica). Proporcione los parámetros `folder` y `storageName` cuando el archivo no se encuentre en la carpeta raíz predeterminada.

## API PostWorksheetMatchBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.


### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                            |
|----------------------|---------|-----------|------------------------------------------------------------------------|
| name                 | string  | path      | El nombre del archivo del libro.                                         |
| sheetName            | string  | path      | El nombre de la hoja de cálculo que contiene el filtro.                    |
| fieldIndex           | integer | query     | Índice de base cero de la columna a la que se aplica el filtro.         |
| folder               | string  | query     | La ruta de la carpeta en el almacenamiento donde se encuentra el libro.              |
| storageName          | string  | query     | El nombre del almacenamiento de Aspose Cloud.                                   |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o faltante. |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |
## Cómo utilizar la API PostWorksheetMatchBlanks con SDK

### Especificación de la API PostWorksheetMatchBlanks

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{{< /tab >}}

{{< tab tabNum="12" >}}
```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}