---
title: "Nesne Var mı API’si – Aspose.Cells Cloud’da Dosya/Klasör Varlığını Kontrol Edin"
second_title: "Belge"
ArticleTitle: "Nesne Var mı API’si – Aspose.Cells Cloud’da Dosya veya Klasör Varlığını Doğrulayın"
linktitle: "Nesne Var mı"
type: docs
url: /object-exists/
keywords: "Aspose.Cells, bulut depolama, nesne var mı, dosya varlığı, klasör varlığı, API"
description: "Aspose.Cells Cloud depolama alanında bir dosya veya klasörün varlığını hızlı bir şekilde doğrulamak için Nesne Var mı API’sini kullanın. İsteğe bağlı depolama adı ve sürüm kimliğini destekler ve sürümü belirlenmiş nesnelerle çalışır."
weight: 100
---

**Nesne Var mı API’si**, geliştiricilerin belirli bir dosya veya klasörün Aspose.Cells Cloud depolama alanında olup olmadığını belirlemesini sağlar. Varlığı ve yolun bir klasöre mi yoksa dosyaya mı işaret ettiğine dair basit bir Boolean döndürür.

## **Excel API: Nesne Var mı**

### Web API’si

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_, depolamadaki dosya veya klasörün tam yoldur.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür    | Konum   | Gerekli | Açıklama                                                             |
| -------------- | ------ | ------- | ------- | -------------------------------------------------------------------- |
| `path`         | string | Yol     | Evet    | Dosya veya klasörün tam yolu.                                        |
| `storageName`  | string | Sorgu   | Hayır   | Depolamanın adı; atlanırsa varsayılan olarak birincil depolama kullanılır. |
| `versionId`    | string | Sorgu   | Hayır   | Dosyanın belirli sürüm tanımlayıcısı (sürümleme etkinleştirilmişse). |

**HTTP Durum Kodları**

| HTTP Kodu | HTTP Durumu           | Açıklama                                                          |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | Tamam (OK)            | Web API’si başarıyla çağrıldı; yanıt işlem ayrıntılarını içerir.  |
| 400       | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401       | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413       | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500       | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                        |

### **Yanıt**

Başarılı bir çağrı, iki özellik içeren bir JSON yükü döndürür:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – Dosya veya klasör varsa `true`; aksi halde `false`.
- **IsFolder** – Yol bir klasöre işaret ediyorsa `true`; dosya için `false`.

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl yapılır gerektiğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
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

Gelişmeyi hızlamanın en iyi yolu bir SDK kullanmaktır. Bir SDK, düşük seviye ayrıntıları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl yapılacağını göstermektedir. Bir Gist yüklenemezse, her sekmenin altında statik bir örnek verilmiştir.