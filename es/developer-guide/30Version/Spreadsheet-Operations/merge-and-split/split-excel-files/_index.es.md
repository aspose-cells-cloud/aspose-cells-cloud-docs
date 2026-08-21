---
title: "Dividir un libro de Excel en varios archivos"
ArticleTitle: "Cómo dividir un libro de Excel en varios archivos mediante la API de Aspose.Cells Cloud"
second_title: "Documentos"
linktype: "Dividir un archivo de Excel"
type: docs
url: /split-multi-excel-files/
aliases: [/split/multi-files/]
keywords: "Excel, Aspose.Cells Cloud, API REST, dividir libro, varios archivos, JPEG, PNG, PDF, CSV, JSON"
description: "La API REST de Aspose.Cells Cloud permite dividir un libro de Excel en varios archivos en distintos formatos. Esta documentación proporciona los parámetros de solicitud, un ejemplo con cURL y ejemplos de código en SDK para lenguajes como C#, Java, PHP, Ruby, Node.js, Python, Perl y Go."
weight: 130
---

Esta API REST divide un **libro** de Excel en varios archivos en distintos formatos.

> **Requisitos previos** – Para usar esta API, debe obtener un token JWT válido, asegurarse de que esté utilizando una versión compatible del SDK y verificar que su libro esté almacenado en una ubicación compatible. Además, la API impone límites de tamaño de archivo que se detallan en las directrices de la plataforma.

## API PostWorkbookSplit

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación   | Descripción                                                                                  | Obligatorio |
| --------------------- | ------- | ----------- | -------------------------------------------------------------------------------------------- | ----------- |
| files[]               | archivo | formData    | Uno o más libros de Excel que se van a **dividir**. Utilice `file1`, `file2`, … en la solicitud. | Sí          |
| format                | cadena  | Query       | Formato deseado para los archivos divididos.                                                | No          |
| from                  | entero  | Query       | Índice inicial de la hoja de cálculo.                                                       | No          |
| to                    | entero  | Query       | Índice final de la hoja de cálculo.                                                          | No          |
| horizontalResolution  | entero  | Query       | Resolución horizontal de la imagen.                                                          | No          |
| verticalResolution    | entero  | Query       | Resolución vertical de la imagen.                                                            | No          |
| outFolder             | cadena  | Query       | Carpeta de salida para los archivos divididos.                                               | No          |
| splitNameRule         | cadena  | Query       | Regla de nomenclatura aplicada a los archivos divididos.                                     | No          |
| folder                | cadena  | Query       | Carpeta que contiene el libro original.                                                      | No          |
| storageName           | cadena  | Query       | Nombre del almacenamiento a utilizar.                                                        | No          |

### **Respuesta**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[nombre_archivo1]",
        "Filesize" : [tamaño_archivo],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[nombre_archivo2]",
        "Filesize" : [tamaño_archivo],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[nombre_archivo3]",
        "Filesize" : [tamaño_archivo],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                   |
|--------|-----------------------------|---------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros ausentes o inválidos (p. ej., tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                                  |
| 413    | Payload demasiado grande     | El archivo subido supera el límite de tamaño.                 |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                              |

## Cómo utilizar la API PostWorkbookSplit con SDK

### Especificación de la API PostWorkbookSplit

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) define una interfaz de programación públicamente accesible que le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted pueda centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando distintos SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---