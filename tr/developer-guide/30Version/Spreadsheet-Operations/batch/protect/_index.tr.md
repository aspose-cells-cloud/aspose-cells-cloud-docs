---
title: "Excel Dosyalarını Toplu Olarak Korumalı Hale Getir"
second_title: "Belge"
type: docs
url: /batch/protect
keywords: "Excel Dosyalarını Toplu Olarak Korumalı Hale Getir, Aspose Cells Cloud, REST API, Excel koruması, toplu koruma"
description: "Aspose.Cells Cloud REST API’sini kullanarak birden fazla Excel dosyasını toplu olarak nasıl koruyabileceğinizi öğrenin. İstek detaylarını, cURL örneğini ve çeşitli programlama dilleri için SDK kod örneklerini içerir."
weight: 100
---

Bu REST API, uygun Excel dosyalarının **toplu korumasını** sağlar.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı        | Tür                  | Konum | Açıklama                                                                                               |
|----------------------|----------------------|-------|--------------------------------------------------------------------------------------------------------|
| batchProtectRequest  | BatchProtectRequest  | body  | Kaynak klasörü, eşleştirme koşullarını, koruma türünü, parolayı ve çıktı klasörünü belirten JSON yükü. |

### BatchProtectRequest Özellikleri

| Ad                | Tür                        | Açıklama                                                                              | Notlar     |
|-------------------|----------------------------|---------------------------------------------------------------------------------------|------------|
| SourceFolder      | string                     | Kaynak Excel dosyalarını içeren klasör.                                               | isteğe bağlı |
| MatchCondition    | MatchConditionRequest      | Korumaya uygun dosyaları seçmek için kullanılan kriterler.                            | isteğe bağlı |
| ProtectionType    | string                     | Uygulanacak koruma türü (örn. `All`, `ReadOnly`).                                     | isteğe bağlı |
| Password          | string                     | Korumalı dosyalar için ayarlanacak parola.                                            | isteğe bağlı |
| OutFolder         | string                     | Korumalı dosyaların konumlandırılacağı hedef klasör.                                  | isteğe bağlı |

### MatchConditionRequest Özellikleri

| Ad                  | Tür        | Açıklama                                     | Notlar     |
|---------------------|------------|----------------------------------------------|------------|
| RegexPattern        | string     | Dosya adlarını eşleştirmek için kullanılan normal ifade. | isteğe bağlı |
| FullMatchConditions | string[]   | Tam dosya adı koşullarının listesi.          | isteğe bağlı |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür  | Açıklama                              |
|---------------|------|---------------------------------------|
| data          | file | Oluşturulacak çalışma kitabının ikili içeriği. |

### **Yanıt**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```
**HTTP Durum Kodları**

| Kod | Anlamı                       | Ne Zaman Döner                          |
|-----|------------------------------|-----------------------------------------|
| 200 OK | Çalışma kitabı başarıyla oluşturuldu | Normal akış                              |
| 201 Created | Çalışma kitabı oluşturuldu (alternatif yanıt) | API oluşturulmuş durumunda döner |
| 400 Bad Request | Geçersiz parametreler | İstemci tarafı hatası                    |
| 401 Unauthorized | Eksik veya geçersiz belirteç | Kimlik doğrulama hatası                 |
| 409 Conflict | Dosya mevcut ve `isWriteOver=false` | Mevcut dosya ile çakışma              

## SDK’lar ile PostProtectConvert API’sini Nasıl Kullanılır

### PostProtectConvert API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PostProtectConvert), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, düşük seviye detayları kendisi yönetir ve sizin projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl atılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}
---