---
title: Excel dosyasını başka bir biçime alır
second_title: Aspose.Cells Cloud Documen
linktitle: Excel'i edinin
type: docs
url: /tr/get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API, excel dosyalarını çeşitli biçim dosyalarına dönüştürmeyi destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir.
weight: 10
kwords: Excel, Office Bulut, REST API, E-tablo, PDF, CSV, Json, Markdown, Excel dosyasını diğer biçimlere dönüştürür
---
Bu REST API, `get` excel dosyasının farklı formatta dosya olduğunu gösterir.

**Sorgu Parametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
|biçim|sicim|Dosya biçimi: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg vb.|
|şifre|sicim|Excel dosyasını açmak için gereken şifre.|
|OtomatikUyumludur|sicim|Bu çalışma kitabında satır ve sütun genişliğini otomatik olarak ayarlar. Varsayılan değer false'tur.|
|sadeceTabloKaydet|sicim|doğru/yanlış|
|çıkış yolu|sicim| Sonucun kaydedileceği yol. Tek bir dosyaysa, `outPath` hem dosya adını hem de uzantıyı kapsamalıdır. Birden fazla dosya olması durumunda, `outPath` yalnızca klasörü içermelidir.|
|outDepolamaAdı|sicim| Kaydedilen dosyanın bulunduğu depolama adı.|
|checkExcelKısıtlama|bool| Kullanıcı hücrelerle ilgili nesneleri değiştirdiğinde Excel dosyasının kısıtlamasını kontrol edin.|
|bölge|sicim| Çalışma kitabı için bölgesel ayarlar.|
|sayfaGenişSayfaBaşınaSığdır|bool| Sayfa genişliği çalışma kağıdına sığar.|
|sayfaUzunSayfaBaşınaSığdır|bool| Sayfanın uzunluğu çalışma kağıdına sığacak kadar uzun.|
|birSayfa/Sayfa|bool| PDF formatına dönüştürülürken her sayfada bir sayfa olacak şekilde.|
|dosya|sicim|Orijinal çalışma kitabı klasörü.|
|depolamaAdı|sicim|Dosyanın bulunduğu depolama adı.|

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Swagger Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/{isim}|ELDE ETMEK|Çalışma kitabını başka bir biçime aktarır.|[ÇalışmaKitabınıAl](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web servislerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
