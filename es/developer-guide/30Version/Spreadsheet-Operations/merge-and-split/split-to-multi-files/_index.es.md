---
title: "Dividir un archivo de Excel en varios archivos"
second_title: "Document"
linktype: "Split Multi Excel files"
type: docs
url: /es/split-an-excel-file-to-multi-files/
aliases: [  /es/split-excel-workbooks/ , /es/workbook/split/ ]
keywords: "Aspose.Cells, Cloud, Excel, Split, API, PDF, CSV, JSON"
description: "Utilice la API REST de Aspose.Cells Cloud para dividir libros de Excel de varias hojas en archivos independientes. Admite formatos de salida como PDF, CSV y JSON, y está disponible mediante SDKs para Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby y Swift."
weight: 32
ArticleTitle: "Dividir un archivo de Excel en varios archivos - Documentación de Aspose.Cells Cloud"
---

La API REST de Aspose.Cells Cloud divide libros de Excel de varias hojas en archivos independientes.

**Requisitos previos**  
Antes de llamar a la API, debe obtener un token JWT válido e incluirlo en el encabezado `Authorization` de cada solicitud. Consulte la [guía de autenticación](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) para más detalles.

## API PostSplit

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.


### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación  | Descripción                                                       |
|----------------------|--------|------------|-------------------------------------------------------------------|
| file                 | file   | formData   | El libro de Excel que se va a cargar.                             |
| format               | string | query      | Formato de salida deseado (por ejemplo, `pdf`, `csv`, `json`).    |
| password             | string | query      | Contraseña para un libro cifrado (opcional).                      |
| from                 | integer| query      | Índice de la primera hoja a incluir (basado en 1).                |
| to                   | integer| query      | Índice de la última hoja a incluir (inclusive).                   |

### **Respuesta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[nombre_archivo1]",
            "Filesize" : [tamaño_archivo],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[nombre_archivo2]",
            "Filesize" : [tamaño_archivo],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[nombre_archivo3]",
            "Filesize" : [tamaño_archivo],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**Códigos de estado HTTP**

| Código | Significado                  | Descripción                                                         |
|--------|------------------------------|---------------------------------------------------------------------|
| 200    | OK                           | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta         | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado                | Token JWT inválido o ausente.                                        |
| 413    | Payload demasiado grande      | El archivo cargado excede el límite de tamaño.                      |
| 500    | Error interno del servidor   | Error inesperado en el servidor.                                    |

## Cómo usar la API PostSplit con SDKs

### Especificación de la API PostSplit

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

**Códigos de estado HTTP**

| Código | Significado                    | Descripción                                                                  |
|--------|--------------------------------|------------------------------------------------------------------------------|
| 200    | OK                             | El libro se dividió correctamente y la respuesta contiene la lista de archivos. |
| 400    | Solicitud incorrecta           | Parámetros faltantes o no válidos (por ejemplo, formato no admitido).       |
| 401    | No autorizado                  | Token JWT inválido o ausente.                                                 |
| 500    | Error interno del servidor     | Se produjo un error inesperado en el lado del servidor.                      |

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# Reemplace xxxxx1.xlsx y xxxxx2.xlsx por las rutas a sus archivos de Excel
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_hoja1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_hoja2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDKs de Aspose.Cells Cloud

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}