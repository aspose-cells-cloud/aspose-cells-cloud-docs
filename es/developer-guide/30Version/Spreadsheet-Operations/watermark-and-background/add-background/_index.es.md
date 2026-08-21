---
title: "Agregar imagen de fondo a un libro de trabajo"
second_title: "Documentos"
linktype: "add"
type: docs
url: /es/add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, agregar imagen de fondo, API de Excel, REST, SDK en la nube, cURL, fondo del libro de trabajo"
description: "Aprenda cómo agregar una imagen de fondo a un libro de trabajo de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye parámetros requeridos, detalles de autenticación, un ejemplo completo con cURL e información sobre manejo de errores."
weight: 160
---

## API REST

Esta API REST agrega una **imagen de fondo** a un libro de trabajo de Excel.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de consulta

| Nombre del parámetro | Tipo   | Descripción                                             |
| -------------------- | ------ | ------------------------------------------------------- |
| `picPath`            | string | Ruta al archivo de imagen que se usará como fondo.     |
| `folder`             | string | Carpeta que contiene el libro de trabajo original.     |
| `storageName`        | string | Nombre del almacenamiento donde reside el archivo.     |

### Parámetro del cuerpo de solicitud

| Nombre del parámetro | Tipo | Descripción                                                     |
| -------------------- | ---- | --------------------------------------------------------------- |
| `datafile`           | file | Archivo del libro de trabajo al que se aplicará el fondo.      |

**Parámetro de ruta** – `{name}` en la URL representa el **nombre del archivo del libro de trabajo** (por ejemplo, `Book1.xlsx`).


### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**Códigos de estado HTTP**

| Código | Significado                  | Descripción                                           |
|--------|------------------------------|-------------------------------------------------------|
| 200    | OK                           | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta         | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                | Token JWT inválido o faltante.                        |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.        |
| 500    | Error interno del servidor   | Error inesperado en el servidor.                      |
## Cómo usar la API PutWorkbookBackground con SDK

### Especificación de la API PutWorkbookBackground

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) define una interfaz de programación pública que permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra una solicitud completa, incluyendo la bandera de carga de archivos multipart y el encabezado de autenticación requerido.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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


### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en su lógica empresarial. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo llamar a los servicios web de Aspose.Cells utilizando diversos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}