---
title: Excel Dosyasını Farklı Biçime Dönüştür
second_title: Aspose.Cells Cloud Documen
linktitle: E-tabloyu dönüştür
type: docs
url: /tr/convert-a-spread-file-to-different-formats/
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API, excel dosyalarının çeşitli biçim dosyalarına dönüştürülmesini destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir.
weight: 10
kwords: Excel, Office Bulut, REST API, E-tablo, PDF, CSV, Json, Markdown, Dönüştür Excel
---
Bu REST API, `convert`'e Excel dosyasını farklı bir formata gösterir. Farklı formatları destekler. Ayrıca dönüştürmeden önce sayfa düzenini ve kaydetme seçeneklerini ayarlayabilir.

**İstek Gövde Parametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
|[ÇalışmaKitabıSeçenekleriniDönüştür](/cells/tr/convert-workbook-options/)| nesne| Çalışma Kitabı Seçeneklerini Dönüştür.|

**Cevap**

[Dosya bilgisi](/cells/tr/file-info/)

## DİNLENME API

|**API**|**Tip**|**Tanım**|**Swagger Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/dönüştür|POSTALAMAK|Çalışma kitabını istek içeriğinden bir biçime dönüştürür|[PostConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook)|

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web servislerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "filename",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
