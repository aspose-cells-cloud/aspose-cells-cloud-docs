---
title: "Toplu Bölme"
second_title: "Belge"
type: docs
url: /batch/split
keywords: "Toplu Bölme, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, Elektronik Tablo, Bulut SDK'sı"
description: "Elektronik tablo dosyalarını PDF, CSV veya JSON gibi birden fazla formata bölen Aspose.Cells Cloud Toplu Bölme API'sinin belgeleri. İstek detayları, örnek cURL komutları ve çeşitli programlama dilleri için SDK kullanımı içerir."
weight: 100
---

Bu REST API, uygun dosyaların **toplu bölünmesini** gerçekleştirir.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür                | Yol/Sorgu/String/HTTPBody | Açıklama                                     |
|------------------|--------------------|---------------------------|----------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                      | Bölme seçeneklerini içeren istek yükü.      |

### **BatchSplitRequest** Özellikleri

| Ad              | Tür                 | Açıklama                                      | Notlar       |
|-----------------|---------------------|-----------------------------------------------|--------------|
| SourceFolder    | string              | Kaynak dosyayı içeren klasör.                 | [isteğe bağlı] |
| SourceStorage   | string              | Kaynak dosyanın bulunduğu depo adı.           | [isteğe bağlı] |
| MatchCondition  | MatchConditionRequest| Dosyaları bölme için kullanılan koşullar.    | [isteğe bağlı] |
| Format          | string              | İstenen çıktı formatı (örn. pdf, csv).       | [isteğe bağlı] |
| FromIndex       | integer             | Bölünecek sayfaların başlangıç indeksi.       | [isteğe bağlı] |
| ToIndex         | integer             | Bölünecek sayfaların bitiş indeksi.           | [isteğe bağlı] |
| OutFolder       | string              | Bölünmüş dosyaların gideceği klasör.          | [isteğe bağlı] |
| SaveOptions     | SaveOptions         | Çıktıyı kaydetmek için ek seçenekler.         | [isteğe bağlı] |

### **MatchConditionRequest** Özellikleri

| Ad                 | Tür       | Açıklama                                     | Notlar       |
|--------------------|-----------|----------------------------------------------|--------------|
| RegexPattern       | string    | Dosya adlarını eşleştirmek için normal ifade.| [isteğe bağlı] |
| FullMatchConditions| string[]  | Tam eşleşme koşullarının listesi.            | [isteğe bağlı] |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür  | Açıklama                                   |
| ------------- | ---- | ------------------------------------------ |
| data          | file | Oluşturulacak çalışma kitaplığı dosyasının ikili içeriği. |

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

| Kod | Anlam                       | Ne Zaman Döndürülür                      |
|-----|-----------------------------|------------------------------------------|
| 200 OK | Çalışma kitabı başarıyla oluşturuldu | Normal akış                              |
| 201 Created | Çalışma kitabı oluşturuldu (alternatif yanıt) | API oluşturuldu durumunu döndürdüğünde |
| 400 Bad Request | Geçersiz parametreler | İstemci tarafı hatası                   |
| 401 Unauthorized | Eksik veya geçersiz belirteç | Kimlik doğrulama hatası                |
| 409 Conflict | Dosya mevcut ve `isWriteOver=false` | Mevcut dosya ile çakışma                 |


## SDK’lar ile PostBatchSplit API’sini Nasıl Kullanılır

### PostBatchSplit API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istekte bulunmayı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
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

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve sizin bölme görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek nasıl atılacağını göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}