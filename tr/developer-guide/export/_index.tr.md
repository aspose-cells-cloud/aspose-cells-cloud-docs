---
title: Çalışma kitabını ve dahili nesneleri çeşitli formatlara aktarın
second_title: Aspose.Cells Cloud Documen
linktitle: İhracat
type: docs
url: /tr/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API, Excel dosyasının ve dahili nesnelerin çeşitli format dosyalarına aktarılmasını destekler. SDK çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 31
---
 Başlangıçta belirli bir formatta Excel dosyası oluşturduysanız, örneğin[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , Ve[CSV](https://docs.fileformat.com/spreadsheet/csv/) , bazen excel dosyasını başka bir formata dönüştürmeyi faydalı bulabilirsiniz, böylece sağladığı özel özelliklerden yararlanabilirsiniz. Örneğin, bir excel dosyasını dışa aktarmak isteyebilirsiniz.[PDF](https://docs.fileformat.com/pdf/) İçeriğinizi yetkisiz değişikliklere karşı korumak ve aynı anda okunmasını ve paylaşılmasını kolaylaştırmak için.

 Excel nesne dışa aktarımı karmaşık bir işlemdir. Birçok faktör karmaşıklığa katkıda bulunur ve bu nedenle ihracat sürecinde dikkate alınmalıdır. Excel nesnesini kesin bir profesyonel kalitede tek formatlı bir dosyaya aktarma yeteneği, Aspose.Cells Cloud'un en önemli özelliğidir.

 Excel dosyasından dışa aktarılan çalışma kitabı, grafik, şekil ve resim için mükemmel çalışır. Formatları dışa aktarabilirsiniz:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) . Yalnızca dışa aktarma biçimleri:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DMF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMARALAR](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk kısmı veri dosyasını, ikincisi ise kaydetme seçeneklerini içerir.

REST API `export` çalışma kitabını ve dahili nesneleri farklı formattaki dosyalara dönüştürün.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| dosya| dosya| form verisi| Yüklenecek dosya|
| Nesne türü| sicim| sorgu|nesne türü (çalışma kitabı/çalışma sayfası/grafik/şekil/resim/listobject/oleobject)|
| biçim| sicim| sorgu|[Dosya formatı](/cells/tr/supported-file-formats/)  |
 
[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.
 
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


 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export.php" >}}


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

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


Aşağıdaki makaleler her API'i ayrıntılı olarak açıklamaktadır ve her API'in cURL ve SDK Örneklerini içermektedir:


1. [Excel grafiğini farklı dosya formatına aktar](/cells/tr/export/excel-chart-to-different-formats/)
2. [Excel liste nesnesini farklı dosya formatına aktar](/cells/tr/export/excel-listobject-to-different-formats/)
3. [Excel ole nesnesini farklı dosya formatına aktar](/cells/tr/export/excel-ole-object/)
4. [Excel resmini farklı dosya formatına aktar](/cells/tr/export/excel-picture-to-different-formats/)
5. [Excel şeklini farklı dosya formatına aktar](/cells/tr/export/excel-shape-to-different-formats/)
6. [Excel çalışma kitabını farklı dosya biçimine aktar](/cells/tr/export/excel-to-different-formats/)
7. [Excel çalışma sayfasını farklı dosya biçimine aktar](/cells/tr/export/excel-worksheet-to-different-formats//)
