---
title: "Aspose.Cells Cloud API – Dosya Listesini Al (Klasör İçeriği)"
description: "Aspose.Cells Cloud deposundaki belirli bir klasörden dosya ve alt klasör listesini alın."
keywords:
  - Aspose.Cells
  - API
  - Dosya Listesini Al
  - Bulut Depolama
  - Excel
  - REST
type: docs
weight: 100
---

**Dosya Listesini Al** işlemi, Aspose.Cells Cloud deposundaki belirli bir klasörde depolanan dosya ve alt klasörlerin koleksiyonunu döndürür.  
Bu işlem, bulut tabanlı Excel çalışma kitaplarını, arşivleri ve diğer desteklenen dosya türlerini tararken temel giriş noktasıdır.

## Aspose.Cells Cloud API – Dosya Listesini Al (Klasör İçeriği)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Ad              | Konum   | Tür     | Gerekli | Açıklama                                                            |
| --------------- | ------- | ------- | ------- | ------------------------------------------------------------------- |
| **path**        | Yol     | string  | Evet    | Bulut deposundaki klasörün yolu.                                    |
| **storageName** | Sorgu   | string  | Hayır   | Kullanılacak depo adı. Atlanırsa, varsayılan depo kullanılır.     |
| **pageSize**    | Sorgu   | integer | Hayır   | Sayfa başına döndürülecek maksimum öge sayısı (varsayılan: 100).   |
| **pageNumber**  | Sorgu   | integer | Hayır   | Alınacak sayfa numarası (1'den başlar, varsayılan: 1).             |

- **Value** – `StorageFile` nesnelerinin dizisi. Her nesne şunları içerir:
  - `Name` – Dosya veya klasör adı.
  - `IsFolder` – Girdi bir klasör ise `true`.
  - `Size` – Bayt cinsinden boyut (klasörler `0` döndürür).
  - `ModifiedDate` – Son değiştirme zaman damgası (ISO 8601).

### **Yanıt**

**HTTP Durum Kodları**

| HTTP Kodu | HTTP Durumu           | Açıklama                                                         |
| --------- | --------------------- | --------------------------------------------------------------- |
| 200       | OK (Tamam)            | Web API’si başarıyla çağrıldı; yanıt işlem ayrıntılarını içerir. |
| 400       | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401       | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                              |
| 413       | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşar.                             |
| 500       | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                      |
|           |                       |                                                                  |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye ayrıntıları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir: