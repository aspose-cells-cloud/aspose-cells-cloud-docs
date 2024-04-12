---
title: Çalışma Sayfasından Hücre Stili Alma
type: docs
url: /tr/get-cell-style-from-a-worksheet/
weight: 10
---
Bu REST API, Excel dosyasındaki `style` hücresini almayı gösterir.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| hücreAdı| sicim| yol| Cell'in adı.|
| dosya| sicim| sorgu| Belgenin klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{

  "Style": {

    "Font": {

      "Color": {

        "A": 255,

        "R": 5,

        "G": 99,

        "B": 193

      },

      "DoubleSize": 11,

      "IsBold": false,

      "IsItalic": false,

      "IsStrikeout": false,

      "IsSubscript": false,

      "IsSuperscript": false,

      "Name": "Calibri",

      "Size": 11,

      "Underline": "Single"

    },

    "Name": null,

    "CultureCustom": "General",

    "Custom": "",

    "BackgroundColor": {

      "A": 0,

      "R": 0,

      "G": 0,

      "B": 0

    },

    "ForegroundColor": {

      "A": 0,

      "R": 0,

      "G": 0,

      "B": 0

    },

    "IsFormulaHidden": false,

    "IsDateTime": false,

    "IsTextWrapped": false,

    "IsGradient": false,

    "IsLocked": true,

    "IsPercent": false,

    "ShrinkToFit": false,

    "IndentLevel": 0,

    "Number": 0,

    "RotationAngle": 0,

    "Pattern": "None",

    "TextDirection": "Context",

    "VerticalAlignment": "Bottom",

    "HorizontalAlignment": "General",

    "BorderCollection": [

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "BottomBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "DiagonalDown"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "DiagonalUp"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "Horizontal"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "LeftBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "RightBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "TopBorder"

      },

      {

        "LineStyle": "None",

        "Color": {

          "A": 255,

          "R": 0,

          "G": 0,

          "B": 0

        },

        "BorderType": "Vertical"

      }

    ],

    "BackgroundThemeColor": null,

    "ForegroundThemeColor": null,

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 200,

  "Status": "OK"

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:



{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetCellStyleWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetCellStyleWorksheet-get-cell-style-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetCellStyle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_cell_style-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetCellStyleFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetCellStyleWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetCellStyleWorksheet-get-cell-style-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetCellStyleWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "c170ea420e8d58f7cf625b629f547351" >}}

{{< /tab >}}

{{< /tabs >}}
