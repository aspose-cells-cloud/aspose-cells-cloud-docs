---
title: "Birden Fazla Excel Dosyasını Tek Bir Elektronik Tabloya Birleştirin – Aspose.Cells Cloud API"
second_title: "Belge"
ArticleTitle: "Birden Fazla Excel Dosyasını Tek Dosyada Birleştirin – Elektronik Tabloları Toplu Olarak 30+ Formata Birleştirin"
linktitle: "Elektronik Tabloları Birleştirin"
type: docs
url: /merge-spreadsheets/
keywords: "Aspose.Cells, elektronik tablo birleştirme, Excel API, bulut elektronik tablo, toplu birleştirme, PDF dönüştürme, CSV birleştirme, ODS birleştirme, API referansı, SDK"
description: "Aspose.Cells Cloud ile yerel Excel, CSV veya ODS dosyalarını tek bir çalışma kitabında birleştirin ve sonucu 30+ formata (PDF, HTML vb.) dönüştürün. uç nokta, parametreler, kimlik doğrulama kılavuzu ve SDK örneklerini içerir."
weight: 100
---

Birden fazla yerel Excel, CSV veya ODS dosyasını Aspose.Cells Cloud API kullanarak tek bir çalışma kitabında birleştirin ve sonucu 30+ çıktı formatına dönüştürün.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı   | Tür      | Konum         | Açıklama                                                                                           |
| ---------------- | -------- | ------------- | -------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Dosya    | FormData      | Yüklenecek yerel elektronik tablo dosyası. XLSX, XLS, CSV, ODS vb. destekler.                      |
| outFormat        | String   | Sorgu         | İstenen çıktı formatı (örn. `XLSX`, `PDF`, `CSV`, `HTML`). 30+ format destekler.                  |
| mergeInOneSheet  | Boolean  | Sorgu         | `true` → tüm veriler tek bir çalışma sayfasında birleştirilir; `false` → orijinal sayfalar korunur.|
| outPath          | String   | Sorgu (isteğe bağlı) | Birleştirilmiş dosyanın kaydedileceği bulut klasör yolu. Atlanırsa varsayılan konum kullanılır. |
| outStorageName   | String   | Sorgu         | Kullanılacak bulut depolama adı (varsayılan veya özel).                                            |
| fontsLocation    | String   | Sorgu (isteğe bağlı) | Doğru PDF/görüntü oluşturma için özel fontların bulunduğu bulut klasörü.                          |
| region           | String   | Sorgu (isteğe bağlı) | Sayı, tarih ve para birimi formatlaması için yerel ayar (örn. `en-US`, `zh-CN`).                  |
| password         | String   | Sorgu (isteğe bağlı) | Korumalı bir elektronik tabloyu açmak için şifre.                                                  |

### **Yanıt**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Dosya doğrudan indirilebilir veya `outPath` ile belirtilen konuma kaydedilebilir.

**Başarılı yanıt detayları**

| Durum Kodu | İçerik Türü                | Açıklama                              |
| ---------- | -------------------------- | ------------------------------------- |
| 200 OK     | `application/octet-stream` | Birleştirilmiş çalışma kitabının ikili akışı. |

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                        |
| --- | --------------------- | --------------------------------------------------------------- |
| 200 | OK                    | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.    |
| 400 | Bad Request           | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized          | Geçersiz veya eksik JWT token.                                   |
| 413 | Payload Too Large     | Yüklenecek dosya boyut sınırını aşıyor.                          |
| 500 | Internal Server Error | Beklenmeyen sunucu hatası.                                       |

## Elektronik Tablo Birleştirme API'si nerede kullanılmalıdır?

### **Eğitim ve Akademik Uygulamalar**

- **Öğrenci Ödev Değerlendirme** – Birleşik yorumlar ve notlar için birden fazla öğrenci ödev dosyasını birleştirin.
- **Araştırma Verisi Toplama** – Farklı deneysel gruplardan gelen veri elektronik tablolarını birleştirin.
- **Eğitici Materyal Oluşturma** – Birden fazla bölümden gelen alıştırmaları tek bir soru bankası çalışma kitabında birleştirin.

### **Veri İşleme ve Analiz**

- **Küçük Veri Seti Entegrasyonu** – Farklı kaynaklardan dışa aktarılan CSV veya Excel dosyalarını birleştirin.
- **Veri Analizi Ön İşleme** – Analiz yapmadan önce ilgili veri dosyalarını birleştirin.
- **Şablon Veri Doldurma** – Önceden ayarlanmış rapor şablonlarını birleştirilmiş verilerle doldurun.

### **Geliştirme ve Teknik Destek**

- **Test Verisi Hazırlama** – Otomatik testler için birden fazla test senaryo dosyasını birleştirin.
- **Günlük Dosyası Analizi** – Farklı dönemlerden gelen sistem günlük raporlarını birleştirin.
- **Yapılandırma Yönetimi** – Birden fazla yapılandırma elektronik tablosunu tek bir yapılandırma dosyasında birleştirin.

## Elektronik Tablo Birleştirme API'sini neden kullanmalısınız?

- **Geliştirici Dostu** – Birçok dil için SDK kütüphaneleri mevcuttur; özel bir çözüm geliştirmeye göre geliştirme çabasını azaltır.
- **Düşük İşgücü Maliyeti** – Manuel belge birleştirme için özel personel gerekmez.
- **Ödeme-Ödeme** – Gerçekten yaptığınız API çağrıları için ödeme yapın; ön ödemeye gerek yoktur.
- **Sıfır Bakım Maliyeti** – Bakımlı sunucu, yazılım güncellemeleri veya uyumluluk sorunları yoktur.

## SDK ile Elektronik Tablo Birleştirme API'sini Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, API'nin makineyle okunabilir bir tanımını sağlar ve doğrudan REST etkileşimlerini mümkün kılar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 kodlu)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK Kullanımı

SDK kullanmak, düşük seviye detayları soyutlayarak elektronik tablo çalışma sayfasına veri içe aktarmak için kısa kodla hızlı geliştime sağlar. Aspose.Cells Cloud SDK'larının tam listesi için <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposu</a>'na göz atın.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}