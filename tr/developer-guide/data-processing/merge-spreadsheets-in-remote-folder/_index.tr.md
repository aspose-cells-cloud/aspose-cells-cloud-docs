---
title: "Uzak Dizindeki Eşleşen Elektronik Tabloları Birleştir"
description: "Aspose Cloud deposunda bulunan elektronik tablo dosyalarını tek bir dosyada birleştirin. PDF, CSV, JSON, XLSX, ODS, XPS ve daha fazlası olmak üzere 30'dan fazla çıktı formatını destekler."
keywords: "Aspose.Cells, elektronik tablo birleştirme, uzak dizin, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

Uzak bir Aspose Cloud depo dizininde bulunan birden fazla elektronik tablo dosyasını tek bir çıktı dosyasında birleştirin. İşlem tamamen bulutta çalışır, bu da kaynak dosyaları yerel olarak indirmenize gerek kalmadan işlem yapılmasını sağlar. 30'dan fazla çıktı formatı desteklenir (PDF, CSV, JSON, XLSX, ODS, XPS, ...).

## MergeSpreadsheetsInRemoteFolder API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri <a id="request-parameters"></a>

| Ad                      | Tür      | Konum   | Gerekli | Açıklama                                                                                             |
| ----------------------- | -------- | ------- | ------- | ---------------------------------------------------------------------------------------------------- |
| **folder**              | string   | sorgu   | **Evet** | Kaynak elektronik tabloları içeren bulut depo dizini.                                               |
| **fileMatchExpression** | string   | sorgu   | **Evet** | Dosyaları seçmek için desen (örneğin, `*rapor*.xlsx`). `*` ve `?` joker karakterlerini destekler.     |
| **outFormat**           | string   | sorgu   | **Evet** | İstenen çıktı formatı (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, ...).                            |
| **mergeInOneSheet**     | boolean  | sorgu   | **Evet** | `true` – tüm veriler tek bir çalışma sayfasında birleştirilir. `false` – her kaynak dosya kendi çalışma sayfasını alır. |
| **storageName**         | string   | sorgu   | Hayır   | Özel depo adı; atlanırsa birincil depo varsayılan olarak kullanılır.                                 |
| **outPath**             | string   | sorgu   | Hayır   | Birleştirilmiş dosyanın kaydedileceği dizin. Atlanırsa dosya kaynak dizininde kaydedilir.             |
| **outStorageName**      | string   | sorgu   | Hayır   | Birleştirilmiş dosyanın yazılacağı depo adı.                                                        |
| **fontsLocation**       | string   | sorgu   | Hayır   | Özel yazı tiplerini içeren dizinin yolu (PDF/Görüntü dışa aktarma için gereklidir).                   |
| **region**              | string   | sorgu   | Hayır   | Sayı, tarih ve para birimi formatlaması için yerel ayar (örneğin, `tr-TR`, `en-US`, `de-DE`).          |
| **password**            | string   | sorgu   | Hayır   | Korumalı kaynak elektronik tablolardan herhangi birinin açılması için gerekli şifre.                  |

## İstek Örneği (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

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

Dosya doğrudan `FileUrl` adresinden indirilebilir veya `outPath` ile belirtilen konuma kaydedilebilir.

**Başarılı yanıt detayları**

| Durum Kodu   | İçerik Türü                | Açıklama                                          |
| ------------ | -------------------------- | ------------------------------------------------- |
| 200 OK       | `application/octet-stream` | Birleştirilmiş çalışma kitaplığı dosyasının ikili akışı. |
| 202 Accepted | `application/json`         | `FileUrl`, `FileName` vb. bilgileri içeren JSON. |

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                           |
| --- | --------------------- | ------------------------------------------------------------------ |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.       |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT belirteci.                               |
| 413 | Payload Too Large (İçerik Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                       |

## Nasıl SDK'lar ile Birleştir Elektronik Tablo API'si Kullanılır?

### OpenAPI Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, API'nin makine tarafından okunabilir bir açıklamasını sağlar ve doğrudan REST etkileşimlerinin yapılmasını mümkün kılar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istek nasıl atlanacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

SDK kullanmak, düşük seviye detayları soyutlayarak elektronik tablo çalışma sayfasına veri içe aktarmak için kısa kodla hızlıca geliştirme yapmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.