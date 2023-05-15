---
title: Çalışma kitabını ve dahili nesneleri forma türlerine dışa aktarma
second_title: Aspose.Cells Cloud Documen
linktitle: İhracat
type: docs
url: /tr/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API, Excel dosyasının ve dahili nesnelerin dosya biçimi türlerine dışa aktarılmasını destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 31
---
 Orijinal olarak belirli bir biçimde bir Excel dosyası oluşturduysanız, örneğin[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , Ve[CSV'ler](https://docs.fileformat.com/spreadsheet/csv/) , sağladığı özel özelliklerden yararlanabilmeniz için bazen excel dosyasını başka bir biçime dönüştürmeyi faydalı bulabilirsiniz. Örneğin, bir excel dosyasını dışa aktarmak isteyebilirsiniz.[PDF](https://docs.fileformat.com/pdf/) içeriğinizi yetkisiz değişikliklerden korumak ve aynı anda okumayı ve paylaşmayı kolaylaştırmak için.

 Excel nesne dışa aktarımı karmaşık bir işlemdir. Birçok faktör karmaşıklığa katkıda bulunur ve bu nedenle ihracat sürecinde dikkate alınmalıdır. Excel nesnesini kesin bir profesyonel kalitede tek bir format dosyasına dışa aktarma yeteneği, Aspose.Cells Cloud'un en önemli özelliğidir.

 Excel dosyasından dışa aktarılan çalışma kitabı, grafik, şekil ve resim için mükemmel çalışır. Şu biçimleri dışa aktarabilirsiniz:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV'ler](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) . Yalnızca dışa aktarma biçimleri:[PDF](https://docs.fileformat.com/pdf/), [ÖTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [SAYILAR](https://docs.fileformat.com/spreadsheet/numbers/), [YEMEKLER](https://docs.fileformat.com/spreadsheet/fods/).

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk bölümü veri dosyasını içerir ve ikincisi kaydetme seçeneklerini içerir.

REST API `export` çalışma kitabı ve dahili nesneleri farklı biçim dosyasına.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| dosya| dosya| form verisi| Yüklenecek dosya|
| Nesne türü| sicim| sorgu|nesne türü (çalışma kitabı/çalışma sayfası/grafik/şekil/resim/liste nesnesi/olenesne)|
| biçim| sicim| sorgu|[Dosya formatı](/cells/tr/supported-file-formats/)  |
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi


 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export.php" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


Aşağıdaki makaleler her bir API'i ayrıntılı olarak açıklar ve her API'in cURL ve SDK Örneklerini içerir:


1. [Excel grafiğini farklı dosya biçimine aktar](/cells/tr/export/excel-chart-to-different-formats/)
2. [Excel liste nesnesini farklı dosya biçimine aktar](/cells/tr/export/excel-listobject-to-different-formats/)
3. [Excel ole nesnesini farklı dosya biçimine aktar](/cells/tr/export/excel-ole-object/)
4. [Excel resmini farklı dosya formatına aktar](/cells/tr/export/excel-picture-to-different-formats/)
5. [Excel şeklini farklı dosya biçimine aktar](/cells/tr/export/excel-shape-to-different-formats/)
6. [Excel çalışma kitabını farklı dosya biçimine aktar](/cells/tr/export/excel-to-different-formats/)
7. [Excel çalışma sayfasını farklı dosya biçimine aktar](/cells/tr/export/excel-worksheet-to-different-formats//)
