---
title: "Calcular una fórmula en una hoja de cálculo de Excel"
second_title: "Documento"
linktitle: "Calcular"
type: docs
url: /es/worksheets/calculate-formula/
aliases: [  /es/calculate-formula-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, cálculo de fórmulas, API REST, SDKs, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Calcule fórmulas en una hoja de cálculo de Excel utilizando la API REST de Aspose.Cells Cloud. Admite múltiples SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) con ejemplos listos para usar."
weight: 20
ArticleTitle: "Calcular una fórmula en una hoja de cálculo de Excel – Documentación de Aspose.Cells Cloud"
---

Esta API REST devuelve el **valor calculado de una fórmula** en una hoja de cálculo. Puede utilizarse para **evaluar una fórmula de Excel** directamente desde su aplicación.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                        |
| --------------------- | ------ | --------- | -------------------------------------------------- |
| name                  | string | path      | Nombre del archivo de Excel.                      |
| sheetName             | string | path      | Nombre de la hoja de cálculo que contiene la fórmula. |
| formula               | string | query     | La fórmula que se va a evaluar (por ejemplo, `SUM(A5:A10)`). |
| folder                | string | query     | Carpeta donde se almacena el documento.           |
| storageName           | string | query     | Nombre del servicio de almacenamiento (si aplica). |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Autenticación

Todas las solicitudes deben incluir un token **Bearer JWT** válido en el encabezado `Authorization`:

```
Authorization: Bearer <your_jwt_token>
```

Puede obtener un token siguiendo el flujo OAuth 2.0 descrito en la guía de autenticación de Aspose.Cells Cloud.

### Códigos de estado de respuesta posibles

| Código | Descripción                                          |
| ------ | ---------------------------------------------------- |
| 200    | Solicitud correcta; se devuelve el valor de la fórmula. |
| 400    | Solicitud incorrecta: faltan parámetros o estos son inválidos. |
| 401    | No autorizado: token JWT inválido o ausente.         |
| 404    | No encontrado: el archivo o la hoja de cálculo especificados no existen. |
| 500    | Error interno del servidor: condición inesperada en el servidor. |

Puede utilizar la herramienta de línea de comandos **cURL** para invocar fácilmente los servicios web de Aspose.Cells Cloud. El siguiente ejemplo muestra cómo solicitar el resultado de una fórmula con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de integrar la API. Un SDK gestiona los detalles de bajo nivel, lo que le permite centrarse en su lógica de negocio. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo invocar los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**Consulte también:**  
- [Obtener hoja de cálculo](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [Actualizar hoja de cálculo](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [Calcular todas las fórmulas](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---