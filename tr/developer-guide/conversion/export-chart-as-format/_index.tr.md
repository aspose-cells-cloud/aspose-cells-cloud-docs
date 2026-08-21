---
title: "Excel Grafik Dışa Aktar – Aspose.Cells Cloud API"
second_title: "Belge"
description: "Bulutta depolanan bir Excel çalışma kitabından bir grafiği tek bir REST isteğiyle PDF, PNG, SVG veya diğer formatlara dönüştürün."
ArticleTitle: "Yerel Bir Elektronik Tablo Çalışma Sayfasını PDF Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktitle: "Çalışma Sayfasını PDF'ye Dönüştür"
type: docs
url: /export-chart-as-format/
keywords: "Aspose.Cells Cloud, Grafik Dışa Aktar, API, PDF, PNG, SVG, Excel, REST, Bulut Dönüştürme"
weight: 100
---

Aspose Cloud Deposu'nda depolanan bir çalışma kitabında bulunan bir grafiği, kaynak dosyayı indirmeden farklı bir dosya formatına (PDF, PNG, SVG, …) dönüştürün.

## ExportChartAsFormat API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### 📦 İstek Parametreleri

| Name               | Type    | Location | Required | Description                                               |
| ------------------ | ------- | -------- | -------- | --------------------------------------------------------- |
| **name**           | string  | Path     | Yes      | Çalışma kitabı dosya adı.                                 |
| **worksheet**      | string  | Path     | Yes      | Grafiğin bulunduğu çalışma sayfası adı.                   |
| **chartIndex**     | integer | Path     | Yes      | Dışa aktarılacak grafiğin sıfır tabanlı dizini.           |
| **format**         | string  | Query    | Yes      | İstenen çıktı formatı (örn., `png`, `pdf`, `svg`).        |
| **folder**         | string  | Query    | No       | Çalışma kitabının bulunduğu klasör yolu (öntanımlı: kök). |
| **storageName**    | string  | Query    | No       | Özel depo adı; öntanımlı depoyu kullanmak için boş bırakın.|
| **outPath**        | string  | Query    | No       | Dönüştürülmüş dosyanın kaydedileceği klasör yolu.         |
| **outStorageName** | string  | Query    | No       | Çıktı dosyası için depo adı.                              |
| **fontsLocation**  | string  | Query    | No       | Özelleştirilmiş yazı tiplerini içeren klasör yolu.        |
| **region**         | string  | Query    | No       | Yerel ayar (örn., `en-US`, `fr-FR`).                      |
| **password**       | string  | Query    | No       | Korumalı bir çalışma kitabını açmak için şifre.           |

### **Yanıt**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | İstek Hatası          | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                               |
| 413 | Yük Çok Büyük         | Yüklenecek dosya boyut sınırını aşıyor.                          |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                       |

## Grafik Dışa Aktar Formatı API'sini SDK'larla Nasıl Kullanılır?

### Grafik Dışa Aktar Formatı API Özellikleri

[Grafik Dışa Aktar Formatı API Özellikleri](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat), herkese açık bir programlama arayüzü sağlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
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

### Aspose.Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, düşük seviye detaylardan soyutlayarak elektronik tablo verilerini PDF dosyasına dönüştürmek için minimum kodla geliştirme yapmanın en hızlı yoludur. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK'lar kullanarak nasıl çağrılacağını göstermektedir: