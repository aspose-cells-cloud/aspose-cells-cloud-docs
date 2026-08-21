---
title: "Excel Çalışma Kitabına Dijital İmza Ekleyin"
ArticleTitle: "Excel Çalışma Kitabına Dijital İmza Ekleyin – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "dijital imza"
type: docs
url: /tr/excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, dijital imza, Excel çalışma kitabı, REST API, .pfx, JWT, imza API'si"
description: "Aspose.Cells Cloud REST API'sini (v4.0) kullanarak bir Excel çalışma kitabına dijital imza nasıl ekleyeceğinizi öğrenin. Uç nokta, parametreler, kimlik doğrulama, yanıt şeması, hata yönetimi ve birden fazla dil için SDK örneklerini içerir."
weight: 35
---


**Önkoşullar:**  
Bu uç noktayı çağırmadan önce şunlardan emin olun:

- Aspose Cloud kimlik doğrulaması yoluyla geçerli bir JWT erişim belirteci edinmiş olmanız.  
- Hedef çalışma kitabının Aspose Cloud depolama alanınıza yüklenmiş olması.  
- `.pfx` veya `.p12` formatında bir dijital imza dosyasına ve şifresine sahip olmanız.

Bu REST API, bir Excel çalışma kitabına **dijital imza** ekler.

## PostDigitalSignature API

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı          | Tür    | Konum                 | Açıklama                                               |
| ------------------------ | ------ | -------------------- | ------------------------------------------------------ |
| **name**                 | string | `<code>path</code>`  | Çalışma kitabının adı.                                |
| **digitalsignaturefile** | string | `<code>query</code>` | Dijital imza dosyasının yolu (`.pfx` veya `.p12`).    |
| **password**             | string | `<code>query</code>` | Çalışma kitabının korunmuş olması durumunda şifresi.  |
| **folder**               | string | `<code>query</code>` | Çalışma kitabının bulunduğu klasör.                   |
| **storageName**          | string | `<code>query</code>` | Kullanılacak depolama hizmetinin adı.                |

*Not: Dosya adı özel karakterler içeriyorsa, sorgu dizisine eklemeden önce URL kodlaması yapın.*

### Hata Yönetimi

| HTTP Durum Kodu | Anlam                                                  |
| --------------- | ------------------------------------------------------ |
| 200             | İmza başarıyla uygulandı.                             |
| 400             | Geçersiz istek – eksik veya geçersiz parametreler.    |
| 401             | Yetkisiz erişim – geçersiz veya süresi dolmuş OAuth belirteci. |
| 403             | Yetki reddedildi – yetersiz izinler veya erişim engellendi. |
| 500             | Sunucu iç hatası – beklenmeyen hata.                  |

### HTTP Durum Kodu Hata Yanıtları

| HTTP Durum Kodu | Kod                 | Açıklama                                                  |
| --------------- | ------------------- | --------------------------------------------------------- |
| 400             | BadRequest          | Eksik veya geçersiz parametreler.                         |
| 401             | Unauthorized        | Geçersiz veya eksik erişim belirteci.                     |
| 404             | NotFound            | Belirtilen çalışma kitabı belirtilen klasör/depolama alanında bulunamadı. |
| 500             | InternalServerError | Beklenmeyen sunucu hatası.                                |


## SDK’larla PostDigitalSignature API Nasıl Kullanılır

### PostDigitalSignature API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature), genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerini çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, API'ye bir isteği göstermektedir:

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Yanıt Şeması**  
API, aşağıdaki alanları içeren bir JSON nesnesi döndürür:

| Alan         | Tür    | Açıklama                                             |
| ------------ | ------ | ---------------------------------------------------- |
| `Code`       | int    | Sonucu belirten HTTP benzeri durum kodu.             |
| `Status`     | string | Sonucu açıklayan kısa metin (örneğin, `OK`).        |
| `SignatureId`| string | Uygulanan dijital imzanın tanımlayıcısı (isteğe bağlı). |
| `Message`    | string | Ek bilgiler veya hata detayları (isteğe bağlı).       |

### Aspose.Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak entegrasyonu basitleştirir ve tekrarlayan kod miktarını azaltır. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}