---
title: PutWorksheetChar
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/specification/operation/putworksheetchart/
description: Добавьте новую диаграмму на лист
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetChart" >}}
{{< blocks/products/cells/docs-title titlemsg="Add a new chart in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Описание,ссылка API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/charts,PUT,Добавьте новую диаграмму на лист.,<a href=\'https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChart\'> PutWorksheetChart</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Имя параметра, тип, описание" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="имя, строка, имя файла." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="имя_листа,строка,имя листа." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Имя параметра, тип, описание" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="chartType,string,Тип диаграммы, см. свойство Type в ресурсе диаграммы." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="UpperLeftRow,integer,Верхняя левая строка новой диаграммы." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="UpperLeftColumn,integer,Верхний левый столбец новой диаграммы." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="LowerRightRow,integer,Нижняя левая строка новой диаграммы." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="LowerRightColumn,integer,Нижний левый столбец новой диаграммы." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="область,строка,Укажите значения, на основе которых будет построен ряд данных." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns=" isVertical,boolean,Укажите, следует ли отображать ряд из диапазона значений ячеек по строке или по столбцу." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="CategoryData,string,Получите или установите диапазон значений оси категорий. Это может быть диапазон ячеек (например, «D1:E10»)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoGetSerialName,boolean,Укажите, следует ли автоматически обновлять серийное имя." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="title,string,Укажите имя заголовка диаграммы." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="папка,строка,Папка, в которой находится файл." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabels,boolean, Представляет поведение отображения значений меток данных указанной диаграммы. True, чтобы отобразить значения, False, чтобы скрыть их." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabelsPosition,string, Представляет положение метки данных (Center/InsideBase/InsideEnd/OutsideEnd/Above/Below/Left/Right/BestFit/Moved)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="PivotTableSheet,string,Источником являются данные сводной таблицы. Если PivotSource не пуст, диаграмма является сводной диаграммой." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="PivotTableName,string,Имя сводной таблицы." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="StorageName,string,Имя хранилища, в котором находится файл." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ChartsController/PutWorksheetChart\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet4/charts?chartType=Pie&upperLeftRow=5&upperLeftColumn=5&lowerRightRow=10&lowerRightColumn=10&area=C7:D11&isVertical=true&title=Aspose Chart&folder=TestData/In"
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
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetChart.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetChart.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetChart.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetChart.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetChart.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetChart.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetChart.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetChart.rb" >}}
{{< /tab >}}

{{< /tabs >}}
