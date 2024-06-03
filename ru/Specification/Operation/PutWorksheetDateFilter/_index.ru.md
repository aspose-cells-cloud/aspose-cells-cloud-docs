---
title: PutWorksheetDateFilte
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/specification/operation/putworksheetdatefilter/
description: Применение фильтра даты на листе
kwords: Excel, Office, электронная таблица, Cloud REST API, PutWorksheetDateFilter
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetDateFilter" >}}
{{< blocks/products/cells/docs-title titlemsg="Apply a date filter in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Описание,ссылка API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter,PUT,Применить фильтр даты на листе.,<a href=\'https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter \'>PutWorksheetDateFilter</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Имя параметра, тип, описание" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="имя, строка, имя файла." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="имя_листа,строка,имя листа." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Имя параметра, тип, описание" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="range,string,Представляет диапазон, к которому применяется указанный автофильтр." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="fieldIndex,integer,целочисленное смещение поля, на котором вы хотите основывать фильтр (слева от списка; самое левое поле — это поле 0)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dateTimeGroupingType,string, Указывает, как группировать значения dateTime (день, час, минута, месяц, секунда, год)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="год, целое число, год." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="месяц, целое число, Месяц." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="день, целое число, день." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="час, целое число, час." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="минута, целое число, минута." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="второй, целое число, Второе." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="matchBlanks,boolean,Сопоставить все пустые ячейки в списке." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="обновить,логическое значение,Обновить автоматические фильтры, чтобы скрыть или отобразить строки." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="папка,строка,Папка, в которой находится файл." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="StorageName,string,Имя хранилища, в котором находится файл." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/AutoFilterController/PutWorksheetDateFilter\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&matchBlanks=false&refresh=true&folder=TestData/In"
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
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetDateFilter.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}
{{< /tab >}}

{{< /tabs >}}
