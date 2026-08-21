---
title: "Elektronik Tablo API’si Oluşturun – Aspose.Cells Cloud (v5.0) | Excel Dosyaları Oluşturun"
second_title: "Belge"
ArticleTitle: "Yeni Excel Elektronik Tabloları Nasıl Oluşturulur – Boş veya Şablon‑Tabanlı Dosyalar Oluşturun"
linktitle: "Elektronik Tablo Oluşturun"
type: docs
url: /create-spreadsheet/
keywords: "Aspose.Cells, elektronik tablo API’si, Excel oluştur, bulut, XLSX, ODS, CSV, şablon, SDK, otomasyon"
description: "Aspose.Cells Cloud API’sini (v5.0) kullanarak boş veya şablon‑tabanlı Excel çalışma kitapları nasıl oluşturacağınızı öğrenin. Uç nokta, parametreler, hata kodları, kimlik doğrulama adımları ve SDK örneklerini içerir."
weight: 100
---

Aspose.Cells Cloud API’si ile programlı olarak yeni Excel elektronik tabloları oluşturun. Boş çalışma kitapları oluşturun veya özel şablonlardan dosyalar oluşturun. RESTful API, otomatikleştirilmiş Excel dosyası oluşturma imkânı sunar; rapor oluşturma, belge otomasyonu ve veri işleme iş akışları için idealdir.

## **Elektronik Tablo Oluştur API’si**

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür    | Konum  | Açıklama                                                                                                                                          |
| ------------------ | ------ | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | String | Sorgu  | **Zorunlu**. Yeni elektronik tablo için dosya formatı (örn. `XLSX`, `XLS`, `ODS`, `CSV`).                                                         |
| **template**       | String | Sorgu  | **İsteğe bağlı**. Bulut depolama alanınızda depolanan bir şablon dosyasının adı (örn. `invoice_template.xlsx`). Atlanırsa, boş bir çalışma kitabı oluşturulur. |
| **outPath**        | String | Sorgu  | **İsteğe bağlı**. Oluşturulan dosyanın kaydedileceği bulut depolama alanındaki hedef klasör yolu. `null` veya atlanırsa, elektronik tablo varsayılan konuma kaydedilir. |
| **outStorageName** | String | Sorgu  | **Zorunlu**. Yapılandırılmış bulut depolama alanının tanımlayıcısı (örn. `MyDrive`).                                                              |
| **region**         | String | Sorgu  | **İsteğe bağlı**. Varsayılan tarih, sayı ve para birimi formatlarını belirleyen yerel ayar (örn. `tr-TR`).                                        |
| **password**       | String | Sorgu  | **İsteğe bağlı**. Şifrelenmiş bir şablon dosyası için şifre. Şablon korumalı değilse boş bırakın.                                                  |

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

| Kod | Anlamı                | Açıklama                                                         |
| --- | --------------------- | ---------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                              |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                            |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                       |

## Elektronik Tablo Oluştur API’si Nerede Kullanılmalı?

- **Otomatik Raporlama Sistemi Başlatma** – Her günlük/haftalık otomasyon döngüsünün başında yeni boş bir çalışma kitabı oluşturun veya standart bir şablondan rapor dosyası oluşturun.
- **Kullanıcı Kendi Hizmetini Sağladığı Portaller** – Müşterilerin bir şablonu (teklif, proje zamanlaması vb.) seçmesine ve anında özelleştirilmiş bir Excel dosyasını indirmesine izin verin.
- **Toplu Veri Dışa Aktarma ve Dağıtım** – Her dışa aktarılan veri seti için tek bir formata sahip ayrı çalışma kitapları oluşturarak sonraki aşamalardaki dağıtım ve işlemeyi kolaylaştırın.

Sonraki işlemler için (örn. çalışma sayfası ekleme veya hücreleri doldurma) **Çalışma Sayfası Ekle API’si**, **Hücreyi Güncelle API’si** ve **Çalışma Kitabını Dışa Aktar API’si** dokümantasyonunu inceleyin.

## Elektronik Tablo Oluştur API’si Neden Kullanılmalı?

- **Geliştirici Dostu** – Birden fazla dil için SDK kütüphaneleri ve kapsamlı dokümantasyon sunar; özel çözümler oluşturmak yerine entegrasyonu kolaylaştırır.
- **İş Gücü Verimliliği** – Belge birleştirme gibi işlemleri otomatikleştirerek manuel çabayı azaltır.
- **Kullanım Ücretli Fiyatlandırma** – Önceden lisans ücreti ödemeden API kullanımına göre ücretlendirilir.
- **Yönetilen Hizmet** – API tamamen barındırılır; yerel sunucu bakımı veya yazılım güncellemeleri gerekmez.

## SDK’lar ile Elektronik Tablo Oluştur API’si Nasıl Kullanılır?

### Elektronik Tablo Oluştur API’si Spesifikasyonu

[Elektronik Tablo Oluştur API’si Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimlerini sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}"
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak özet kodla elektronik tablo oluşturmanızı sağladığı için en hızlı gelişim yöntemidir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’larla Aspose.Cells web hizmetlerine nasıl istek atılacağını gösterir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}