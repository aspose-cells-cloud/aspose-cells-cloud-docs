---
title: Resmi Excel Çalışma Sayfasına Aktar
second_title: Aspose.Cells Cloud Documen
linktitle: Resmi içe aktar
type: docs
url: /tr/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API, resmin Excel dosyalarına aktarılmasını destekler. SDK çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 19
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Resmi Excel Çalışma Sayfasına Aktar
---
Bu REST API `import picture data`'i Excel çalışma sayfasına dönüştürün.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk kısmı ImportPictureOption verilerini, ikincisi ise bir veri dosyasını içerir.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```


Önemli parametreler aşağıdaki tabloda açıklanmıştır:


**Resim İçe Aktarma Seçeneği**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
| ÜstSolSatır| int||
| ÜstSol Sütun| int||
| AltSağSatır| int||
| Alt Sağ Sütun| int||
| Dosya adı| sicim||
| Veri| Sicim||
| HedefÇalışma Sayfası| sicim| hedef çalışma sayfası adı.|
| Ekle| sicim| doğru yanlış.|
| Veri Türü İçe Aktarma| sicim|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Kaynak| Dosya Kaynağı| BatchData parametresi null olduğunda veri dosyası konumunu gösterir.|


**Örnek**


## Bulut SDK Ailesi

 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}



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


{{< /tab >}}

{{< /tabs >}}

