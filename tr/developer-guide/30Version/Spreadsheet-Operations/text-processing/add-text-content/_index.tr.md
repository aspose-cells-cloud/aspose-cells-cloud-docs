---
title: "Excel'e Metin Ekle: Hızlı ve Verimli Şekilde Veri Ekleme için Elektronik Tablo Web API'si"
second_title: "Belge"
linktype: "Metin Ekle"
type: docs
url: /excel-add-text/
keywords: "Excel, Aspose.Cells, Metin Ekle, Elektronik Tablo API'si, REST API, Ofis Bulutu, Metin Ekleme, Excel API"
description: "Aspose.Cells Cloud API aracılığıyla bir Excel elektronik tablosunda belirli bir konuma metin ekler."
weight: 100
---

Bir elektronik tabloda belirli bir konuma metin içeriği ekler. Bu işlem, eklenecek metni ve ekleme konumunu tanımlayan bir nesne gerektirir.

## **Excel API: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### **Fonksiyon Açıklaması**

Bu yöntem, yeni metni güvenli bir şekilde seçilen hücrelere ekler; birden fazla ekleme modunu ve biçimlendirme işlemini destekler.

- **Seçili hücrelerin başına metin ekleme**  
  Tüm seçili hücrelerin başına metin ekler ve veri girişi tutarlılığını sağlar. Ürün kodları, kategoriler veya önekler gibi ortak tanımlayıcılar veya etiketler eklemek için idealdir.

- **Belirli metnin öncesine veya sonrasına karakter ekleme**  
  Seçili hücrelerdeki hedef metnin öncesine veya sonrasına karakter yerleştirerek yapılandırılmış ve düzenli içerik oluşturma imkanı sunar.

- **Seçili her hücrenin sonuna aynı metni ekleme**  
  Birden fazla hücrenin sonuna tek bir işlemde aynı metni ekler; veri girişi basitleştirir ve birbirine benzer görünüm sağlar.

- **Belirli sayıda karakterden önce veya sonra metin ekleme**  
  Hedef aralıktaki her hücrenin başına veya sonundan belirli bir sayıda karakterden sonra metin ekler. Tipik kullanım durumları arasında kodları, zaman damgalarını veya özel ayraçları biçimlendirme yer alır.

### **İstek Parametresi**

| Parametre Adı | Tür  | Konum | Açıklama                                                                 |
| -------------- | ---- | ----- | --------------------------------------------------------------------------- |
| addTextOptions | Sınıf | Gövde | Eklenecek metin içeriğini ve metnin ekleneceği konumu belirtir. |

### **Yanıt**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırlarını aşıyor. |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |

## PostAddTextContent API'sini SDK'lar ile Nasıl Kullanılır?

### PostAddTextContent API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, geliştirmeyi hızlandırmak için en verimli yoldur. Bir SDK, düşük seviye detayları işleyerek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}