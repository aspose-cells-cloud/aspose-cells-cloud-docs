---
title: Reparar el archivo Excel
second_title: Documen
type: docs
linktitle: Reparar el archivo Excel
url: /es/repair-excel-files/
keywords: Repair Excel, ODS, WPS, and so on files
description: Repara los archivos Excel usando Aspose.Cells Cloud REST API. El API admite múltiples lenguajes de desarrollo, incluidos Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift para una rápida integración en tus proyectos.
weight: 39
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Reparación
---
Este REST API indica los archivos `repair` Excel.

- Reparar XLS, XLSX, XLSM, XLSB, ODS, etc.
- Admite múltiples archivos.

Aspose.Cells Cloud Excel Repair recupera datos de archivos corruptos Excel en línea sin necesidad de instalación. Los archivos corruptos Excel pueden ser un problema, ya que no podrás abrirlos. Puedes probar la app Aspose.Cells Cloud Excel Repair para recuperar datos de archivos corruptos Excel.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/repair

```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| archivo| archivo| datos del formulario| Archivo para cargar|
| formato| cadena| consulta| Formato de salida, el valor predeterminado es nulo, el formato de salida es igual al formato del archivo de entrada.|

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/repair" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash

{
    "Files":
    [
        {
            "Filename":"xxxx1.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        {
            "Filename":"xxxx2.xlsx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}

```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}
