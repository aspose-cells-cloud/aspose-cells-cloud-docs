---
title: "Agregar una fila vacía en una hoja de cálculo de Excel"
ArticleTitle: "Agregar una fila vacía a una hoja de cálculo de Excel utilizando la API de Aspose.Cells Cloud"
second_title: "Documentos"
linktitle: "Fila"
type: docs
url: /es/rows/add/row/
aliases: [  /es/add-an-empty-row-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, agregar fila vacía, hoja de cálculo, API REST, insertar fila, hoja de cálculo en la nube"
description: "Utilice la API REST de Aspose.Cells Cloud para insertar una fila vacía en una hoja de cálculo de Excel. Admite múltiples SDK (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) para un desarrollo rápido."
weight: 20
---

Esta API REST agrega una nueva fila a una hoja de cálculo de Excel. Inserta una fila vacía en el índice especificado, el cual es de base cero.

**Requisitos previos:**  
- Debe incluirse un token de acceso válido de Aspose Cloud (Bearer JWT) en el encabezado `Authorization`.  
- El libro de trabajo objetivo debe cargarse en su almacenamiento de Aspose Cloud, y los parámetros `folder` y `storageName` deben apuntar a su ubicación.

**Notas:**  
- El `rowIndex` es de base cero; insertar en el índice 0 agrega una fila al inicio de la hoja de cálculo.  
- Las hojas de cálculo de Excel tienen un máximo de 1 048 576 filas; intentar insertar más allá de este límite resultará en un error.

## API PutInsertWorksheetRow

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Parámetros de la solicitud**

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                                  |
|----------------------|---------|-----------|--------------------------------------------------------------|
| name                 | string  | path      | Nombre del archivo del libro de trabajo.                    |
| sheetName            | string  | path      | Nombre de la hoja de cálculo.                               |
| rowIndex             | integer | path      | Índice de base cero donde se insertará la nueva fila.       |
| folder               | string  | query     | Ruta de la carpeta en el almacenamiento que contiene el libro. |
| storageName          | string  | query     | Nombre del almacenamiento de Aspose Cloud a utilizar.       |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Nota:** Todos los puntos finales de Aspose.Cells Cloud requieren HTTPS. Utilice el esquema seguro `https://` para llamadas en producción.

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

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                                         |
|--------|--------------------------|---------------------------------------------------------------------|
| 200    | OK                       | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT inválido o faltante.                                      |
| 413    | Payload demasiado grande  | El archivo cargado excede el límite de tamaño.                     |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                   |

*Ejemplo de una respuesta de error (por ejemplo, cuando el índice de fila excede el límite de la hoja de cálculo):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Índice de fila fuera de rango. Número máximo de filas permitidas: 1048576."
}
```

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK abstrae los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}