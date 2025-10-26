---
title: Aspose.Cells Cloud Web API - Elektronik Tabloları Koru
second_title: Developer Guide for Excel Protectio
ArticleTitle: Protect the Spreadsheet with passwor
linktitle: E-Tabloları Koru
type: docs
url: /tr/protect-spreadsheet/
keywords: Aspose.Cells Cloud Web API, password protection, encrypt spreadsheet, modify passwor
description: Bu API, Excel elektronik tablolarına çift katmanlı parola koruması uygulayarak şifreleme yoluyla güvenli erişim ve değişiklik sağlar
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, çift katmanlı parola koruması, elektronik tabloyu şifreleme, güvenli Exce
---
Excel elektronik tablolarına hem açma hem de değiştirme parolalarını destekleyerek parola koruması uygular.

## **Elektronik Tabloyu Koru API**

```http
PUT http://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|Korunacak elektronik tablo dosyasını yükleyin.|
|şifre|Sicim|Sorgu|E-tablo dosyası için şifreleme parolası.|
|Şifreyi değiştir|Sicim|Sorgu|E-tabloyu değiştirmek için şifre gerekiyor.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Korunan çalışma kitabının saklanacağı klasör yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyalarının saklanacağı depolama alanının adı.|
|bölge|Sicim|Sorgu|E-tablo için bölge ayarlarını tanımlar.|

## **Cevap**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Protect Spreadsheet API'i nerede kullanmalıyız?

E-tablonuzu şifre ile kilitlemeniz gerektiğinde API numarasını kullanabilirsiniz.

## Protect Spreadsheet API'i neden kullanmalısınız?

- Elektronik tablolarınızı şifreyle hızlıca kilitleyin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## Protect E-Tablosu API SDK'larla Nasıl Kullanılır

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/ProtectionController/ProtectSpreadsheet)REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için ayrıntılı bir programlama arayüzü sağlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, hücreler için elektronik tabloları minimum kodla korumanıza olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
