---
title: "Proteger archivos de Excel"
second_title: "Documento"
linktitle: "Cifrar archivos de Excel"
type: docs
url: /es/protect-excel-files/
aliases:
  [
    /protect/without-storage/,
    /protect/without-using-storage/,
    /protect/without-using-storage/,
  ]
keywords: "Aspose.Cells, API de protección de Excel, cifrar libro de Excel, seguridad de hojas de cálculo en la nube, API REST"
description: "Utilice la API REST de Aspose.Cells Cloud para proteger archivos de Excel. Esta guía muestra cómo cifrar libros mediante HTTP POST, cURL y SDKs para múltiples lenguajes de programación, en 2026."
weight: 40
---

Esta API REST protege archivos de Excel.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación                  | Descripción                                    |
| --------------------- | ------ | -------------------------- | ---------------------------------------------- |
| file                  | file   | formData (cuerpo)          | Archivo para subir                             |
| password              | string | cadena de consulta (`password`) | Contraseña utilizada para proteger el libro |

### Respuesta


```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "nombre protegido: smaple1.xlsx",
      "FileSize": tamaño,
      "FileContent": "-----CadenaBase64 de sample1-----"
    },
    {
      "Filename": "nombre protegido: sample2.xlsx",
      "FileSize": tamaño,
      "FileContent": "-----CadenaBase64 de sample2-----"
    }
  ]
}
```

**Códigos de estado HTTP**

| Código | Significado                      | Descripción                                                    |
|--------|----------------------------------|----------------------------------------------------------------|
| 200    | OK                               | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta             | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                    | Token JWT inválido o faltante. |
| 413    | Carga demasiado grande           | El archivo subido excede el límite de tamaño. |
| 500    | Error interno del servidor       | Error inesperado del servidor. |

## Cómo usar la API PostProtect con SDKs

### Especificación de la API PostProtect

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo invocar la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----CadenaBase64 de sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----CadenaBase64 de sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Manejo de errores**

– La API puede devolver los siguientes códigos de estado:

| Código HTTP | Significado                                     | Ejemplo de carga útil JSON de error                          |
|-------------|-------------------------------------------------|--------------------------------------------------------------|
| 400         | Solicitud incorrecta (por ejemplo, archivo faltante) | `{"Code":400,"Message":"Se requiere el archivo."}`            |
| 401         | No autorizado (token inválido o faltante)       | `{"Code":401,"Message":"Token de acceso inválido."}`          |
| 403         | Prohibido (permisos insuficientes)              | `{"Code":403,"Message":"Acceso denegado."}`                   |
| 500         | Error interno del servidor                      | `{"Code":500,"Message":"Error inesperado del servidor."}`     |

### Utilizar SDKs de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel para que pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo invocar los servicios web de Aspose.Cells utilizando diversos SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}