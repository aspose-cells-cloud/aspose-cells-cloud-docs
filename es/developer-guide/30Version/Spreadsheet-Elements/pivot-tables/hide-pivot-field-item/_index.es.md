---
title: "Ocultar un elemento de campo de pivote en una tabla dinámica"
second_title: "Document"
linktitle: Ocultar
type: docs
url: /es/pivot-tables/hide-pivot-field-item/
aliases: [/es/hide-pivot-field-item/]
keywords: "Aspose.Cells, ocultar elemento de campo de pivote, API de tabla dinámica, API REST, SDK en la nube"
description: "Aprenda a ocultar un elemento de campo de pivote en una tabla dinámica utilizando la API REST de Aspose.Cells Cloud. Incluye detalles de la solicitud, ejemplo de cURL y fragmentos de código del SDK para múltiples lenguajes."
weight: 110
ArticleTitle: "Ocultar elemento de campo de pivote en una tabla dinámica – Guía de la API de Aspose.Cells Cloud"
---

Antes de llamar a la API, asegúrese de tener:

* Un **token de acceso JWT** válido (obtenible mediante el flujo de autenticación de Aspose Cloud).  
* El libro de trabajo objetivo cargado en su almacenamiento de Aspose Cloud.  
* La hoja de cálculo y la tabla dinámica ya creadas.

Estos requisitos previos evitan errores de autenticación y respuestas de "recurso no encontrado". Los siguientes pasos describen la configuración necesaria antes de invocar la API.

Esta API REST oculta un elemento de campo de pivote en una tabla dinámica.

## API PostPivotTableFieldHideItem

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                                                      |
| --------------------- | ------- | --------- | ------------------------------------------------------------------------------------------------ |
| name                  | string  | path      | Nombre del archivo Excel.                                                                        |
| sheetName             | string  | path      | Hoja de cálculo que contiene la tabla dinámica.                                                  |
| pivotTableIndex       | integer | path      | Índice de la tabla dinámica dentro de la hoja de cálculo.                                        |
| pivotFieldType        | string  | query     | Tipo del campo de pivote (Fila, Columna, Página, Datos, etc.).                                   |
| fieldIndex            | integer | query     | Índice de base cero del campo de pivote que se va a modificar.                                   |
| itemIndex             | integer | query     | Índice del elemento específico dentro del campo que se va a ocultar.                             |
| isHide                | boolean | query     | Establecer en **true** para ocultar el elemento; **false** para mostrarlo.                       |
| needReCalculate       | boolean | query     | Indica si la tabla dinámica debe recalcularse tras el cambio. El valor predeterminado es **false**. |
| folder                | string  | query     | Ruta de la carpeta donde se almacena el libro de trabajo.                                        |
| storageName           | string  | query     | Nombre del servicio de almacenamiento.                                                           |

**Referencia rápida de los parámetros de consulta requeridos**

- **pivotFieldType** – tipo del campo (por ejemplo, `Row`).  
- **fieldIndex** – índice de base cero del campo que se va a modificar.  
- **itemIndex** – índice de base cero del elemento que se va a ocultar/mostrar.  
- **isHide** – `true` para ocultar, `false` para mostrar.  
- **needReCalculate** – opcional, por defecto es `false`.

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El ejemplo siguiente muestra cómo llamar a la API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Detalles de la respuesta**

| Código de estado | Descripción                                                          |
| ---------------- | -------------------------------------------------------------------- |
| 200              | El elemento se ocultó correctamente.                                |
| 400              | Solicitud incorrecta – parámetros faltantes o inválidos.            |
| 401              | No autorizado – token JWT inválido o faltante.                      |
| 500              | Error del servidor – no se pudo completar la operación.             |

**Nota:** Si el `fieldIndex` o `itemIndex` proporcionado está fuera de rango, la API devuelve una respuesta **400 Bad Request**.

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar contra la API. Los SDK gestionan los detalles de bajo nivel, lo que le permite centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo ocultar un elemento de campo de pivote utilizando diversos SDK.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Preparar el libro de trabajo y la hoja de cálculo
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Cargar el libro de trabajo
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Crear la hoja de cálculo que contendrá la tabla dinámica
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Crear una segunda hoja de cálculo con datos de ejemplo
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Importar datos de ejemplo en Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Truncado por brevedad
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Agregar una tabla dinámica a PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Ocultar un elemento específico del campo de fila
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**Nota:** Los ejemplos de SDK asumen que ya ha configurado la autenticación (token JWT) y que el libro de trabajo se encuentra en la carpeta de almacenamiento especificada. Ajuste los parámetros `folder` y `storageName` según sea necesario para su entorno.