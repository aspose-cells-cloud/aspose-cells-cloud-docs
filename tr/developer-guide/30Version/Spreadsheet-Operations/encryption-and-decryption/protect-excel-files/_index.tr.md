---
title: "Excel Dosyalarını Korumak"
second_title: "Belge"
linktitle: "Excel dosyalarını şifrelemek"
type: docs
url: /tr/protect-excel-files/
aliases:
  [
    "/protect/without-storage/",
    "/protect/without-using-storage/",
    "/protect/without-using-storage/",
  ]
keywords: "Aspose.Cells, Excel koruma API'si, Excel çalışma kitabını şifrele, bulut hesap tablosu güvenliği, REST API"
description: "Aspose.Cells Cloud REST API’sini kullanarak Excel dosyalarını koruyun. Bu kılavuz, 2026 itibarıyla HTTP POST, cURL ve birden fazla programlama dili için SDK’lar aracılığıyla çalışma kitaplarını nasıl şifreleyeceğinizi gösterir."
weight: 40
---

Bu REST API, Excel dosyalarını korur.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Konum                      | Açıklama                             |
|---------------|-------|----------------------------|--------------------------------------|
| file          | dosya | formData (gövde)           | Yüklenecek dosya                     |
| password      | string| sorgu dizgesi (`password`) | Çalışma kitabını korumak için kullanılacak şifre |

### Yanıt

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "korunmuş dosya adı: smaple1.xlsx",
      "FileSize": boyut,
      "FileContent": "-----sample1’in Base64 dizesi-----"
    },
    {
      "Filename": "korunmuş dosya adı: sample2.xlsx",
      "FileSize": boyut,
      "FileContent": "-----sample2’nin Base64 dizesi-----"
    }
  ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK (Tamam)                  | Süzgeç başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                   |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırlarını aşıyor.          |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                     |

## SDK’lar ile PostProtect API’sini Nasıl Kullanılır?

### PostProtect API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample1’in Base64 dizesi-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample2’nin Base64 dizesi-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Hata işleme**

– API aşağıdaki durum kodlarını döndürebilir:

| HTTP Kodu | Anlam                                      | Örnek JSON hata yükü                               |
|-----------|--------------------------------------------|----------------------------------------------------|
| 400       | Bad request (Hatalı istek; örneğin, eksik dosya) | `{"Code":400,"Message":"Dosya gereklidir."}`        |
| 401       | Unauthorized (Yetkisiz; geçersiz veya eksik belirteç) | `{"Code":401,"Message":"Geçersiz erişim belirteci."}`    |
| 403       | Forbidden (Yasaklandı; yetersiz izinler)   | `{"Code":403,"Message":"Erişim reddedildi."}`           |
| 500       | Internal server error (İç sunucu hatası)  | `{"Code":500,"Message":"Beklenmeyen sunucu hatası."}` |

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini farklı SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}