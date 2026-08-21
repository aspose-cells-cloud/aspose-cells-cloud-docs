---
title: "Proteger un libro de Excel con la API de Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Proteger un archivo de Excel"
type: docs
url: /es/protect-excel-file/
aliases: [  /es/protect-excel-workbooks/ , /es/workbook/protect/ ]
keywords: "Aspose.Cells, protección de Excel, API, REST, SDK"
description: "Aprenda a proteger un libro de Excel mediante la API REST de Aspose.Cells Cloud. Incluye pasos de autenticación, parámetros de consulta y cuerpo, solicitud cURL y ejemplos de código SDK para C#, Java, PHP, Ruby, Node.js, Python, Perl y Go."
weight: 30
ArticleTitle: "Proteger un libro de Excel utilizando la API de Aspose.Cells Cloud"
---

Esta API REST **protege** un libro de Excel, permitiéndole proteger de forma segura un libro de Excel con contraseña y opciones de protección mediante Aspose.Cells Cloud.

## API PostProtectDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de consulta

| Nombre del parámetro | Tipo   | Descripción                                                           |
| -------------------- | ------ | --------------------------------------------------------------------- |
| folder               | string | Carpeta que contiene el libro de origen. _(opcional)_                 |
| storageName          | string | Nombre de la ubicación del almacenamiento. _(opcional; predeterminado = "Default")_ |

### Parámetros del cuerpo de la solicitud

| Nombre del parámetro | Tipo                      | Descripción                                                       |
| -------------------- | ------------------------- | ----------------------------------------------------------------- |
| protection           | WorkbookProtectionRequest | Objeto que define la configuración de protección para el libro. |

#### WorkbookProtectionRequest

| Nombre del parámetro | Tipo   | Descripción                                                                                                                                                 |
| -------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType       | string | Tipo de protección a aplicar. Valores permitidos (no sensibles a mayúsculas/minúsculas): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password             | string | Contraseña opcional para establecer en la protección.                                                                                                       |

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                      |
|--------|-----------------------------|------------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante.                                   |
| 413    | Payload demasiado grande     | El archivo subido supera el límite de tamaño.                   |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                                 |

## Cómo usar la API PostProtectDocument con SDK

### Requisitos previos

Antes de llamar a la API, asegúrese de haber completado los siguientes pasos:

- **Obtener un token de acceso JWT** mediante el flujo de autenticación descrito en la sección de seguridad.  
- **Subir el libro de Excel** a su almacenamiento de Aspose Cloud o confirmar que ya existe en la carpeta de destino.  
- **Conocer el nombre del almacenamiento** (predeterminado es `"Default"` si no se especifica) y el nombre exacto del archivo que desea proteger.

### Especificación de la API PostProtectDocument

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a> define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

### Ejemplo: Proteger un libro con cURL

1. Obtenga un token de acceso según se describe en **Requisitos previos / Autenticación**.  
2. Ejecute la solicitud:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   La respuesta incluirá un objeto de estado que confirma que la protección se realizó correctamente.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar con Aspose.Cells Cloud. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en su lógica de negocio. Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Respuesta completa de ejemplo

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```