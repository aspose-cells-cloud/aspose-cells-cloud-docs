---
title: "Toplu Kilidi Açma"
second_title: "Belge"
type: docs
url: /tr/batch/unlock
keywords: "toplu kilidi açma, Aspose.Cells Cloud, Excel, REST API, elektronik tablo, bulut SDK"
description: "Aspose.Cells Cloud REST API ile birden fazla Excel dosyasını toplu olarak kilidini açın. C#, Java, Python ve diğer diller için SDK'ları destekler."
weight: 100
---

Bu REST API, uygun Excel dosyalarını toplu olarak kilidini açar.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Konum | Açıklama |
|----------------|------|----------|-------------|
| **BatchLockRequest** |  | gövde | Kilidi açma ayarlarını içeren istek gövdesi. |

### **BatchLockRequest** Özellikleri

| Ad            | Tür                     | Açıklama                                 | Notlar |
|---------------|--------------------------|---------------------------------------------|-------|
| SourceFolder  | string                   | Kaynak Excel dosyalarını içeren klasör.  | [isteğe bağlı] |
| MatchCondition| MatchConditionRequest    | Kilidini açılacak dosyaları seçmek için kullanılan kriterler. | [isteğe bağlı] |
| Password      | string                   | Korumalı çalışma kitaplarına uygulanan şifre. | [isteğe bağlı] |
| OutFolder     | string                   | Kilidi açılmış dosyalar için hedef klasör. | [isteğe bağlı] |

### **MatchConditionRequest** Özellikleri

| Ad                 | Tür       | Açıklama                                 | Notlar |
|--------------------|-----------|---------------------------------------------|-------|
| RegexPattern       | string    | Dosya adlarını eşleştirmek için normal ifade. | [isteğe bağlı] |
| FullMatchConditions| string[]  | Eşleştirilecek tam dosya adı koşulları.     | [isteğe bağlı] |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Oluşturulacak çalışma kitabı dosyasının ikili içeriği. |
  
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

| Kod | Anlam                       | Ne Zaman Döndürülür                    |
|------|-----------------------------|-----------------------------------------|
| 200 OK | Çalışma kitabı başarıyla oluşturuldu | Normal akış                              |
| 201 Created | Çalışma kitabı oluşturuldu (alternatif yanıt) | API oluşturuldu durumunda döndüğünde |
| 400 Bad Request | Geçersiz parametreler | Taraf hatası                        |
| 401 Unauthorized | Eksik veya geçersiz belirteç | Kimlik doğrulama hatası                    |
| 409 Conflict | Dosya mevcut ve `isWriteOver=false` | Mevcut dosya ile çakışma    

## SDK'larla PostBatchLock API Nasıl Kullanılır

### PostBatchLock API Spesifikasyonu


[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

### Aspose.Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, kilidi açma işlevselliği geliştirmenin en hızlı yoludur. Bir SDK, düşük seviyeli ayrıntıları soyutlar ve iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}
---