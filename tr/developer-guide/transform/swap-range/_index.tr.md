---
title: Aspose.Cells Cloud Web API - E-Tablodaki Takas Aralığı
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: Takas Aralığı
type: docs
url: /tr/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: Excel API için Aralık Değiştirme, bir Excel dosyasındaki herhangi iki sütunu, satırı, aralığı veya tek tek hücreyi değiştirmek için güçlü bir araç sağlar. Bu API, kullanıcıların tablolarını verimli bir şekilde yeniden düzenlemelerine olanak tanır ve orijinal veri biçimlendirmesinin korunmasını ve mevcut tüm formüllerin doğru şekilde çalışmaya devam etmesini sağlar. Bu API'den yararlanarak kullanıcılar veri işleme görevlerini kolaylaştırabilir ve elektronik tablolarının bütünlüğünü koruyabilirler.
weight: 100
kwords: Excel, Office Bulut, REST, PDF, CSV, Json, Markdown
---
Excel dosyasındaki herhangi iki sütun, satır, aralık veya ayrı hücreler arasında veri alışverişi yapın.

## **Takas Aralığı API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|E-tablo dosyasını yükleyin.|
|çalışma sayfası1|Sicim|Sorgu|Değişim veri alanının kaynağı olan çalışma sayfasını belirtin.|
|aralık1|Sicim|Sorgu|Değişim verilerinin kaynağını belirtin.|
|çalışma sayfası2|Sicim|Sorgu|Değişim veri alanının hedefi olan çalışma sayfasını belirtin.|
|aralık2|Sicim|Sorgu|Değişim verilerinin hedefini belirtin.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyası Depolama Adı.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için şifre.|

### **Cevap**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Swap Range API'i nerede kullanmalıyız?

Bir elektronik tabloda aralık verilerini değiştirmeniz gerektiğinde API'i kullanabilirsiniz.

## Neden API Swap Aralığını kullanmalısınız?

- Excel elektronik tablosunda aralık verilerini hızla değiştirin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## API Swap Aralığı SDK'larla Nasıl Kullanılır

### Takas Aralığı API Spesifikasyonu

 The[Takas Aralığı API Spesifikasyonu](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak kısa kodla aralığı değiştirmenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
