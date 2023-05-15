---
title: Excel çalışma sayfasından bir otomatik şekil alın
second_title: Aspose.Cells Cloud Documen
linktitle: Otomatik Şekillendirme
type: docs
url: /tr/shapes/get-autoshape/
aliases: [/get-autoshape-from-a-worksheet/]
keywords: Get autoshape to different format from an Excel worksheet
description: Aspose.Cells Cloud REST API, bir Excel Çalışma Sayfasından farklı biçime otomatik şekil almayı destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 10
---
Bu REST API, `get autoshape info`'i gösterir.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoshapes/{autoshapeNumber}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| otomatik şekil numarası| tamsayı| yol| Otomatik şekil numarası.|
| biçim| sicim| sorgu| Dışa aktarılan biçim.|
| dosya| sicim| sorgu| Belge klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Autoshapes/GetWorksheetAutoshape) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/autoshapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "AutoShape": {

    "Name": "AutoShape 2",

    "MsoDrawingType": "CellsDrawing",

    "AutoShapeType": "FlowChartDocument",

    "Placement": "FreeFloating",

    "UpperLeftRow": 7,

    "Top": 6,

    "UpperLeftColumn": 5,

    "Left": 0,

    "LowerRightRow": 10,

    "Bottom": 0,

    "LowerRightColumn": 11,

    "Right": 0,

    "Width": 102,

    "Height": 45,

    "X": 85,

    "Y": 129,

    "RotationAngle": 0.0,

    "HtmlText": "<Font Style=\"FONT-FAMILY: Tahoma;FONT-SIZE: 10pt;COLOR: #000000;TEXT-ALIGN: center;\">Body</Font>",

    "Text": "Body",

    "AlternativeText": "",

    "TextHorizontalAlignment": "Center",

    "TextHorizontalOverflow": "Overflow",

    "TextOrientationType": "NoRotation",

    "TextVerticalAlignment": "Center",

    "TextVerticalOverflow": "Overflow",

    "IsGroup": false,

    "IsHidden": false,

    "IsLockAspectRatio": false,

    "IsLocked": false,

    "IsPrintable": false,

    "IsTextWrapped": false,

    "IsWordArt": false,

    "ZOrderPosition": 1,

    "link": {

      "Href": "http://api.aspose.cloud/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1",

      "Rel": "self"

    }

  },

  "Code": "200",

  "Status": "OK"

}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-GetAutoshape-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-GetAutoshape-get-auto-shape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-GetWorksheetAutoshape-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-get_autoshape_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetAutoshapeFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-GetAutoshape-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-GetAutoshape-get-auto-shape.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-GetAutoshape-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "de52ec3211922aa795d7dd11ef0bd755" >}}

{{< /tab >}}

{{< /tabs >}}
