---
title: "Aspose.Cells Cloud – Convertir rango de Excel a HTML"
description: "Convierta un rango específico de un archivo de Excel (por ejemplo, A1:C10) a un archivo HTML mediante la API REST de Aspose.Cells Cloud. Incluye autenticación, ejemplos de solicitud, manejo de respuesta, fragmentos de SDK y códigos de error."
keywords: "Aspose.Cells, Excel a HTML, conversión de rango, API en la nube, hoja de cálculo"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Convierta un rango seleccionado de un libro de Excel local directamente en un archivo HTML mediante Aspose.Cells Cloud. La conversión ocurre completamente en el servidor en la nube, por lo que nunca necesita cargar todo el libro ni tener Excel instalado localmente.

## API para convertir rango a HTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

El cuerpo de la solicitud es `multipart/form-data` que contiene el archivo de hoja de cálculo. Todas las demás opciones se proporcionan como parámetros de consulta.

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre             | Tipo    | Ubicación   | Obligatorio | Descripción                                                                  |
| ------------------ | ------- | ----------- | ----------- | ---------------------------------------------------------------------------- |
| **Spreadsheet**    | Archivo | FormData    | Sí          | El libro de Excel que se va a convertir.                                     |
| **worksheet**      | Cadena  | Consulta    | Sí          | Nombre de la hoja de cálculo que contiene el rango.                          |
| **range**          | Cadena  | Consulta    | Sí          | Área de celdas que se va a convertir, por ejemplo, `A1:C10`.                 |
| **outPath**        | Cadena  | Consulta    | No          | Ruta de carpeta donde debe guardarse el archivo HTML resultante (por defecto `null`). |
| **outStorageName** | Cadena  | Consulta    | No          | Nombre del servicio de almacenamiento para el archivo de salida.            |
| **fontsLocation**  | Cadena  | Consulta    | No          | Ruta a una carpeta personalizada de fuentes.                                  |
| **AutoRowsFit**    | Booleano| Consulta    | No          | Ajustar automáticamente todas las filas en la hoja de cálculo.               |
| **AutoColumnsFit** | Booleano| Consulta    | No          | Ajustar automáticamente todas las columnas en la hoja de cálculo.            |
| **region**         | Cadena  | Consulta    | No          | Identificador regional (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números y fechas. |
| **password**       | Cadena  | Consulta    | No          | Contraseña para abrir un libro protegido.                                    |
| **fontsLocation**  | Cadena  | Consulta    | No          | Ubicación personalizada de fuentes.                                           |
| **region**         | Cadena  | Consulta    | No          | Configuración regional/idioma de la hoja de cálculo.                         |
| **password**       | Cadena  | Consulta    | No          | Contraseña para abrir el archivo de hoja de cálculo.                         |

## Respuesta

La API devuelve el archivo HTML convertido como **fluxo binario** (`application/octet-stream`).

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

### Ejemplo de respuesta exitosa (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

Guarde el cuerpo de la respuesta en un archivo (por ejemplo, `report.html`) para ver la tabla renderizada en un navegador.

---

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                     |
| 413    | Carga útil demasiado grande | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## ¿Cómo utilizar la API Convert Range to HTML con SDK?

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) describe una API públicamente accesible, lo que permite interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiéndole convertir un rango de datos en un archivo HTML con un código mínimo.  
Consulte la lista completa de SDK de Aspose.Cells Cloud en nuestro [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK. Si la carga desde Gist está bloqueada, puede descargar los ejemplos directamente desde el repositorio.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}