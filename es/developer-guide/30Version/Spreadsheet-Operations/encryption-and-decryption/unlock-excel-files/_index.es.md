---
title: "Desbloquear archivos de Excel"
second_title: "Documento"
linktitle: "Desbloquear archivos de Excel"
type: docs
url: /es/unlock-excel-files/
aliases: [  /es/unlock/without-storage/ , /es/unlock/ , /es/unlock/without-using-storage/ ]
keywords: "Desbloquear Excel, Aspose.Cells Cloud, API REST, Desbloqueo de Excel, libro protegido por contraseña, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "La API REST de Aspose.Cells Cloud proporciona un punto final para desbloquear archivos de Excel protegidos por contraseña. Los SDK están disponibles para múltiples lenguajes de programación, incluidos Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift."
ArticleTitle: "Desbloquear archivos de Excel mediante la API REST de Aspose.Cells Cloud"
weight: 70
---

Esta API REST desbloquea archivos de Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### Seguridad y autenticación

Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación             | Descripción                                   |
| --------------------- | ------ | --------------------- | --------------------------------------------- |
| file                  | file   | formData (cuerpo HTTP) | Archivo que se va a cargar                    |
| password              | string | cadena de consulta     | Contraseña para desbloquear el archivo (si está protegido) |

### Respuesta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                             |
|--------|-----------------------------|---------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o faltante. |
| 413    | Payload demasiado grande     | El archivo cargado supera el límite de tamaño. |
| 500    | Error interno del servidor  | Error inesperado en el servidor. |

## Cómo usar la API PostUnlock con SDK

### Especificación de la API PostUnlock

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

**Notas**  
- La API puede desbloquear varios archivos de Excel en una sola solicitud; cada archivo se devuelve en el array `Files` de la respuesta.  
- Asegúrese de que la versión del SDK coincida con la versión de la API (`v3.0`) para evitar problemas de compatibilidad.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}