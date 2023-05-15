---
title: Çalışma Sayfasından Hücre Verilerini Alma
type: docs
url: /tr/get-cell-data-from-a-worksheet/
weight: 10
---
Bu REST API, `cellOrMethodName` parametresi hücre adı olduğunda bir Excel dosyasında `cell` alındığını gösterir.

- **cURL Örnek**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X GET "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=xxxx&client_secret=xxxx" -H "Content-Type: application/json" -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "Cell": {

    "Name": "A3",

    "Row": 2,

    "Column": 0,

    "Value": "Statistical",

    "Type": "IsString",

    "IsFormula": false,

    "IsMerged": false,

    "IsArrayHeader": false,

    "IsInArray": false,

    "IsErrorValue": false,

    "IsInTable": false,

    "IsStyleSet": false,

    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",

    "Style": {

      "link": {

        "Href": "/style",

        "Rel": "self"

      }

    },

    "link": {

      "Href": "http://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",

      "Rel": "self"

    }

  },

  "Code": "200",

  "Status": "OK"

} 

```

{{< /tab >}}

{{< /tabs >}}

- **Bulut SDK Ailesi**

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetCellWorksheet-get-cell-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetCell-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-read_cell_data_by_cell_name-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetCellFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetCellWorksheet-get-cell-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "a4d1011129858e5237f4dc8c949a1be6" >}}

{{< /tab >}}

{{< /tabs >}}
