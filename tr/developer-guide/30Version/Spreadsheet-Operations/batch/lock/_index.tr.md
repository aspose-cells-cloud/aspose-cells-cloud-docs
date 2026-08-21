---
title: "Excel Dosyalarını Toplu Kilitleyin"
second_title: "Belge"
type: docs
url: /batch/lock
keywords: "toplu kilit, Excel, Aspose.Cells, Bulut API'si, elektronik tablo, dosya koruma"
description: "Aspose.Cells Cloud API, birden fazla Excel dosyasını toplu olarak kilitlemenizi sağlar. Dosyaları toplu kilitlemek için REST uç noktası veya desteklenen SDK'ların herhangi birini (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go vb.) kullanın."
weight: 100
---

Bu REST API, uygun Excel dosyalarının **toplu kilitlemesini** sağlar.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek Parametreleri

| Parametre Adı   | Tür               | Konum | Açıklama                                 |
|------------------|--------------------|----------|---------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body     | Kilitleme parametrelerini içeren JSON gövdesi.      |

#### **BatchLockRequest** Özellikleri

| Ad              | Tür                     | Açıklama                                            | Notlar    |
|-----------------|--------------------------|--------------------------------------------------------|----------|
| SourceFolder    | string                   | Kaynak Excel dosyalarını içeren klasör.           | isteğe bağlı |
| MatchCondition  | MatchConditionRequest    | Hangi dosyaların kilitleneceğini seçmek için kullanılan koşullar.         | isteğe bağlı |
| Password        | string                   | Kilidili dosyalara uygulanacak şifre.                | isteğe bağlı |
| OutFolder       | string                   | Kilidili dosyaların bulunacağı hedef klasör.              | isteğe bağlı |

#### **MatchConditionRequest** Özellikleri

| Ad                 | Tür      | Açıklama                                          | Notlar    |
|--------------------|----------|------------------------------------------------------|----------|
| RegexPattern       | string   | Dosya adlarını eşleştirmek için normal ifade deseni.      | isteğe bağlı |
| FullMatchConditions| string[] | Kilitlemek için tam dosya adı eşleşmeleri.                 | isteğe bağlı |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Oluşturulacak çalışma kitapğı dosyasının ikili içeriği. |
  
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

| Kod | Anlamı                     | Ne Zaman Döndürülür                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | Çalışma kitabı başarıyla oluşturuldu | Normal akış                              |
| 201 Created | Çalışma kitabı oluşturuldu (alternatif yanıt) | API oluşturuldu durumunu döndürdüğünde |
| 400 Bad Request | Geçersiz parametreler | İstemci tarafında hata                        |
| 401 Unauthorized | Eksik veya geçersiz belirteç | Kimlik doğrulama hatası                    |
| 409 Conflict | Dosya mevcut ve `isWriteOver=false` | Mevcut dosya ile çakışma    

## SDK'lar ile PostBatchLock API'sini Nasıl Kullanılır

### PostBatchLock API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sini nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviyeli detayları soyutlayarak kilitleme görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}
---