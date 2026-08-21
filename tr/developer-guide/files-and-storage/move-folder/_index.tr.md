---
title: "Aspose.Cells Cloud Klasör Taşıma API’si – Bulutta Klasörleri Hızlıca Taşıyın"
second_title: "Belge"
ArticleTitle: "Bulut Tabanlı Excel Dosyası Yönetimi – Bulutta Klasörleri Hızlıca Taşıyın"
linktype: "Klasörü Taşı"
type: docs
url: /tr/move-folder/
keywords: "Aspose.Cells, Klasörü Taşı, Bulut Depolama, Excel API"
description: "Aspose.Cells Cloud deposunda RESTful Klasör Taşıma API’si aracılığıyla klasörleri nasıl taşırayacağınızı öğrenin. Endpoint, parametreler, örnek cURL, hata kodları ve C#, Java, Python ve daha fazlası için SDK örneklerini içerir."
weight: 100
---

Bu API, bir klasörü Aspose.Cells Cloud deposu içindeki bir konumdan diğerine taşır. Dosyaları düzenlemeye ve bulut depolamayı verimli şekilde yönetmeye yardımcı olur.

## **Excel API: Klasörü Taşı**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Örnek cURL isteği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **moveFolder** API’sinin istek parametreleri şunlardır:

| Parametre Adı   | Tür    | Konum | Açıklama                                                           |
| ---------------- | ------ | ----- | ------------------------------------------------------------------ |
| srcPath          | string | Yol   | Taşınacak klasörün tam yolu, örneğin `FolderA/`.                  |
| destPath         | string | Sorgu | Klasörün taşınacağı hedef yol, örneğin `FolderB/`.                |
| srcStorageName   | string | Sorgu | (İsteğe bağlı) Kaynak depo adı.                                   |
| destStorageName  | string | Sorgu | (İsteğe bağlı) Hedef depo adı.                                     |

**Parametre detayları**

- **srcPath** – zorunludur. Kaynak klasör yolu.
- **destPath** – zorunludur. Hedef klasör yolu.
- **srcStorageName** – isteğe bağlıdır. Kaynak depo tanımlayıcısı.
- **destStorageName** – isteğe bağlıdır. Hedef depo tanımlayıcısı.

### **Yanıt**

Başarılı durumda API, HTTP durum kodu **200 OK** ile boş bir yanıt gövdesi döndürür. Hatalar, bir `error` alanı içeren JSON nesneleri olarak döndürülür.

**HTTP Durum Kodları**

| HTTP Kodu | HTTP Durumu           | Açıklama                                                            |
| --------- | --------------------- | ------------------------------------------------------------------- |
| 200       | OK (Tamam)            | Web API başarıyla çağrıldı; yanıt işlem ayrıntılarını içerir.     |
| 400       | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401       | Unauthorized (Yetkisiz)    | Geçersiz veya eksik JWT belirteci.                                  |
| 413       | Payload Too Large (Payload Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor.                               |
| 500       | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                          |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları kendisi yönetir ve sizin projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir: