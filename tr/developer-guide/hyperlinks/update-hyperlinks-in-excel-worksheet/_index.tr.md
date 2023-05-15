---
title: güncelleme
type: docs
url: /tr/hyperlinks/update/
aliases: [/update-hyperlinks-in-excel-worksheet/]
keywords: Update a hyperlink in an Excel worksheet
description: Aspose.Cells Cloud REST API, bir Excel çalışma sayfasındaki köprüyü güncellemeyi destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 30
---
Bu REST API, bir Excel çalışma sayfasında dizine göre `update worksheet hyperlink`'i gösterir.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| hyperlinkIndex| tamsayı| yol| Köprünün dizini.|
| köprü|| vücut| Köprü nesnesi|
| dosya| sicim| sorgu| Belge klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Hypelinks/PostWorksheetHyperlink) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v  "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"Hyperlink\": { \"Address\": \"https://www.msnbc.com/\", \"Area\": { \"EndColumn\": 6, \"EndRow\": 1, \"StartColumn\": 6, \"StartRow\": 1 }, \"ScreenTip\": null, \"TextToDisplay\": \"https://www.msnbc.com/\", \"link\": { \"Href\": \"/test.xlsx/worksheets/Sheet1/hyperlinks/4\", \"Rel\": \"self\", \"Title\": null, \"Type\": null } }, \"Code\": 200, \"Status\": \"OK\"}"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "Code": 200,

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Hyperlinks-UpdateHyperlinkWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-hyperlinks-UpdateHyperlinkWorksheet-update-hyperlink-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Hyperlinks-PostWorkSheetHyperlink-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Hyperlinks-update_worksheet_hyperlink_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateHyperlinksInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-hyperlinks-UpdateHyperlinkWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-hyperlinks-UpdateHyperlinkWorksheet-update-hyperlink-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-hyperlinks-UpdateHyperlinkWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "952ad1f5ec954099efe4245fa4153605" >}}

{{< /tab >}}

{{< /tabs >}}
