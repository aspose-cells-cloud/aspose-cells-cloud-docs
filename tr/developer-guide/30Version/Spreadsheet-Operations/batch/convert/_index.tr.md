---
title: "Excel Dosyalarını Toplu Dönüştürme"
second_title: "Belge"
type: docs
url: /batch/convert
keywords: "toplu dönüştürme, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, elektronik tablo"
description: "Aspose.Cells Cloud API'sini kullanarak birden fazla Excel dosyasını PDF, CSV, JSON veya Markdown gibi formatlara toplu olarak nasıl dönüştüreceğinizi öğrenin. Bu kılavuz, REST uç noktası ayrıntılarını, istek parametrelerini, cURL örneğini ve çeşitli programlama dilleri için SDK kod parçacıklarını içerir."
weight: 100
---

Bu REST API, uygun dosyaların **toplu dönüştürülmesini** sağlar.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı        | Tür     | Konum | Açıklama                                              |
|----------------------|---------|-------|-------------------------------------------------------|
| **batchConvertRequest** | nesne   | gövde  | Dönüştürme ayarlarını içeren istek gövdesi.           |

#### BatchConvertRequest Özellikleri

| Ad               | Tür                 | Açıklama                                              | Notlar     |
|------------------|---------------------|-------------------------------------------------------|------------|
| **SourceFolder** | dize                | Kaynak Excel dosyalarını içeren klasörün yolu.        | [isteğe bağlı] |
| **MatchCondition** | MatchConditionRequest | Dönüştürme için dosyaları seçmek üzere kullanılan koşullar. | [isteğe bağlı] |
| **Format**       | dize                | Dönüştürme hedef formatı (örn. `pdf`, `csv`).        | [isteğe bağlı] |
| **OutFolder**    | dize                | Dönüştürülen dosyaların kaydedileceği hedef klasör.   | [isteğe bağlı] |
| **SaveOptions**  | SaveOptions         | Dosyaların nasıl kaydedileceğini kontrol eden ek seçenekler. | [isteğe bağlı] |

#### MatchConditionRequest Özellikleri

| Ad                   | Tür        | Açıklama                                             | Notlar     |
|----------------------|------------|------------------------------------------------------|------------|
| **RegexPattern**     | dize       | Dosya adlarını filtrelemek için kullanılan normal ifade. | [isteğe bağlı] |
| **FullMatchConditions** | dize[]    | Eşleşmek için tam dosya adı koşullarının listesi.     | [isteğe bağlı] |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür  | Açıklama                                      |
| -------------- | ---- | --------------------------------------------- |
| data           | dosya | Oluşturulacak çalışma kitabı dosyasının ikili içeriği. |

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

| Kod | Anlamı                      | Ne Zaman Döndürülür                     |
|-----|-----------------------------|-----------------------------------------|
| 200 OK | Çalışma kitabı başarıyla oluşturuldu | Normal akış                              |
| 201 Created | Çalışma kitabı oluşturuldu (alternatif yanıt) | API oluşturuldu durumunu döndürürse |
| 400 Bad Request | Geçersiz parametreler | İstemci tarafı hatası                   |
| 401 Unauthorized | Eksik veya geçersiz belirteç | Kimlik doğrulama hatası                |
| 409 Conflict | Dosya mevcut ve `isWriteOver=false` | Mevcut dosya ile çakışma               |

## SDK’lar ile PostBatchConvert API’sini Nasıl Kullanılır

### PostBatchConvert API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PostBatchConvert), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl atlanacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye ayrıntıları yönetir ve size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl atlanacağını göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}