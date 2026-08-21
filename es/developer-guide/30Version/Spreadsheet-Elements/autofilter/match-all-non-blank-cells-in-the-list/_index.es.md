---
title: "Coincidir con todas las celdas no vacías en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Coincidir con todas las celdas no vacías"
type: docs
url: /autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, coincidir celdas no vacías, AutoFiltro, API de Excel"
description: "Aprenda a usar la API REST de Aspose.Cells Cloud para coincidir con todas las celdas no vacías en una lista de AutoFiltro en una hoja de cálculo de Excel. Incluye endpoint, parámetros, autenticación, esquema de respuesta, códigos de error y ejemplos de SDK."
ArticleTitle: "Coincidir con todas las celdas no vacías en una hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud"
weight: 100
---

**Resumen**  
La operación *Coincidir con todas las celdas no vacías* aplica un AutoFiltro a una hoja de cálculo y devuelve únicamente las filas en las que la columna especificada contiene datos, ignorando las celdas vacías. Esto resulta útil para limpiar conjuntos de datos, generar informes o preparar datos para análisis posteriores.

**Requisitos previos**  
- Un token JWT válido para la autenticación en Aspose.Cells Cloud.  
- El libro debe estar cargado en el almacenamiento de Aspose Cloud.  
- Necesita el nombre del archivo, el nombre de la hoja de cálculo y el índice de columna en base cero (`fieldIndex`) que desea filtrar.

Esta API REST coincide con todas las celdas no vacías en la lista de AutoFiltro de una hoja de cálculo de Excel.

## API PostWorksheetMatchNonBlanks

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                    |
| --------------------- | ------- | --------- | -------------------------------------------------------------- |
| name                  | string  | path      | Nombre del archivo de Excel.                                   |
| sheetName             | string  | path      | Nombre de la hoja de cálculo que contiene el AutoFiltro.       |
| fieldIndex            | integer | query     | Índice en base cero de la columna a la que se aplica el filtro. |
| folder                | string  | query     | _(Opcional)_ Ruta de la carpeta donde se encuentra el archivo. |
| storageName           | string  | query     | _(Opcional)_ Nombre del servicio de almacenamiento a utilizar. |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                                  |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño.                |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                              |

*Ejemplo de respuesta de error (400)*  

```json
{
  "Code": 400,
  "Message": "Parámetro no válido: fieldIndex debe ser un entero no negativo."
}
```

## Cómo usar la API PostWorksheetMatchNonBlanks con SDK

### Especificación de la API PostWorksheetMatchNonBlanks

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
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

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}