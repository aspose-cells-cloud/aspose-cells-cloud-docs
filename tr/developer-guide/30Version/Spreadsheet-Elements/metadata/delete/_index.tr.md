---
title: "Excel dosyalarından meta verileri silme"
second_title: "Belge"
linktype: "Depolama kullanmadan silme"
type: docs
url: /tr/metadata/delete/
keywords: "Aspose.Cells, meta veri silme, Excel API, çalışma kitabı özellikleri"
description: "Aspose.Cells Cloud API ile çalışma kitabı meta verilerini (yazar, başlık, özel) silin. Uç nokta, kimlik doğrulama, parametreler, cURL ve SDK örneklerini içerir."
weight: 55
ArticleTitle: "Excel dosyalarından meta verileri silme – Aspose.Cells Cloud Belgeleri"
---

**Genel Bakış**  
Meta Veri Silme işlemi, yüklenen Excel dosyas(lar)ından tüm çalışma kitabı özelliklerini (standart ve özel) kalıcı olarak kaldırır ve işlenmiş dosya(lar)ı yanıt olarak döndürür.

**Önkoşullar**  
- Geçerli bir Aspose.Cells Cloud JWT belirteci (OAuth 2.0 kimlik doğrulama akışıyla elde edilebilir).  
- API sürümü **v3.0** (bu örnekte kullanılan uç nokta).  
- SDK kullanımı için, dilinize uygun Aspose.Cells Cloud SDK'sını kurun (örneğin, NuGet, Maven, npm, pip, CPAN veya Go modülleri aracılığıyla).

Bu REST API, bir veya daha fazla Excel dosyasından **meta veri** siler. Yazar, başlık ve özel veri gibi çalışma kitabı özelliklerini kaldırır ve temizlenmiş dosyaları döndürür.

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür   | Konum     | Açıklama                                                |
| ------------- | ----- | --------- | --------------------------------------------------------- |
| file          | dosya | formData  | **Meta veri** silme için yüklenecek Excel dosyası        |
| type          | string| query     | İşlem türü; tüm **meta verileri** silmek için **all** olarak ayarlayın |

<a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye istek nasıl yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Hata yanıtları** şunları içerebilir:

- **400 Bad Request (Kötü İstek)** – eksik dosya veya geçersiz `type` değeri.
- **401 Unauthorized (Yetkisiz)** – geçersiz veya eksik JWT belirteci.
- **500 Internal Server Error (İç Sunucu Hatası)** – sunucu tarafı işleme hatası.

API, her durum için ayrıntıları içeren bir `Error` alanı içeren JSON nesnesi döndürür.

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | OK (Tamam) | Meta veri silindi, dosya döndürüldü |
| 400 | Bad Request (Kötü İstek) | Eksik dosya veya geçersiz `type` |
| 401 | Unauthorized (Yetkisiz) | Geçersiz veya eksik JWT |
| 500 | Internal Server Error (İç Sunucu Hatası) | Sunucu işleme hatası |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye detayları yöneterek proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını gösterir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}