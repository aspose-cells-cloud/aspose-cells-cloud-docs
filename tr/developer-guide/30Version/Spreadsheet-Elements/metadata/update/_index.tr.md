---
title: "Meta Verilerini Güncelleme"
second_title: "Belge"
linktitle: "Depolama kullanmadan güncelleme"
type: docs
url: /metadata/update/
keywords: "meta veriler, Excel, Aspose.Cells Cloud, REST API, güncelleme, elektronik tablo"
description: "Aspose.Cells Cloud REST API, Excel dosyalarında meta verileri güncellemenizi sağlar. Birden fazla programlama dilinde (C#, Java, Python, Ruby, Go vb.) sorunsuz entegrasyon için çeşitli SDK’ları (C#, Java, Python, Ruby, Go vb.) destekler."
weight: 35
ArticleTitle: "Meta Verileri Güncelle – Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, birden fazla Excel dosyasındaki **meta verileri** günceller.

**Önkoşullar:** Aktif bir Aspose Cloud hesabı, geçerli bir JWT erişim belirteci ve yüklenmesi gereken Excel dosyaları.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek parametreleri

| Parametre Adı      | Tür    | Konum             | Açıklama                                       |
| ------------------ | ------ | ----------------- | ---------------------------------------------- |
| file               | dosya  | formData          | Yüklenecek Excel dosyası.                      |
| DocumentProperties | nesne  | HTTP gövdesi (JSON) | Excel dosyası için ayarlanacak belge özellikleri. |

**Notlar:** Tek bir istekte en fazla 10 dosya yüklenebilir. Desteklenen formatlar: `.xlsx`, `.xls` ve `.csv`. Toplam istek boyutu 100 MB’ı aşmamalıdır.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PostMetadata), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

İstek, Bearer JWT belirteci içeren bir **Authorization** başlığı gerektirir. Belirtecin Aspose Cloud istemci kimlik bilgileriniz kullanılarak oluşturulduğundan emin olun.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Seti

SDK kullanmak, geliştirme hızını en çok artıracak en iyi yoldur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakınız:**  
- [Meta Verileri Al](/metadata/get/)  
- [Meta Verileri Sil](/metadata/delete/)  
---