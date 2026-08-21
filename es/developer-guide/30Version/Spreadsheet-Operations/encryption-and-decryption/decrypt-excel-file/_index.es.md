---
title: "Descifrar un libro de Excel"
second: "Documento"
linktitle: "Descifrar un archivo de Excel"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, descifrado de Excel, API REST, SDK en la nube"
description: "Aprenda cómo descifrar un libro de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye parámetros requeridos, ejemplo de cURL, ejemplos de código con SDK y detalles sobre manejo de errores."
ArticleTitle: "Cómo descifrar un libro de Excel utilizando la API de Aspose.Cells Cloud"
weight: 50
---

**Prerrequisitos**

- Un token de acceso JWT válido.
- El libro debe estar cargado en el almacenamiento de Aspose Cloud y su ruta especificada en el parámetro de consulta `folder`.

## API DeleteDecryptWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de consulta

| Nombre del parámetro | Tipo   | Descripción                                           |
| --------------------- | ------ | ----------------------------------------------------- |
| folder                | string | Ruta de la carpeta donde se encuentra el libro original. |
| storageName           | string | Nombre del almacenamiento donde reside el libro.      |

### Parámetro del cuerpo de la solicitud

| Nombre del parámetro | Tipo                      | Descripción                                          |
| --------------------- | ------------------------- | ---------------------------------------------------- |
| encryption            | WorkbookEncryptionRequest | Configuraciones de cifrado necesarias para el descifrado. |

### WorkbookEncryptionRequest

| Nombre del parámetro | Tipo    | Descripción                                                                                                    |
| --------------------- | ------- | -------------------------------------------------------------------------------------------------------------- |
| EncryptionType        | string  | Algoritmo de cifrado (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength             | integer | Longitud de la clave de cifrado en bits.                                                                      |
| Password              | string  | Contraseña utilizada para el descifrado.                                                                       |

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Ejemplos de respuestas de error**

```json
{
  "Code": "400",
  "Message": "Parámetros de solicitud inválidos."
}
```

```json
{
  "Code": "401",
  "Message": "La autenticación falló. Token JWT inválido o faltante."
}
```

```json
{
  "Code": "413",
  "Message": "Carga útil demasiado grande. El archivo cargado supera el tamaño permitido."
}
```

```json
{
  "Code": "500",
  "Message": "Error interno del servidor. Intente nuevamente más tarde."
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                              |
| ------ | --------------------------- | -------------------------------------------------------- |
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                           |
| 413    | Carga útil demasiado grande | El archivo cargado supera el límite de tamaño.          |
| 500    | Error interno del servidor  | Error inesperado del servidor.                           |

## Cómo utilizar la API DeleteDecryptWorkbook con SDK

### Especificación de la API DeleteDecryptWorkbook

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}