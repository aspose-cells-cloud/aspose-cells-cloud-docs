---
title: "Cifrar un libro de Excel con la API de Aspose.Cells Cloud – Ejemplos rápidos de cURL y SDK"
second_title: "Documento"
linktype: "Cifrar un archivo de Excel"
type: docs
url: /excel-file-encrypt/
aliases: [/encrypt-excel-workbooks/, /workbook/encrypt/]
keywords: "Cifrar libro con Aspose Cells, API de cifrado de Excel, API REST, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Aprenda a cifrar un libro de Excel mediante la API REST de Aspose.Cells Cloud (v3.0). Incluye comandos cURL, ejemplos de código para SDK (C#, Java, Python, etc.), parámetros requeridos y manejo de errores."
weight: 20
ArticleTitle: "Cifrar un libro de Excel con la API de Aspose.Cells Cloud – Ejemplos de cURL y SDK"
---

Esta API REST cifra un **libro** de Excel.

**Prerrequisitos:** Debe poseer un token JWT válido y haber subido el libro a una ubicación de almacenamiento antes de llamar a este endpoint.

## API PostEncryptDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de consulta**

| Nombre del parámetro | Tipo   | Obligatorio | Descripción                                   |
| --------------------- | ------ | ----------- | --------------------------------------------- |
| folder                | string | ✗           | Ruta de la carpeta donde se encuentra el libro original. |
| storageName           | string | ✗           | Nombre del almacenamiento a utilizar.         |

### **Parámetro del cuerpo de la solicitud**

| Nombre del parámetro | Tipo                      | Obligatorio | Descripción                           |
| --------------------- | ------------------------- | ----------- | ------------------------------------- |
| encryption            | WorkbookEncryptionRequest | ✓           | Configuración de cifrado para el libro. |

#### **WorkbookEncryptionRequest**

| Nombre del parámetro | Tipo    | Obligatorio | Descripción                                                                        |
| --------------------- | ------- | ----------- | ---------------------------------------------------------------------------------- |
| EncryptionType        | string  | ✓           | Algoritmo de cifrado. Consulte la tabla siguiente para los valores admitidos y su significado. |
| KeyLength             | integer | ✗           | Longitud de la clave de cifrado en bits (se ignora para `XOR` y `Compatible`).   |
| Password              | string  | ✓           | Contraseña utilizada para el cifrado.                                              |

#### **Valores de EncryptionType**

| Valor                             | Descripción                                    |
| --------------------------------- | ---------------------------------------------- |
| `XOR`                             | Algoritmo XOR simple (heredado, baja seguridad). |
| `Compatible`                      | Cifrado compatible con Excel 97‑2003 (40 bits). |
| `EnhancedCryptographicProviderV1` | AES‑128 con hash SHA‑1.                        |
| `StrongCryptographicProvider`     | AES‑256 con hash SHA‑512 (el más seguro).      |

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                           |
| ------ | --------------------------- | ----------------------------------------------------- |
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o inválidos (p. ej., tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                         |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.       |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                     |

## Cómo usar la API PostEncryptDocument con SDK

### Especificación de la API PostEncryptDocument

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Cifrar el libro "test.xlsx" utilizando el algoritmo XOR (clave de 128 bits) y la contraseña "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Posibles respuestas de error**

| Estado HTTP | Código                | Mensaje                                              |
| ----------- | --------------------- | ---------------------------------------------------- |
| 400         | BadRequest            | Parámetros faltantes o inválidos.                    |
| 401         | Unauthorized          | El token de autenticación no está presente o es inválido. |
| 403         | Forbidden             | Permisos insuficientes para acceder al almacenamiento. |
| 500         | InternalServerError   | Error inesperado en el servidor.                     |

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK maneja los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}