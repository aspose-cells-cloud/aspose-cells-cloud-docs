---
title: "Gelişmiş Excel Dosyası Dönüştürme"
second_title: "Belge"
linktype: "Gelişmiş Dönüştür"
type: docs
url: /tr/advanced-convert-excel/
keywords: "Aspose.Cells, Excel dönüştürme, Bulut API'si, SDK"
description: "Aspose.Cells Cloud REST API, Excel çalışma kitaplarını PDF, HTML, CSV vb. bir dizi biçime dönüştürme, sayfa ayarlarını yapılandırma, kaydetme seçeneklerini ve yazdırma ayarlarını belirleme konusunda güçlü özellikler sunar. SDK'lar, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift için mevcuttur ve birden fazla platformda sorunsuz entegrasyon sağlar."
weight: 50
ArticleTitle: "Gelişmiş Excel Dosyası Dönüştürme – Aspose.Cells Cloud API Kılavuzu"
---

## Excel Dönüştürme İçin Gelişmiş Bulut API'si

Gelişmiş Dönüştürme işlemi, bir Excel çalışma kitabını PDF, HTML, CSV vb. çeşitli çıktı biçimlerine dönüştürmenizi sağlarken, sayfa ayarı, kaydetme seçenekleri ve yazdırma ayarları konusunda ince ayar kontrolü sağlar.

**Ön Koşullar / Yetkilendirme**  
Bu uç noktayı kullanmak için Aspose.Cells Cloud'dan bir erişim belirteci almalı ve bunu `Authorization` başlığında Bearer token olarak eklemeniz gerekir.

**API Referansı**  
- **Yöntem:** `PUT`  
- **Uç Nokta:** `/cells/convert`  
- **Parametreler:**  
  - `format` (string, gerekli) – İstenen çıktı formatı (örn. `pdf`, `html`).  
  - `outPath` (string, isteğe bağlı) – Dönüştürülen dosyanın bulut depolama alanında kaydedileceği yol.  
  - `options` (object, isteğe bağlı) – `pageSetup`, `saveOptions` ve `printSettings` gibi gelişmiş dönüştürme seçeneklerini içeren JSON nesnesi.  
- **İstek Gövdesi Örneği:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Yanıt:**  
  - `200 OK` – Dönüştürme başarılı; yanıt, dönüştürülen dosya akışını veya kaydedilen dosyaya ilişkin referansı içerir.  
  - `400 Bad Request` – Geçersiz parametreler veya bozuk istek gövdesi.  
  - `401 Unauthorized` – Yetkilendirme başarısız oldu veya belirteç eksik.  
  - `500 Internal Server Error` – Dönüştürme sırasında sunucu tarafında hata oluştu.  

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Süzgeç başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400  | Bad Request                 | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401  | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413  | Payload Too Large           | Yüklenen dosya boyut limitini aşıyor. |
| 500  | Internal Server Error       | Beklenmeyen sunucu hatası. |

**Notlar**  
* Bazı çıktı biçimlerinin belirli sınırlamaları vardır (örn. HTML dönüştürmesi makroları korumaz). Detaylar için ilgili format belgelerini inceleyin.

### Hesap tablosu dosyalarını birden fazla veri kaynağından yükleme yeteneği

### Sayfa Ayarlarını ve Kaydetme Seçeneklerini Belirleme

## Bulut SDK Ailesi

Bir SDK kullanmak, düşük seviye ayrıntıları yöneterek projenizin görevlerine odaklanmanızı sağlar ve geliştirme sürecini hızlandırır. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web hizmetlerine nasıl istekte bulunulacağını göstermektedir:

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

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Gelişmiş Dönüştürme",
  "description":"Excel çalışma kitabını PDF/HTML/CSV'ye gelişmiş seçeneklerle dönüştürün.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"İstenen çıktı formatı (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>