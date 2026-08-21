---
title: "Bir Excel Çalışma Kitabını Şifresini Çözme"
second_title: "Belge"
linktitle: "Bir Excel dosyasının şifresini çözme"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, Excel şifre çözme, REST API, bulut SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabının şifresini nasıl çözeceğinizi öğrenin. Gerekli parametreleri, cURL örneğini, SDK kod örneklerini ve hata işleme ayrıntılarını içerir."
ArticleTitle: "Aspose.Cells Cloud API Kullanarak Bir Excel Çalışma Kitabının Şifresini Nasıl Çözersiniz?"
weight: 50
---

**Ön Gereksinimler**

- Geçerli bir JWT erişim belirteci.
- Çalışma kitabının Aspose Cloud deposuna yüklenmiş olması ve yolu `folder` sorgu parametresinde belirtilmiş olması gerekir.

## DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvendedir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### Sorgu Parametreleri

| Parametre Adı | Tür   | Açıklama                                     |
| -------------- | ------ | ----------------------------------------------- |
| folder         | string | Orijinal çalışma kitabının bulunduğu klasör yolu.           |
| storageName    | string | Çalışma kitabının bulunduğu depo adı. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür                      | Açıklama                                  |
| -------------- | ------------------------- | -------------------------------------------- |
| encryption     | WorkbookEncryptionRequest | Şifre çözme için gereken şifreleme ayarları. |

### WorkbookEncryptionRequest

| Parametre Adı | Tür    | Açıklama                                                                                                   |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| EncryptionType | string  | Şifreleme algoritması (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength      | integer | Şifreleme anahtarının bit cinsinden uzunluğu.                                                                         |
| Password       | string  | Şifre çözme için kullanılan şifre.                                                                                 |

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**Örnek Hata Yanıtları**

```json
{
  "Code": "400",
  "Message": "Geçersiz istek parametreleri."
}
```

```json
{
  "Code": "401",
  "Message": "Kimlik doğrulama başarısız. Geçersiz veya eksik JWT belirteci."
}
```

```json
{
  "Code": "413",
  "Message": "Yük çok büyük. Yüklenen dosya izin verilen boyutu aşıyor."
}
```

```json
{
  "Code": "500",
  "Message": "İç sunucu hatası. Lütfen daha sonra tekrar deneyin."
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam (OK)                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Geçersiz İstek (Bad Request)                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)                | Geçersiz veya eksik JWT belirteci. |
| 413  | Yük Çok Büyük (Payload Too Large)           | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası (Internal Server Error)       | Beklenmeyen sunucu hatası. |
## DeleteDecryptWorkbook API’sini SDK’larla Nasıl Kullanırız?

### DeleteDecryptWorkbook API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sini nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK düşük seviye ayrıntıları yöneterek size proje görevlerine odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}