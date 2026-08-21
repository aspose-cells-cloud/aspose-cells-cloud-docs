---
title: "Aspose.Cells Cloud Değiştirme Web API’si – Uzak Elektronik Tablo Aralığında Metni Güncelleştir"
second_title: "Belge"
ArticleTitle: "Bulut Excel Dosyalarında Toplu Aralık Metni Değiştirme – Bul ve Değiştir API’si"
linktitle: "Uzak Aralık İçeriğini Değiştir"
type: docs
url: /tr/replace-content-in-remote-range/
keywords: "uzak excel aralığında metin değiştir, Aspose.Cells Cloud API, Excel bul ve değiştir, bulut elektronik tablo düzenleme, uzak Excel dosyası güncelleştir"
description: "Aspose.Cells Cloud kullanarak uzak bir Excel dosyasının belirli bir aralığında metin bulup değiştirin. Kimlik doğrulamayı, hata işlemeyi ve çoklu dil SDK’larını destekler."
weight: 100
---

Bulutta depolanan uzak Excel dosyalarında toplu metin değiştirme işlemi gerçekleştirin. Aspose.Cells Bul ve Değiştir API’si ile seçili aralıklardaki belirli metin dizgelerini verimli bir şekilde bulun ve güncelleyin.

## **Uzak Aralıktaki İçeriği Değiştir API’si**

### Web API’si

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token tabanlı kimlik doğrulamayı</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri**

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                                    |
| :------------ | :---- | :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | Yol                         | Değiştirilecek, bulut depolamada saklanan çalışma kitaplığı dosyasının adı (örn. `"rapor.xlsx"`).                                                            |
| searchText    | String | Sorgu                       | Belirtilen çalışma sayfası ve hücre aralığında aranacak metin dizgisi. Tam metin eşleştirmeyi destekler.                                                      |
| replaceText   | String | Sorgu                       | Belirtilen aralıkta `searchText` ile eşleşen tüm durumların değiştirileceği metin dizgisi.                                                                   |
| worksheet     | String | Yol                         | Bul ve değiştir işleminin yapılacağı çalışma sayfasının adı.                                                                                                |
| cellArea      | String | Yol                         | Metin arama ve değiştirme işleminin yapılacağı belirli hücre aralığı (örn. `"A1:D20"`).                                                                      |
| folder        | String | Sorgu                       | Kaynak çalışma kitabının bulunduğu bulut depolama klasör yolu.                                                                                              |
| storageName   | String | Sorgu                       | _(İsteğe bağlı)_ Çalışma kitabının bulunduğu bulut depolamanın adı. Atlanırsa varsayılan bulut depolama kullanılır.                                         |
| region        | String | Sorgu                       | _(İsteğe bağlı)_ Metin işleme için yerel ayarı belirler; bu, arama işlemlerinde büyük/küçük harf duyarlılığını ve karakter kodlamasını etkileyebilir (örn. `"en-US"`, `"tr-TR"`). |
| password      | String | Sorgu                       | _(İsteğe bağlı)_ Çalışma kitabısı şifreliyse dosyayı açıp değiştirmek için şifreyi sağlayın.                                                                 |

### **Yanıt**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

Başarılı bir çağrı aşağıdaki somut JSON verisini döndürür:

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### Hata Kodları

| Kod | Mesaj          | Ne Zaman Oluşur                                          |
| --- | -------------- | -------------------------------------------------------- |
| 400 | Bad Request    | İstek URI’si ya da parametreler bozuk.                   |
| 401 | Unauthorized   | Eksik veya geçersiz kimlik doğrulama jetonu.             |
| 404 | Not Found      | Belirtilen çalışma kitaplığı bulunamıyor ya da erişilemiyor. |
| 500 | Server Error   | Çalışma kitabısı işlenirken iç sunucu hatası oluştu.      |

## Uzak Elektronik Tabloda Aralığın İçeriğini Değiştir API’si Nerede Kullanılmalı?

- **Toplu Bulut Dosyası Güncelleme**: AWS S3 ve Azure Blob gibi bulut depolama ortamlarında saklanan birden fazla Excel dosyasının içeriğini değiştirin.
- **Dinamik Bulut Şablonları Doldurma**: Bulutta depolanan rapor şablonları için dinamik verileri toplu olarak doldurun.
- **Bölgesel Dosya Senkronizasyonu**: Farklı coğrafi bölgelerdeki bulut depolamadaki Excel dosyalarının içerik tutarlılığını senkronize edin.

## Uzak Elektronik Tabloda Aralığın İçeriğini Değiştir API’si Neden Kullanılmalı?

- **Geliştirici Dostu**: Aspose.Cells Cloud, çoklu dillerde SDK kütüphaneleri sunar; hızlı geliştirme ve kapsamlı belgeler sağlar. Özel çözümler geliştirme karşılaştırıldığında geliştirme iş yükünü önemli ölçüde azaltır.
- **Düşük İşgücü Maliyeti**: Belge birleştirme işlerini yürütmek için özel personel ihtiyaçını azaltır.
- **Ödeme-per-kullanım**: Ön ödeme gerektirmez; yalnızca gerçekten kullanılan API çağrıları için ödeme yapılır.
- **Sıfır Bakım Maliyeti**: Sunucuları bakım yapmaya, yazılımları güncellemeye veya uyumluluk sorunlarıyla uğraşmaya gerek yoktur.
- **Karmaşık Excel Biçimlendirmesini Korur**: Evrensel olarak erişilebilir bir PDF formatında karmaşık Excel biçimlendirmesini korur.

## SDK’larla Uzak Elektronik Tabloda Aralığın İçeriğini Değiştir API’si Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoldur. SDK, altta yatan ayrıntıları yöneterek, elektronik tablolarda içerik değiştirme işlemini en az kodla gerçekleştirmenizi sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}