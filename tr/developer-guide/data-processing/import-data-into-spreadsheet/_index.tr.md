---
title: "Aspose.Cells Cloud Veri İçe Aktarma API'si – CSV, JSON ve XML verilerini Excel elektronik tablolara otomatik olarak içe aktarmak için bulut tabanlı bir çözüm."
second_title: "Belge"
ArticleTitle: "Çok Kaynaklı Veri Entegrasyonu Excel Platformu – Aspose.Cells Cloud Otomatik Veri İçe Aktarma ve Dönüşüm API'si."
linktitle: "Elektronik Tabloya Veri İçe Aktar"
type: docs
url: /tr/import-data-into-spreadsheet/
keywords: "Aspose Cells, veri içe aktarma API'si, CSV'den Excel'e, JSON'dan Excel'e, XML'den Excel'e, bulut tabanlı elektronik tablo, REST API"
description: "Aspose.Cells Cloud REST API ile CSV, JSON veya XML verilerini Excel elektronik tablolara içe aktarın. İstek formatını, parametreleri, örnek SDK kodunu ve hata yönetimi hakkında bilgi edinin."
weight: 100
---

## Temel Özellikler

### Çoklu Format Veri Desteği

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> Veri İçe Aktarma**: Çeşitli ayırıcıları destekler ve kodlamayı otomatik olarak algılar.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> Veri İşleme**: Karmaşık JSON yapılarını Excel tablolarına düzleştirir.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> Dosya Dönüştürme**: Düğüm verilerini Excel satır ve sütun yapısına eşler.

## **Elektronik Tabloya Veri İçe Aktarma API'si Açıklaması**

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür    | Konum             | Açıklama                                                                 |
| ------------------ | ------ | ----------------- | ------------------------------------------------------------------------ |
| datafile           | Dosya  | FormData          | İçe aktarılacak veri dosyası (CSV, JSON veya XML).                      |
| spreadsheet        | Dosya  | FormData          | İçe aktarılan veriyi alacak hedef çalışma kitabı.                        |
| worksheet          | string | Sorgu             | Verilerin yerleştirileceği çalışma sayfasının adı.                        |
| startCell          | string | Sorgu             | İçe aktarmanın başlayacağı sol üst hücre (örn. `A1`).                    |
| insert             | bool   | Sorgu             | Satırların eklenmesi için `true`; mevcut verilerin üzerine yazılması için `false`. |
| convertNumericData | bool   | Sorgu             | İçe aktarma sırasında sayısal dizgelerin sayılara dönüştürülmesi için `true`. |
| splitter           | string | Sorgu             | Tek karakterli CSV ayırıcısı (varsayılan: `,`).                         |
| outPath            | string | Sorgu (isteğe bağlı) | Güncellenen çalışma kitabının depolanacağı klasör yolu.                  |
| outStorageName     | string | Sorgu (isteğe bağlı) | Çıktı dosyası için depolama konumunun adı.                              |
| fontsLocation      | string | Sorgu (isteğe bağlı) | Gerekirse özel yazı tipi klasörünün yolu.                               |
| region             | string | Sorgu (isteğe bağlı) | Elektronik tablo bölge yapılandırması (örn. `tr-TR`).                   |
| password           | string | Sorgu (isteğe bağlı) | Korumalı bir çalışma kitabının açılması için şifre.                      |

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

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413 | İçerik Çok Büyük      | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                        |

## Bu API'yi Neden Kullanmalısınız?

- **Verimli veri yükleme** – Büyük veri kümelerinin ara dosyalar oluşturmadan doğrudan bir çalışma kitabına toplu olarak içe aktarılmasını sağlar.
- **Geniş SDK desteği** – .NET, Java, PHP, Ruby, Node.js, Python, Go ve Perl için istemci kitaplıkları sağlar ve entegrasyonu basitleştirir.
- **Bellek içi işleme** – Geçici depolama gereksinimlerini azaltmak için dönüşümleri bellek içinde gerçekleştirir.

## SDK’lar ile Elektronik Tabloya Veri İçe Aktarma API'sini Nasıl Kullanılır?

**Notlar / Sınırlamalar:** API, içe aktarma başına en fazla 1 000 000 satırı destekler. Varsayılan CSV ayırıcısı yalnızca virgüldür; diğer tek karakterli ayırıcılar `splitter` parametresi aracılığıyla belirtilebilir. Büyük XML dosyaları işlemenin süresini artırabilir.

Veri dışa aktarma veya çalışma kitabı formatlarını dönüştürme gibi ilgili işlemler için **Veriyi Dışa Aktar** ve **Çalışma Kitabını Dönüştür** belgelerine bakın.

### Elektronik Tabloya Veri İçe Aktarma API'si Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">Elektronik Tabloya Veri İçe Aktarma API Spesifikasyonu</a>, doğrudan web tarayıcınızdan REST etkileşimlerine izin veren herkese açık bir programlama arayüzü sağlar.
Aspose.Cells web hizmetlerine kolayca ulaşmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
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

SDK kullanımı, düşük seviyeli ayrıntıları soyutlayarak elektronik tablo çalışma sayfasına veri içe aktarmak için kısa kodla geliştirme yapmanın en hızlı yoludur. Aspose.Cells Cloud SDK’larının tam listesi için <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.