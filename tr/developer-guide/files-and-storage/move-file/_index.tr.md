---
title: "Aspose.Cells Cloud Move File API – Bulut Ortamında Dosyaların Hızlı Taşınması İçin Arayüz"
second_title: "Belge"
ArticleTitle: "Bulut Tabanlı Excel Dosyası Verimli Yönetim Çözümü – Bulut Ortamında Dosyaların Hızlı Taşınması İçin Arayüz"
linktitle: "Dosya Taşı"
type: docs
url: /tr/move-file/
keywords: "Aspose.Cells, Dosya Taşı API, Bulut Depolama, Excel API, Dosya Yönetimi"
description: "Aspose.Cells Cloud deposunda v4.0 Dosya Taşı API’si kullanarak klasörler arasında dosya taşıma yöntemi – uç nokta, parametreler, örnekler ve SDK bağlantıları."
weight: 100
---

**moveFile** API’si, bir dosyayı Aspose.Cells Cloud deposunda bir konumdan diğerine taşır. Bu, dosyalarınızı düzenlemenize ve depolama alanını verimli şekilde yönetmenize yardımcı olur.

## **Excel API: Dosya Taşı**

### Web API’si

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **moveFile** API’sinin İstek Parametreleri

| Parametre Adı   | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                          |
|-----------------|--------|-------------------------------|---------------------------------------------------|
| srcPath         | String | Yol                           | Taşınacak dosyanın kaynak yolu.                   |
| destPath        | String | Sorgu                         | Dosyanın taşınacağı hedef yol.                    |
| srcStorageName  | String | Sorgu                         | Uygulanabilirse kaynak depo adı.                  |
| destStorageName | String | Sorgu                         | Uygulanabilirse hedef depo adı.                   |
| versionId       | String | Sorgu                         | Uygulanabilirse dosyanın sürüm kimliği.           |

### **Yanıt**

Başarılı bir istek, boş JSON gövdesiyle **HTTP 200 OK** döndürür.

```json
{}
```

**HTTP Durum Kodları**

| HTTP Kodu | HTTP Durumu         | Açıklama                                                           |
|-----------|---------------------|--------------------------------------------------------------------|
| 200       | OK (Tamam)          | Web API’si başarıyla çağrıldı; yanıt işlem ayrıntılarını içerir.  |
| 400       | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401       | Unauthorized (Yetkisiz)    | Geçersiz veya eksik JWT belirteci.                               |
| 413       | Payload Too Large (Aşırı Büyük Yük) | Yüklenen dosya boyut limitini aşıyor.                          |
| 500       | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                    |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FileController/MoveFile), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:

---