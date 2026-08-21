---
title: "Aspose.Cells Cloud API ile Excel Çalışma Kitabını Şifreleyin – Hızlı cURL ve SDK Örnekleri"
second_title: "Belge"
linktype: "İçerik"
type: docs
url: /excel-file-encrypt/
aliases: [/encrypt-excel-workbooks/, /workbook/encrypt/]
keywords: "Aspose Cells çalışma kitabını şifreleme, Excel şifreleme API'si, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma kitabını nasıl şifreleyeceğinizi öğrenin. cURL komutu, SDK kod örnekleri (C#, Java, Python, vb.), gerekli parametreler ve hata işleme içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Kitabını Şifreleyin – cURL ve SDK Örnekleri"
---

Bu REST API, bir Excel **çalışma kitabını** şifreler.

**Önkoşullar:** Bu uç noktayı çağırmadan önce geçerli bir JWT jetonuna ve çalışılan çalışma kitabının bir depolama konumuna yüklenmiş olması gerekir.

## PostEncryptDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### **Sorgu Parametreleri**

| Parametre Adı | Tür     | Gerekli | Açıklama                              |
| ------------- | ------- | ------- | ------------------------------------- |
| folder        | string  | ✗       | Orijinal çalışma kitabının klasör yolu. |
| storageName   | string  | ✗       | Kullanılacak depo adı.                |

### **İstek Gövdesi Parametresi**

| Parametre Adı | Tür                       | Gerekli | Açıklama                              |
| ------------- | ------------------------- | ------- | ------------------------------------- |
| encryption    | WorkbookEncryptionRequest | ✓       | Çalışma kitabının şifreleme ayarları. |

#### **WorkbookEncryptionRequest**

| Parametre Adı | Tür     | Gerekli | Açıklama                                                                              |
| ------------- | ------- | ------- | ------------------------------------------------------------------------------------- |
| EncryptionType | string  | ✓       | Şifreleme algoritması. Desteklenen değerler ve anlamları için aşağıdaki tabloya bakın. |
| KeyLength     | integer | ✗       | Şifreleme anahtarının bit cinsinden uzunluğu (`XOR` ve `Compatible` için yoksayılır). |
| Password      | string  | ✓       | Şifreleme için kullanılan şifre.                                                      |

#### **EncryptionType Değerleri**

| Değer                             | Açıklama                                      |
| --------------------------------- | --------------------------------------------- |
| `XOR`                             | Basit XOR algoritması (eski, düşük güvenlik). |
| `Compatible`                      | Excel 97‑2003 uyumlu şifreleme (40‑bit).     |
| `EnhancedCryptographicProviderV1` | SHA‑1 karma ile AES‑128.                      |
| `StrongCryptographicProvider`     | SHA‑512 karma ile AES‑256 (en güçlü).        |

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT jetonu.                           |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.                     |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                                |

## SDK’lar ile PostEncryptDocument API Nasıl Kullanılır?

### PostEncryptDocument API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# "test.xlsx" çalışma kitabını XOR algoritması (128‑bit anahtar) ve "mateen" şifresiyle şifreleyin.
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Olası hata yanıtları**

| HTTP Durumu | Kod                 | Mesaj                                         |
| ----------- | ------------------- | --------------------------------------------- |
| 400         | BadRequest          | Eksik veya geçersiz parametreler.             |
| 401         | Unauthorized        | Kimlik doğrulama jetonu eksik veya geçersiz.  |
| 403         | Forbidden           | Depoya erişim için yetersiz izinler.          |
| 500         | InternalServerError | Beklenmeyen sunucu hatası.                    |

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerine odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---