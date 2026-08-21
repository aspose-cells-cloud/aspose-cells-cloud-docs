---
title: "Aspose.Cells Cloud – Dosya Silme API'si"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud – Dosya Silme API'si"
linktitle: "Dosya Sil"
type: docs
url: /delete-file/
keywords: "Aspose Cells, Dosya Silme API'si, Excel Bulut Depolama, REST API, Dosya Yönetimi"
description: "Aspose.Cells Cloud depolarından bir Excel dosyasını REST tabanlı Dosya Silme API'si ile silin. Uç nokta, parametreler, kimlik doğrulama ve örnek kod içerir."
weight: 100
---

**deleteFile** API'si, belirtilen dosyayı bulut depolama alanından kaldırarak kaynak ve veri yönetimini verimli hale getirir.

## **Excel API'si: Dosya Silme**

### Web API'si

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### İstek Parametreleri

| Parametre Adı | Tür    | Konum | Açıklama                                                                                      |
| :------------ | :----- | :---- | :-------------------------------------------------------------------------------------------- |
| `path`        | string | Yol   | Silinmesi gereken dosyanın URL ile kodlanmış yolu.                                            |
| `storageName` | string | Sorgu | Dosyanın bulunduğu depo adı. Varsayılan depo kullanılıyorsa atlanabilir.                      |
| `versionId`   | string | Sorgu | Silinecek belirli dosya sürümünün tanımlayıcısı. Atlanırsa en son sürüm silinir.              |

### Yanıt Açıklaması

Başarılı bir istek, boş bir yanıt gövdesiyle **HTTP 200** döndürür. JSON yükü döndürülmez.

```json
{}
```

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                             |
| --- | --------------------- | -------------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.        |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT belirteci.                                   |
| 413 | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor.                                |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                          |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/DeleteFile), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istek yapma yöntemini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web servislerine istek yapma yöntemlerini göstermektedir.

---