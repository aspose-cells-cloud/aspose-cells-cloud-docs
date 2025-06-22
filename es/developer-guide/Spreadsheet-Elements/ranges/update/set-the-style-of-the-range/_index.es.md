---
title: Establecer el estilo del rango
second_title: Aspose.Cells Cloud Documen
linktitle: Establecer estilo
type: docs
url: /es/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: Aspose.Cells Cloud REST API admite la configuración de estilos de rango en una hoja de cálculo Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 70
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Establecer el estilo del rango
---
## **Introducción**
Este ejemplo le permite configurar el estilo del rango usando Aspose.Cells Cloud API en sus aplicaciones. Puede usar nuestro REST API con cualquier lenguaje: .NET, Java, PHP, Ruby, Rails, Python, jQuery y muchos más.
## **API Información**

|**API**|**Tipo**|**Descripción**|**Enlace de recursos**|
|:- |:- |:- |:- |
|/celdas/{nombre}/hojasdetrabajo/{nombredehoja}/rangos/estilo|CORREO|Establecer el estilo de celda de un rango con nombre|[Estilo de rango de celdas de la hoja de trabajo posterior](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL Ejemplo**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"Range\": { \"ColumnCount\": 2, \"ColumnWidth\": 0, \"FirstColumn\": 1, \"FirstRow\": 1, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 2, \"RowHeight\": 0, \"Worksheet\": \"Sheet1\" }, \"Style\": { \"Font\": { \"DoubleSize\": 1, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true } }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **Fuente del SDK**
Los SDK de la nube Aspose.Cells se pueden descargar desde la siguiente página:[SDK disponibles](/cells/es/available-sdks/)
### **Ejemplos de SDK**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
