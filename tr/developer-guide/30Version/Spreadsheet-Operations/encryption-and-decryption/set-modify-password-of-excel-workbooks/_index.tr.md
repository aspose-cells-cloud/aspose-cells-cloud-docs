---
title: "Bir Excel Çalışma Kitabının Şifre Korumasını Değiştirme"
second_title: "Belge"
linktitle: "Bir Excel dosyasının şifresini değiştirme"
type: docs
url: /workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "Excel şifresi, Aspose.Cells Cloud, yazma koruması, REST API, çalışma kitabının şifresini değiştirme"
description: "Aspose.Cells Cloud REST API’sini (v3.0) kullanarak bir Excel çalışma kitabının yazma koruma şifresini değiştirin. cURL ve SDK örneklerini içerir."
weight: 100
ArticleTitle: "Bir Excel Çalışma Kitabının Şifre Korumasını Değiştirme – Aspose.Cells Cloud"
---

Bu REST API, mevcut bir Excel çalışma kitabının **yazma koruma şifresini değiştirir**.

Yazma koruma şifresini programatik olarak güncellemek, dosyayı indirmenize gerek kalmadan şifreleri döndürmenizi veya değiştirmenizi sağlar. Özellikle Aspose.Cells Cloud depolama alanına kayıtlı korunmuş çalışma kitaplarını yönetirken oldukça işe yarar.


## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.


### İstek Parametreleri

| Parametre Adı   | Tür    | Konum     | Açıklama                                            |
| ---------------- | ------ | --------- | --------------------------------------------------- |
| **name**         | string | path      | Excel çalışma kitabının adı (zorunludur).             |
| **password**     | string | body (JSON) | Aylandırılacak yeni yazma koruma şifresi (zorunludur). |
| **folder**       | string | query     | Çalışma kitabının bulunduğu isteğe bağlı klasör.      |
| **storageName**  | string | query     | İsteğe bağlı depolama hizmetinin adı.                 |

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                            |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt, işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                   |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.                |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                           |

## PutDocumentProtectFromChanges API'sini SDK'lar ile Nasıl Kullanılır

### PutDocumentProtectFromChanges API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges), web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık programlama arayüzünü tanımlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki cURL komutu Cloud API’ye nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları yönetir, böylece iş mantığınıza odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı gösterir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}