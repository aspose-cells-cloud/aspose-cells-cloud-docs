---
title: "Quitar protección de libro de Excel – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Quitar protección de archivo de Excel"
type: docs
url: /es/excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, API para quitar protección de Excel, eliminar protección de libro, API REST, hoja de cálculo en la nube"
description: "Aprenda a quitar la protección de un libro de Excel mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, ejemplo de cURL y código de SDK en múltiples lenguajes."
weight: 60
ArticleTitle: "Quitar protección de libro de Excel – Aspose.Cells Cloud API"
---

Utilice esta API REST para quitar la protección de un libro de Excel.

## API DeleteUnProtectWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de ruta

| Parámetro | Tipo   | Descripción                                              | Obligatorio |
| --------- | ------ | -------------------------------------------------------- | ----------- |
| **name**  | string | Nombre del archivo del libro (incluyendo la extensión). | Sí          |

### Parámetros de consulta

| Nombre del parámetro | Tipo   | Descripción                                          |
| -------------------- | ------ | ---------------------------------------------------- |
| folder               | string | Ruta a la carpeta que contiene el libro original.   |
| storageName          | string | Nombre del servicio de almacenamiento donde reside el libro. |

### Parámetros del cuerpo de la solicitud

| Nombre del parámetro | Tipo                      | Descripción                                         |
| -------------------- | ------------------------- | --------------------------------------------------- |
| protection           | WorkbookProtectionRequest | Objeto que especifica la configuración de protección que se eliminará. |

#### WorkbookProtectionRequest

| Nombre del parámetro | Tipo   | Descripción                                                                                             |
| -------------------- | ------ | ------------------------------------------------------------------------------------------------------- |
| ProtectionType       | string | Tipo de protección que se eliminará (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password             | string | Contraseña necesaria para quitar la protección (opcional).                                             |

#### Ejemplo de cURL

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Respuesta (éxito)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Códigos de error de respuesta HTTPS

| Estado HTTP | Código                | Descripción                                                 |
| ----------- | --------------------- | ----------------------------------------------------------- |
| 400         | BadRequest            | Parámetros ausentes o no válidos.                           |
| 401         | Unauthorized          | Token de acceso inválido o ausente.                         |
| 404         | NotFound              | El libro especificado no se encontró en la carpeta/almacén dado. |
| 500         | InternalServerError   | Error inesperado del servidor.                              |

## Cómo utilizar la API DeleteUnProtectWorkbook con SDK

### Especificación de la API DeleteUnProtectWorkbook

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

### Utilizar los SDK de Aspose.Cells Cloud

El uso de un SDK simplifica la integración y reduce el código repetitivo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---