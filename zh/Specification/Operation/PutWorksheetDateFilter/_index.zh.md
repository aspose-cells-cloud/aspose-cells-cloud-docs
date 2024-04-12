---
title: 放置工作表日期过滤器
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/operation/putworksheetdatefilter/
description: 在工作表中应用日期过滤器
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetDateFilter" >}}
{{< blocks/products/cells/docs-title titlemsg="Apply a date filter in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,描述,API参考" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter,PUT,在工作表中应用日期过滤器。,<a href=\'https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter \'>PutWorksheetDateFilter</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="参数名称、类型、描述" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="名称，字符串，文件名。" >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName,字符串,工作表名称。" >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="参数名称、类型、描述" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="range,字符串,表示指定自动筛选应用的范围。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="fieldIndex,integer,要作为过滤器基础的字段的整数偏移量（从列表左侧开始；最左侧的字段是字段 0）。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dateTimeGroupingType,字符串,指定如何对日期时间值（日、小时、分钟、月、秒、年）进行分组。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="年，整数，年份。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="月份，整数，月份。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="天，整数，天。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="小时，整数，小时。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="分钟，整数，分钟。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="第二个，整数，第二个。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="matchBlanks,boolean,匹配列表中的所有空白单元格。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="刷新，布尔值，刷新自动过滤器以隐藏或取消隐藏行。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="文件夹，字符串，文件所在的文件夹。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,文件所在的存储名称。" >}} 
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
