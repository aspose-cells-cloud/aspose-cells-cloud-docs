---
title: "Excel Dosyalarını Kilitle"
second_title: "Belge"
linktitle: "Excel dosyalarını kilitle"
type: docs
url: /tr/lock-excel-files/
aliases: [  /tr/lock/without-storage/ , /tr/lock/ , /tr/lock/without-using-storage/ ]
keywords: "Kilitle, Excel, API, Aspose.Cells, Bulut, REST, Çalışma Kitabı, Elektronik Tablo, SDK"
description: "Aspose.Cells Cloud REST API’sini (v3.0) kullanarak Excel çalışma kitaplarını nasıl kilitleyeceğinizi öğrenin. HTTPS uç noktası, kimlik doğrulama, cURL isteği, yanıt şeması ve C#, Java, Python ve diğerleri için SDK kod örnekleri içerir."
ArticleTitle: "Excel Dosyalarını Kilitle – Aspose.Cells Cloud API Dokümantasyonu"
weight: 70
---

**API Sürümü:** v3.0 (geçerli)

Bu REST API, Excel çalışma kitaplarını **kilitler**.

## PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Gereksinimler** – İstek, **HTTPS** üzerinden gönderilir ve `Authorization` başlığında geçerli bir OAuth 2.0 Bearer belirteci içerir.

### İstek parametreleri şunlardır

| Parametre Adı | Tür   | Konum                     | Açıklama                                      |
| ------------- | ----- | ------------------------- | --------------------------------------------- |
| file          | dosya | form‑data (çok parçalı gövde) | Yüklenip kilitlenecek Excel çalışma kitabını belirtir. |
| password      | string | sorgu dizisi            | Çalışma kitabının parolası (isteğe bağlı).    |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>, herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sini **çağırma** yöntemini göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*İsteği test etmek için bir örnek çalışma kitabını indirebilirsiniz — [Sample.xlsx](https://example.com/Sample.xlsx).*

**Not:** API, 100 MB’a kadar olan dosyaları destekler; daha büyük yükler 413 (Yük Çok Büyük) yanıtıyla sonuçlanabilir.

### **Yanıt detayları**

| Alan        | Tür             | Açıklama                                          |
| ----------- | --------------- | ------------------------------------------------- |
| Filename    | string          | Hizmet tarafından döndürülen kilitli çalışma kitabının adı. |
| FileSize    | integer         | Kilitli dosyanın bayt cinsinden boyutu.          |
| FileContent | string (Base64) | Base64 dizisi olarak kodlanmış kilitli çalışma kitabının içeriği. |

Kilitli çalışma kitabını almak için `FileContent` değerini Base64’ten çözün ve yanıtta sağlanan `Filename` kullanarak kaydedin.

### **Hata işleme**

– API, standart HTTP durum kodlarını (`400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` gibi) ve `Code` ile `Message` alanlarını içeren bir JSON hata nesnesini döndürür.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye ayrıntıları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine çeşitli SDK’lar kullanılarak nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}