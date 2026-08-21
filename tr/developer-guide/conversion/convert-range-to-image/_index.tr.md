---
title: "Excel Aralığını Görüntüye Dönüştür – Aspose.Cells Cloud API"
description: "Aspose.Cells Cloud REST API aracılığıyla yerel bir Excel dosyasından belirli bir aralığı PNG, JPEG, SVG, TIFF veya BMP formatına dönüştürün – tüm çalışma kitabını yüklemenize gerek yoktur."
keywords: "Aspose.Cells Cloud, Aralığı Görüntüye Dönüştür, Excel API, Görüntü Formatları, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

Çağrı, yerel bir elektronik tablo dosyasını okur, belirtilen aralığı dönüştürür ve görüntüyü ikili bir akış olarak döndürür.

## Aralığı Görüntüye Dönüştürme Yöntemi

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

## İstek Parametreleri

| Adı                | Konum                              | Tür     | Gerekli  | Açıklama                                                                        |
| ------------------ | ---------------------------------- | ------- | -------- | ------------------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Verisi (`multipart/form-data`)| Dosya   | **Evet** | İşlenecek Excel dosyası.                                                        |
| **worksheet**      | Sorgu                              | Dize    | **Evet** | Aralığın bulunduğu çalışma sayfası adı (örneğin `Sheet1`).                      |
| **range**          | Sorgu                              | Dize    | **Evet** | Dönüştürülecek hücre alanı, örneğin `A1:C10`.                                   |
| **format**         | Sorgu                              | Dize    | **Evet** | Çıkış görüntü formatı (`png`, `jpeg`, `svg`, `tiff`, `bmp`).                    |
| **printHeadings**  | Sorgu                              | Boolean | Hayır    | Görüntüde satır/sütun başlıklarını dahil etmek için `true`.                     |
| **outPath**        | Sorgu                              | Dize    | Hayır    | Dosyayı bulut depolama alanına kaydetmek istediğinizde kullanılacak klasör yolu.|
| **outStorageName** | Sorgu                              | Dize    | Hayır    | Depolama hizmetinin adı (örneğin `MyStorage`).                                 |
| **fontsLocation**  | Sorgu                              | Dize    | Hayır    | Dönüştürme sırasında kullanılan özel yazı tiplerinin URL’si veya yolu.          |
| **region**         | Sorgu                              | Dize    | Hayır    | Yerel ayar tanımlayıcısı (örneğin `en-US`, `fr-FR`). Sayı ve tarih formatlamasını etkiler. |
| **password**       | Sorgu                              | Dize    | Hayır    | Şifrelenmiş çalışma kitapları için şifre.                                       |
| **AutoRowsFit**    | Sorgu                              | Boolean | Hayır    | İşlemeden önce satırları otomatik sığdır.                                       |
| **AutoColumnsFit** | Sorgu                              | Boolean | Hayır    | İşlemeden önce sütunları otomatik sığdır.                                       |

## Yanıt

API, dönüştürülen HTML dosyasını **ikili akış** (`application/octet-stream`) olarak döndürür.

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

### Örnek Başarılı Yanıt (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

Görüntülenen görüntüyü tarayıcıda görmek için yanıt gövdesini bir dosyaya (örneğin `report.png`) kaydedin.

---

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
|-----|-----------------------|-------------------------------------------------------------------|
| 200 | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401 | Yetkisiz (Unauthorized)| Geçersiz veya eksik JWT belirteci.                               |
| 413 | İçerik Çok Büyük      | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                        |

## Aralığı Görüntüye Dönüştür API’sini SDK’larla Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage), web tarayıcısından doğrudan REST etkileşimlerini mümkün kılan herkese açık bir API’yi tanımlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, düşük seviye ayrıntıları gizleyerek bir aralığı görüntü dosyasına dönüştürmek için minimum kodla geliştirme yapmanın en hızlı yoludur.  
Aspose.Cells Cloud SDK’larının tam listesini [GitHub deposunda](https://github.com/aspose-cells-cloud) inceleyebilirsiniz.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını göstermektedir. Gist’ten yükleme engellenirse, örnekleri doğrudan depodan indirebilirsiniz.

---