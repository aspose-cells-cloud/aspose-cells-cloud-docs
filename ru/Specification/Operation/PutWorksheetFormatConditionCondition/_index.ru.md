﻿---
title: PutWorksheetFormatConditionConditio
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/specification/operation/putworksheetformatconditioncondition/
description: Добавьте условие для условия формата на листе.
kwords: Excel, Office, электронная таблица, Cloud REST API, PutWorksheetFormatConditionCondition
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetFormatConditionCondition" >}}
{{< blocks/products/cells/docs-title titlemsg="Add a condition for the format condition in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Описание,ссылка API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition,PUT,Добавьте условие для условия формата на листе.,<a href=\'https://apireference.aspose.cloud/ cell/#/ConditionalFormattings/PutWorksheetFormatConditionCondition\'>PutWorksheetFormatConditionCondition</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Имя параметра, тип, описание" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="имя, строка, имя файла." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="имя_листа,строка,имя листа." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="index,integer,Получает элемент условного форматирования по указанному индексу." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Имя параметра, тип, описание" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="тип, строка, тип условия форматирования (CellValue/Expression/ColorScale/DataBar/IconSet/Top10/UniqueValues/DuplateValues/ContainsText/NotContainsText/BeginsWith/EndsWith/ContainsBlanks/NotContainsBlanks/ContainsErrors/NotContainsErrors/TimePeriod/AboveAverage)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="operatorType,string, представляет тип оператора условного формата и проверки данных (Between/Equal/GreaterThan/GreaterOrEqual/LessThan/None/NotBetween/NotEqual)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Formula1,string,Значение или выражение, связанное с условным форматированием." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Formula2,string,Значение или выражение, связанное с условным форматированием." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="папка,строка,Папка, в которой находится файл." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="StorageName,string,Имя хранилища, в котором находится файл." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ConditionalFormattingsController/PutWorksheetFormatConditionCondition\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Between&formula1=v1&formula2=v2&folder=TestData/In"
    -X PUT 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetFormatConditionCondition.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFormatConditionCondition.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFormatConditionCondition.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFormatConditionCondition.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFormatConditionCondition.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFormatConditionCondition.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFormatConditionCondition.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFormatConditionCondition.rb" >}}
{{< /tab >}}

{{< /tabs >}}
