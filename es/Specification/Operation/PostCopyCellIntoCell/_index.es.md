﻿---
title: Publicar copiar celda en celda
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/operation/postcopycellintocell/
description: Copie datos de una celda de origen a una celda de destino en la hoja de trabajo
kwords: Excel, Office, hoja de cálculo, nube REST API, PostCopyCellIntoCell
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostCopyCellIntoCell" >}}
{{< blocks/products/cells/docs-title titlemsg="Copy data from a source cell to a destination cell in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API, método Http, descripción, referencia API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/cells/{destCellName}/copy,POST,Copiar datos de una celda de origen a una celda de destino en la hoja de trabajo.,<a href=\'https://apireference.aspose .cloud/cells/#/Cells/PostCopyCellIntoCell\'>PostCopyCellIntoCell</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Nombre del parámetro, tipo, descripción" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="nombre, cadena, el nombre del archivo." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="destCellName, cadena, el nombre de la celda de destino." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="nombre de la hoja, cadena, el nombre de la hoja de trabajo de destino." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Nombre del parámetro, tipo, descripción" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="hoja de trabajo, cadena, el nombre de la hoja de trabajo de origen." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="nombre de celda, cadena, el nombre de la celda de origen." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="fila, entero, índice de la fila de origen." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="columna, entero, índice de la columna de origen." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="carpeta, cadena, la carpeta donde se encuentra el archivo." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="nombre de almacenamiento, cadena, el nombre del almacenamiento donde se encuentra el archivo." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/CellsController/PostCopyCellIntoCell\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet1/cells/C1/copy?worksheet=Sheet2&cellname=A1&row=1&column=1&folder=TestData/In"
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostCopyCellIntoCell.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyCellIntoCell.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyCellIntoCell.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyCellIntoCell.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyCellIntoCell.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyCellIntoCell.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyCellIntoCell.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyCellIntoCell.rb" >}}
{{< /tab >}}

{{< /tabs >}}
