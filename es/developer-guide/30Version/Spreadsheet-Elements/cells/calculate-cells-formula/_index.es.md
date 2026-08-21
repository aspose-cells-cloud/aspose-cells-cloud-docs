---
title: "Calcular fórmula de celda – API de Aspose.Cells Cloud"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, calcular fórmula de celda, API de Excel, API REST, SDK"
description: "Calcule una fórmula de celda de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye el punto de conexión, parámetros, ejemplo con cURL y fragmentos de SDK."
ArticleTitle: "Calcular fórmula de celda – Documentación de la API de Aspose.Cells Cloud"
---

## API REST

Esta API REST calcula la **fórmula de celda** en un libro de Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación del parámetro (ruta/consulta/cuerpo) | Descripción                                                          |
| --------------------- | ------ | ----------------------------------------------- | -------------------------------------------------------------------- |
| name                  | string | path                                            | Nombre del archivo de Excel (por ejemplo, `Book1.xlsx`).            |
| sheetName             | string | path                                            | Nombre de la hoja de cálculo que contiene la celda.                 |
| cellName              | string | path                                            | Dirección de la celda que se va a calcular (por ejemplo, `A1`).     |
| options               | object | body                                            | Objeto JSON con opciones de cálculo (véase la tabla **Objeto options**). |
| folder                | string | query                                           | Carpeta en el almacenamiento donde se encuentra el archivo.         |
| storageName           | string | query                                           | Nombre del almacenamiento de Aspose Cloud.                          |

#### Objeto options

| Campo           | Tipo    | Descripción                                                                    | Valor predeterminado |
| --------------- | ------- | ------------------------------------------------------------------------------ | -------------------- |
| CalcStackSize   | string  | Tamaño máximo de la pila de cálculo.                                           | `"1"`                |
| IgnoreError     | boolean | Si es `true`, los errores de cálculo se ignoran y el valor de la celda se establece en `#N/A`. | `false`              |
| Recursive       | boolean | Habilita el cálculo recursivo de celdas dependientes.                          | `false`              |
| Precision       | string  | Número de decimales para los resultados numéricos.                             | `"15"`               |
| UseThreading    | boolean | Habilita el cálculo multiproceso.                                              | `false`              |


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
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT no válido o ausente. |
| 413    | Payload demasiado grande    | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado del servidor. |

## Cómo usar la API PostCellCalculate con SDK

### Especificación de la API PostCellCalculate

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube con cURL. **Primero obtenga un token JWT** autenticándose contra el punto de conexión `/connect/token` y reemplace `<jwt token>` por el valor del token.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
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

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
---