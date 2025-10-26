---
title: Resmi Excel Çalışma Sayfasına Aktar
second_title: Documen
linktitle: Resmi içe aktar
type: docs
url: /tr/import-picture-into-excel-worksheet/
aliases: [/import-picture-into-worksheet/,/import-data/picture/, /import/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API, Excel dosyalarına resim aktarmayı destekler. SDK, Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift gibi çeşitli geliştirme dillerini destekler.
weight: 19
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Resmi Excel Çalışma Sayfasına Aktar
---
Bu REST API `import picture data`'i Excel çalışma sayfasına dönüştürün.

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk kısmı ImportPictureOption verilerini, ikinci kısmı ise bir veri dosyasını içerir.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Önemli parametreler aşağıdaki tabloda açıklanmıştır:

**Resimİçe AktarmaSeçeneği**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
| Sol Üst Satır| int||
| Sol Üst Sütun| int||
| AltSağSatır| int||
| AltSağSütun| int||
| Dosya adı| sicim||
| Veri| Sicim||
|Hedef Çalışma Sayfası| sicim| hedef çalışma sayfası adı.|
| IsInsert| sicim| doğru/yanlış.|
| Veri Türünü İçe Aktar| sicim|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Kaynak| Dosya Kaynağı| BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.|

**Örnek**

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

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
