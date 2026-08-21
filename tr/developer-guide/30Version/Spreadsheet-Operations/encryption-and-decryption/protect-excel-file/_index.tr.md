---
title: "Aspose.Cells Cloud API ile Excel Çalışma Kitabını Koruma"
second_title: "Belge"
linktype: "İçerik"
type: docs
url: /tr/protect-excel-file/
aliases: [  /tr/protect-excel-workbooks/ , /tr/workbook/protect/ ]
keywords: "Aspose.Cells, Excel koruma, API, REST, SDK"
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma kitabını nasıl koruyacağınızı öğrenin. Kimlik doğrulama adımlarını, sorgu ve gövde parametrelerini, cURL isteğini ve C#, Java, PHP, Ruby, Node.js, Python, Perl ve Go için SDK kod örneklerini içerir."
weight: 30
ArticleTitle: "Aspose.Cells Cloud API Kullanarak Excel Çalışma Kitabını Koruma"
---

Bu REST API, bir Excel çalışma kitabını **korur**; böylece Aspose.Cells Cloud kullanarak bir Excel çalışma kitabını şifre ve koruma seçenekleriyle güvenli bir şekilde korumanızı sağlar.

## PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### Sorgu Parametreleri

| Parametre Adı | Tür    | Açıklama                                                         |
| ------------- | ------ | ---------------------------------------------------------------- |
| folder        | string | Kaynak çalışma kitabını içeren klasör. _(isteğe bağlı)_           |
| storageName   | string | Depolama konumunun adı. _(isteğe bağlı; varsayılan = "Default")_ |

### İstek Gövdesi Parametreleri

| Parametre Adı | Tür                      | Açıklama                                                   |
| ------------- | ------------------------ | ---------------------------------------------------------- |
| protection    | WorkbookProtectionRequest | Çalışma kitabının koruma ayarlarını tanımlayan nesne. |

#### WorkbookProtectionRequest

| Parametre Adı  | Tür    | Açıklama                                                                                                                                              |
| -------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType | string | Uygulanacak koruma türü. İzin verilen değerler (büyük/küçük harf duyarsız): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password       | string | Koruma için ayarlanacak isteğe bağlı şifre.                                                                                                           |

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

## PostProtectDocument API'yi SDK’larla Nasıl Kullanılır

### Ön Gereksinimler

API’yi çağırmadan önce aşağıdaki adımları tamamladığınızdan emin olun:

- **JWT erişim belirteci edinin**, güvenlik bölümünde açıklanan kimlik doğrulama akışını kullanarak.  
- **Çalışma kitabını** Aspose Cloud depolama alanınıza yükleyin veya hedef klasörde zaten mevcut olduğunu doğrulayın.  
- **Depo adını** (belirtilmezse varsayılan "Default") ve korumak istediğiniz tam dosya adını bilmelisiniz.

### PostProtectDocument API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Örnek: cURL ile Çalışma Kitabını Koruma

1. **Ön Gereksinimler / Kimlik Doğrulama** bölümünde açıklanan şekilde bir erişim belirteci edinin.  
2. İsteği yürütün:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   Yanıt, korumanın başarıyla tamamlandığını onaylayan bir durum nesnesi içerir.

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, Aspose.Cells Cloud ile geliştirme yapmanın en hızlı yoludur. SDK, düşük seviyeli detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub Deposu</a>'na bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Örnek Tam Yanıt

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```