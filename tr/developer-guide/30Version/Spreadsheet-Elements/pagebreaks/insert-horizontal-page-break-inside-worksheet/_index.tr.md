---
title: "Yatay Sayfa Sonu Ekle"
second_title: "Belge"
linktitle: "Yatay Sayfa Sonu Ekle"
type: docs
url: /tr/page-breaks/add-horizontal-page-break/
aliases: [  /tr/insert-horizontal-page-break-inside-worksheet/ ]
keywords: "yatay sayfa sonu, Aspose.Cells Cloud, Excel API, REST, SDK, çalışma sayfası, cURL"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasına yatay sayfa sonu eklemeyi öğrenin. İstek ayrıntılarını, cURL örneğini ve birden fazla programlama dili için SDK kod parçacıklarını içerir."
weight: 30
ArticleTitle: "Yatay Sayfa Sonu Ekle – Aspose.Cells Cloud API"
---

**Yatay Sayfa Sonu Ekle** API'si, bir Excel çalışma sayfasına yatay bir sayfa sonu ekler.

**Önkoşullar ve Kimlik Doğrulama**  
Tüm Aspose.Cells Cloud API çağrıları için geçerli bir JWT belirteci gereklidir. Belirteci, kimlik doğrulama kılavuzunda açıklanan OAuth 2.0 iş akışıyla edinin ve istek başlığına `Authorization: Bearer <jwt token>` olarak ekleyin. Hedef çalışma kitabının, API tarafından erişilebilir bir depolama konumunda (varsayılan depolama veya belirttiğiniz özel `storageName`) olması gerekir.

## PutHorizontalPageBreak API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür     | Konum   | Açıklama                                                                  |
| -------------- | ------- | ------- | ------------------------------------------------------------------------- |
| name           | string  | path    | Excel dosyasının adı.                                                     |
| sheetName      | string  | path    | Sayfa sonunun ekleneceği çalışma sayfasının adı.                          |
| cellname       | string  | query   | Sayfa sonunun başlangıcını belirten hücre referansı (örneğin **A1**).     |
| row            | integer | query   | Sayfa sonunun sıfır tabanlı satır indeksi.                               |
| column         | integer | query   | Sayfa sonunun sıfır tabanlı sütun indeksi.                               |
| startColumn    | integer | query   | Sayfa sonu eklerken aralığın başlangıç sütunu.                           |
| endColumn      | integer | query   | Sayfa sonu eklerken aralığın bitiş sütunu.                               |
| folder         | string  | query   | Excel dosyasını içeren klasör yolu.                                       |
| storageName    | string  | query   | Aspose Cloud depolama alanının adı.                                       |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir arayüz tanımlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli iletişim sağlamak için HTTPS kullanın
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

JWT belirteci eksik veya geçersiz olduğunda döndürülen bir hata yanıtı örneği:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Geçersiz veya eksik JWT belirteci."
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|------|-----------------------------|----------------------------------------------------|
| 200  | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized                | Geçersiz veya eksik JWT belirteci.                |
| 413  | Payload Too Large           | Yüklenen dosya boyut limitini aşıyor.             |
| 500  | Internal Server Error       | Beklenmeyen sunucu hatası.                        |

İlgili işlemler hakkında daha fazla bilgi için **[Yatay Sayfa Sonlarını Al](../get-horizontal-page-breaks/)** ve **[Yatay Sayfa Sonunu Sil](../delete-horizontal-page-break/)** API sayfalarına bakın.

## Bulut SDK Koleksiyonu

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları soyutlayarak projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}