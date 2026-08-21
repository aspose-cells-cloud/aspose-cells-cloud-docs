---
title: "Aspose.Cells Cloud – Bulut’ta Excel Dosyalarını Birleştirin | API ile Çizelgeleri Birleştirin"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Excel Dosyalarını Bulut’ta Birleştirin – Aspose.Cells Cloud API ile Çizelgeleri Çevrimiçi Birleştirin"
linktitle: "Uzak Çizelgeyi Birleştir"
type: docs
url: /tr/merge-remote-spreadsheet/
keywords: "Aspose.Cells, Excel birleştir, bulut API, çizelge birleştir"
description: "Aspose.Cells Cloud API ile bulut depolamada saklanan Excel çalışma kitaplarını birleştirin. Tek bir HTTPS çağrısıyla çıktı formatını, hedef klasörü ve birleştirme modunu belirtin."
weight: 100
---

Aspose.Cells Cloud API ile bulutta depolanan Excel dosyalarını diğer çizelgelerle hızlıca birleştirin ve çıktı verisi formatını ve depolama konumunu belirtin.

## Uzak Çizelgeyi Birleştirme API’si

Bu işlemi çağırmadan önce şunlardan emin olun:

- Geçerli bir **JWT erişim belirteci** (kimlik doğrulama kılavuzuna bakın).
- Birleştirilecek kaynak çalışma kitabının ve tüm dosyaların bulut depolamanıza yüklenmiş olması.
- Kaynak klasörden okuma ve hedef klasöre yazma için uygun izinlere sahip olunması.

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri:

| Parametre Adı     | Tür      | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                              |
| :---------------- | :------- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------ |
| name              | String   | Yol                         | Birleştirilecek kaynak çalışma kitap dosyasının adı.                                                                                 |
| mergedSpreadsheet | String   | Sorgu                       | Kaynak çalışma kitabına birleştirilecek çizelge dosya adlarının virgülle ayrılmış listesi.                                           |
| folder            | String   | Sorgu                       | Kaynak çalışma kitabını içeren bulut depolama klasörünün yolü.                                                                      |
| outFormat         | String   | Sorgu                       | Birleştirilmiş çıktı dosyası için istenen format (örn. `XLSX`, `PDF`, `CSV`).                                                       |
| mergeInOneSheet   | Boolean  | Sorgu                       | Tüm kaynak verileri tek bir çalışma sayfasına birleştirmek için `true`, her dosya için ayrı çalışma sayfaları oluşturmak için `false`. |
| storageName       | String   | Sorgu                       | _(İsteğe bağlı)_ Kaynak çalışma kitabının bulunduğu bulut depolamanın adı. Atlanırsa varsayılan depolama kullanılır.                |
| outPath           | String   | Sorgu                       | _(İsteğe bağlı)_ Birleştirilmiş dosyanın kaydedileceği bulut depolama hedef klasör yolu. Atlanırsa dosya kaynak klasörde kaydedilir. |
| outStorageName    | String   | Sorgu                       | Çıktı dosyasının kaydedileceği bulut depolamanın adı.                                                                                |
| fontsLocation     | String   | Sorgu                       | _(İsteğe bağlı)_ Görüntü/PDF formatlarına dönüştürme sırasında kullanılan yazı tipi dosyaları için özel klasör yolu.                 |
| region            | String   | Sorgu                       | _(İsteğe bağlı)_ Çıktı dosyasındaki tarih, sayı ve para birimi formatlaması için yerel ayar/bölge (örn. `tr-TR`, `en-US`, `de-DE`).   |
| password          | String   | Sorgu                       | _(İsteğe bağlı)_ Kaynak çalışma kitabının korunmuş olması durumunda açılması için gerekli şifre.                                      |

### Yanıt

**Durum:** `200 OK`

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

Dosya doğrudan `outPath` ile belirtilen konumdan indirilebilir veya oraya kaydedilebilir.

**Başarılı yanıt ayrıntıları**

| Durum Kodu | İçerik Türü                | Açıklama                              |
| ---------- | -------------------------- | ------------------------------------- |
| 200 OK     | `application/octet-stream` | Birleştirilmiş çalışma kitap dosyasının ikili akışı. |

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                         |
| --- | --------------------- | ---------------------------------------------------------------- |
| 200 | OK                    | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | Bad Request           | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized          | Geçersiz veya eksik JWT belirteci.                               |
| 413 | Payload Too Large     | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | Internal Server Error | Beklenmeyen sunucu hatası.                                       |

## Uzak Çizelgeyi Birleştirme API’si nerede kullanılmalı?

### Kurumsal düzeyde veri entegrasyonu

- **Çoklu departman rapor birleştirme** – Satış, pazarlama, finans ve diğer ekipler tarafından gönderilen ayrı Excel raporlarını birleştirin.
- **Şube verisi özeti** – Dünyanın her yerindeki her şubenin performans verilerini özetleyin.
- **Ortak veri birleştirme** – Birden fazla ortak tarafından gönderilen veri katkılarını tek bir çalışma kitabında birleştirin.

### Bulut belge işleme iş akışı

- Bulut depolama dosya işleme: AWS S3, Azure Blob veya Google Cloud Storage’da depolanan Excel dosyalarını doğrudan birleştirin.
- **Çoklu kaynaklı veri birleştirme** – Farklı bulut konumlarından gelen dosyaları tek bir çalışma kitabında birleştirin.
- **Otomatik veri hatları** – Dosya birleştirmeyi otomatikleştirmek için API’yi ETL süreçlerine entegre edin.

### Belge yönetimi otomasyonu

- **Sürüm kontrolü birleştirme** – Bir proje planının veya bütçeleme çalışma kitabının farklı sürümlerini birleştirin.
- **Şablon veri doldurma** – Standart rapor şablonlarına veri dosyalarını ekleyin.
- **Düzenli rapor oluşturma** – Haftalık, aylık ve üç aylık özet raporları oluşturmayı otomatikleştirin.

### Çapraz platform iş birliği

- **Uzaktan ekip iş birliği** – Dağılmış ekip üyelerinin gönderdiği çalışmaları birleştirin.
- **Müşteri verisi düzenleme** – Birden fazla müşteriden gelen sipariş veya geri bildirim verilerini birleştirin.
- **Tedarikçi bilgisi özeti** – Birden fazla tedarikçiden gelen teklifleri veya ürün bilgilerini birleştirin.

## Uzak Çizelgeyi Birleştirme API’si neden kullanılmalı?

- **Geliştirici dostu** – Aspose.Cells Cloud, geliştirme süresini kısaltan ve kapsamlı belgeler sunan birçok programlama dili için SDK sağlar. Özel bir çözüm oluşturmaya kıyasla iş yükünü ciddi oranda azaltır.
- **Azaltılmış iş gücü maliyetleri** – Elle belge birleştirme ile görevlendirilmiş personel ihtiyacını azaltır.
- **Ödeme-her-kullanım için** – Önceden yatırım gerekmez; sadece kullandığınız API çağrıları için ödeme yaparsınız.
- **Sıfır bakım maliyeti** – Bakımı yapılacak sunucu yoktur, yazılım güncellemesi yoktur ve uyumluluk sorunu yoktur.

## SDK’lar ile Uzak Çizelgeyi Birleştirme API’si Nasıl Kullanılır?

### Uzak Çizelgeyi Birleştirme API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet" target="_blank" rel="noopener noreferrer">Uzak Çizelgeyi Birleştirme API Spesifikasyonu</a>, doğrudan herhangi bir HTTP istemciden çağrılabilen REST arayüzünü açıklar.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak ve kısa kod parçacığıyla bir çizelgeyi başka bir çizelgeye birleştirmenin en hızlı yoludur.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}