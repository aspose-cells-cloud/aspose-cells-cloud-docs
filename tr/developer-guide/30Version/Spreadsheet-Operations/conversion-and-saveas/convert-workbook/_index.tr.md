---
title: "Bir Excel Dosyasını Farklı Biçimlere Dönüştürme"
second_title: "Belge"
linktype: "Döküman"
url: /tr/convert-a-spread-file-to-different-formats/
keywords: "Excel dönüştürme, spreadsheet dönüştürme, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, dosya biçimi dönüştürme"
description: "Aspose.Cells Cloud REST API’sini kullanarak Excel çalışma kitaplarını PDF, CSV, JSON ve Markdown gibi çeşitli biçimlere dönüştürün. API, C#, Java, Python ve diğerleri gibi diller için birden fazla SDK’yi destekler."
weight: 10
ArticleTitle: "Bir Excel Dosyasını Farklı Biçimlere Dönüştürme – Aspose.Cells Cloud API Kılavuzu"
---

Bu REST API, bir Excel dosyasını farklı bir forma dönüştürür. Geniş bir çıktı formatı yelpazesi sunar ve dönüştürme işleminden önce sayfa ayarlarını ve kaydetme seçeneklerini belirlemenize olanak tanır.

## PostConvertWorkBook API

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

Bu API’yi kullanmadan önce geçerli bir JWT belirteciniz olduğundan ve programlama diliniz için uygun Aspose.Cells Cloud SDK’sini yüklediğinizden emin olun.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

## SDK’lar ile PostConvertWorkBook API’yi Nasıl Kullanılır?

### PostConvertWorkBook API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca ulaşmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "dosya_adı",
  "FileSize": 12345,
  "FileContent": "Dosya İçeriği: base64_kodlanmış_dize"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK, düşük seviye detayları soyutlayarak projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

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
---