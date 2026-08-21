---
title: "Excel Çalışma Sayfasında Hücre Biçimlendirmesini Temizleme"
type: docs
url: /clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, Hücre Biçimlendirmesini Temizleme, REST API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API'sini kullanarak Excel çalışma sayfasındaki hücre biçimlendirmesini temizleyin. İstek detaylarını, cURL örneğini ve birden fazla dil için SDK kod snippet'lerini içerir."
ArticleTitle: "Excel Çalışma Sayfasında Hücre Biçimlendirmesini Temizleme - Aspose.Cells Cloud API"
---

**Not:** Tüm Aspose.Cells Cloud API çağrıları **HTTPS** üzerinden yapılmalıdır. HTTP uç noktaları kullanımdan kaldırılmıştır ve tarayıcılar tarafından engellenebilir.

- **Metod:** POST  
- **Uç Nokta:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

Bu REST API, bir Excel dosyasındaki hücre biçimlendirmesini temizler ve Excel çalışma sayfalarında hücre biçimlendirmesini temizlemek için Aspose.Cells Cloud paketinin bir parçasıdır.

## PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Yanıt Şeması**

| Alan   | Türü    | Açıklama                                         |
|--------|---------|--------------------------------------------------|
| Code   | tamsayı | API tarafından döndürülen HTTP durum kodu (örn., 200). |
| Status | dize    | İşlemin sonucu (başarılı durumda `OK`).          |

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                          |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.               |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırlarını aşıyor.         |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                        |

## PostClearFormats API’sini SDK’larla Nasıl Kullanılır

### PostClearFormats API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca ulaşabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

SDK kullanmak, geliştirmenin en hızlı yoludur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakınız**

- [Hücre İçeriğini ve Stillerini Temizleme](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [Hücre Stili Ayarlama](https://docs.aspose.cloud/cells/set-cell-style)
---