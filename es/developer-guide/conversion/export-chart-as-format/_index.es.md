---
title: Aspose.Cells Cloud Web API - Exportar un gráfico de hoja de cálculo como un archivo de formato
second_title: Documen
ArticleTitle: Export a Spreadsheet Chart as a Format fil
linktitle: Gráfico de exportación como formato
type: docs
url: /es/export-chart-as-format/
keywords: Export Chart, Aspose.Cells Cloud Web API, Spreadsheet Conversion, PDF Export, Image Export, REST, Excel, CSV, JSO
description: Convierte de manera eficiente gráficos de hojas de cálculo almacenadas en la nube a formatos específicos como PDF o imagen directamente sin descargarlos
weight: 100
kwords: Exportar gráfico, REST, conversión de hoja de cálculo, PDF, CSV, JSON, Markdown, Excel, formato de imagen
---
Exporte una hoja de cálculo en la nube/gráfico Excel a otro formato de archivo con Aspose.Cells Cloud Web API.

## **Exportar gráfico en formato API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody| Descripción|
|:- |:- |:- |:- |
| nombre| Cadena| Camino| (Obligatorio) El nombre del archivo del libro de trabajo que se recuperará.|
| hoja de trabajo| Cadena| Camino| Nombre de la hoja de trabajo|
| Índice de gráficos| Entero| Camino| Índice del gráfico|
| formato| Cadena| Consulta| (Obligatorio) El formato de salida deseado (por ejemplo, "png", "pdf", "svg").|
| carpeta| Cadena| Consulta| (Opcional) La ruta de la carpeta donde se almacena el libro de trabajo; el valor predeterminado es nulo.|
| nombreDeAlmacenamiento| Cadena| Consulta|(Opcional) El nombre del almacenamiento si se utiliza almacenamiento en la nube personalizado; utilice el almacenamiento predeterminado si se omite.|
| Ruta de salida| Cadena| Consulta| (Opcional) La ruta de la carpeta donde se almacena el libro de trabajo; el valor predeterminado es nulo.|
|nombreAlmacenamientoExterno| Cadena| Consulta| Nombre de almacenamiento del archivo de salida.|
| Ubicación de fuentes| Cadena| Consulta| Utilice fuentes personalizadas.|
| región| Cadena| Consulta| La configuración de la región de la hoja de cálculo.|
| contraseña| Cadena| Consulta| La contraseña para abrir el archivo de hoja de cálculo.|

### **Respuesta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Códigos de error

- **400 Solicitud incorrecta**: URI de nube Apose.Cells no válido API.
- **401 No autorizado**Token de acceso no válido. O ID de cliente y secreto no válidos.
- **404 No encontrado**:El archivo de hoja de cálculo no es accesible.
- **Error de servidor 500**:La hoja de cálculo ha encontrado una anomalía al obtener los datos de cálculo.

## ¿Por qué debería utilizar el gráfico de hoja de cálculo de exportación con formato API?

- Puede convertir archivos en la nube a diferentes formatos en cualquier momento y en cualquier lugar.
- El desarrollo se puede completar rápidamente a través del SDK existente.

## ¿Cómo utilizar el gráfico de hoja de cálculo de exportación como formato API con SDK?

### Exportar gráfico como formato API Especificación

 El[Exportar gráfico como formato API Especificación](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat) define una interfaz de programación de acceso público que le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la forma más rápida de desarrollar, ya que abstrae los detalles de bajo nivel y permite exportar los datos de un gráfico de una hoja de cálculo a un archivo de formato con código corto.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
