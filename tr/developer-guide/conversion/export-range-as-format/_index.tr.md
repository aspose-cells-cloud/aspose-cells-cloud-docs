---
title: "Excel Aralığını PDF, PNG, CSV Olarak Dışa Aktar – Aspose.Cells Cloud API"
second_title: "Belge"
ArticleTitle: "Uzak Bir Elektronik Tablo Aralığını Diğer Formatlara Dışa Aktarma: Adım Adım Kılavuz"
linktitle: "Aralığı Format Olarak Dışa Aktar"
type: docs
url: /export-range-as-format/
keywords: "Aspose Cells, Excel Aralığını Dışa Aktar, PDF, PNG, CSV, Bulut API, Elektronik Tablo Dönüştürme"
description: "Aspose Cells Cloud'da saklanan belirli bir Excel aralığını PDF, PNG, CSV veya diğer formatlara nasıl dönüştüreceğinizi öğrenin. Uç nokta ayrıntıları, parametreler, örnek istekler, yanıt işleme ve hata bilgilerini içerir."
weight: 100
---

Bulut üzerindeki bir elektronik tablo/Excel aralığını bir format dosyasına dışa aktarın. Format dosyası, bulut üzerinde kaydedilebilir veya yerel depolama alanına dışa aktarılabilir.

## Aralığı Format Olarak Dışa Aktar API

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür     | Konum | Açıklama                                                                                                                                          |
| :----------------- | :------ | :---- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**           | String  | Yol   | (Zorunlu) Getirilecek çalışma kitapası dosyasının adı.                                                                                           |
| **worksheet**      | String  | Yol   | Elektronik tablonun çalışma sayfası adı.                                                                                                         |
| **range**          | String  | Yol   | Dönüştürülecek aralık (örneğin, `A1:C12`).                                                                                                        |
| **format**         | String  | Sorgu | (Zorunlu) İstenen çıktı formatı (örneğin, `pdf`, `png`, `svg`).                                                                                 |
| **folder**         | String  | Sorgu | (İsteğe Bağlı) Çalışma kitabının bulunduğu klasör yolu.                                                                                           |
| **storageName**    | String  | Sorgu | (İsteğe Bağlı) Özel bir bulut depolama alanı kullanılıyorsa depolama alanı adı.                                                                  |
| **outPath**        | String  | Sorgu | (İsteğe Bağlı) Bulut depolama alanındaki çıktı dosyasının yolu.                                                                                  |
| **outStorageName** | String  | Sorgu | (İsteğe Bağlı) Çıktı dosyası için depolama alanı adı.                                                                                            |
| **fontsLocation**  | String  | Sorgu | (İsteğe Bağlı) Özel yazı tipi konumu.                                                                                                             |
| **region**         | String  | Sorgu | (İsteğe Bağlı) Elektronik tablo bölgesi/dil ayarı (örneğin, `en-US`, `fr-FR`). SayıBiçimlendirme, tarih ayrıştırma ve yerel ayara özel davranışları etkiler. |
| **password**       | String  | Sorgu | (İsteğe Bağlı) Elektronik tablo dosyasını açmak için gereken parola.                                                                              |

### Yanıt

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

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                              |
| ---- | --------------------- | --------------------------------------------------------------------- |
| 200  | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.        |
| 400  | Hatalı İstek          | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                   |
| 413  | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                                |
| 500  | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                           |

## Aralığı Başka Bir Formata Dışa Aktar API'si nerede kullanılmalıdır?

### Veri Dışa Aktarma ve Taşıma Senaryoları

- **Veritabanı Entegrasyonu** – Belirli Excel aralıklarını doğrudan veritabanı sistemlerine dışa aktarın.
- **Uygulama Entegrasyonu** – Seçili elektronik tablo verilerini SaaS uygulamalarına besleyin.
- **Sistem Geçişi** – Belirli veri aralıklarını eski ve modern sistemler arasında taşıyın.
- **Çoklu Platform Paylaşımı** – Farklı platformlar arasında odaklanmış veri alt kümelerini paylaşın.

### Raporlama ve Analitik

- **Hedefli Raporlama** – Odaklı analiz için belirli rapor bölümlerini diğer formatlara dışa aktarın.
- **Gösterge Tablosu Veri Beslemeleri** – Belirli veri aralıklarını BI gösterge tablosu araçlarına sağlayın.
- **Performans Göstergeleri** – Performans takip sistemleri için KPI aralıklarını çıkarın.
- **Finansal Raporlama** – Dış denetim için mali durum raporu bölümlerini dışa aktarın.

### Geliştirme ve Test

- **Test Verisi Yönetimi** – Test amacıyla belirli veri aralıklarını dışa aktarın.
- **Geliştirme Ortamları** – Örnek veri aralıklarını geliştirme ekiplerine paylaşın.
- **API Testi** – Belirli elektronik tablo bölümlerinden CSV test verileri oluşturun.
- **Prototip Geliştirme** – Uygulama prototipleri için odaklanmış veri kümeleri sağlayın.

### İşletme İşlemleri

- **Seçici Veri Paylaşımı** – Belirli veri aralıklarını dış ortaklarla paylaşın.
- **Kısmi Veri Yedekleme** – Kritik veri aralıklarını seçilen bir formatta yedekleyin.
- **Bölüm Arası Veri Aktarımı** – Belirli verileri departmanlar arasında paylaşın.
- **Uyumluluk Raporlama** – Uyumluluk gönderimleri için düzenleyici veri aralıklarını dışa aktarın.

### Otomasyon İş Akışları

- **Zamanlanmış Aralık Dışa Aktarımları** – Belirli aralıkları zamanlanmış olarak otomatik olarak dışa aktarın.
- **Tetikleyici Tabanlı Çıkarım** – İş olaylarına veya tetikleyicilere göre aralıkları dışa aktarın.
- **İş Akışı Entegrasyonu** – Aralık dışa aktarımlarını iş süreçleri iş akışlarına entegre edin.
- **Toplu Aralık İşleme** – Birden fazla belirli aralığı toplu işlemlerde işleyin.

## Aralığı Başka Bir Formata Dışa Aktar API'sini neden kullanmalısınız?

- **Geliştirici Dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kitaplıkları sunar ve kapsamlı belgelerle hızlı geliştirme sağlar. Özel grafik oluşturma çözümleri inşa etmeye kıyasla, geliştirme yükünü önemli ölçüde azaltır.
- **Düşük İşgücü Maliyeti** – Belge birleştirme için ayrılmış personel gereksinimi azalır.
- **Ödeme-Yapılan-Kadar** – Önceden yatırım gerekmez; yalnızca gerçek olarak kullandığınız API çağrıları için ödeme yaparsınız.
- **Sunucu Bakımı Gerekmez** – Bakımı yapmanız gereken sunucu yoktur, yazılım güncellemeleri ve uyumluluk sorunları da yoktur.
- **Karmaşık Excel Biçimlendirmesini Korur** – Çıktı dosyaları, orijinal elektronik tablonun biçimlendirmesini korur.

## Elektronik Tablo Aralığını Format Olarak Dışa Aktar API'si SDK'ları ile Nasıl Kullanılır?

### Aralığı Format Olarak Dışa Aktar API Belirtimi

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">Aralığı Format Olarak Dışa Aktar API Belirtimi</a>, web tarayıcısından doğrudan REST etkileşimlerini mümkün kılan herkese açık bir programlama arayüzü sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 ile kodlanmış)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak elektronik tablo aralığını bir format dosyasına kısa kodla dışa aktarmanızı sağlayan en hızlı geliştirme yoludur. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}