---
title: "Excel çalışma sayfasında sütunları göster"
ArticleTitle: "Excel çalışma sayfasında sütunları göster - Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Göster"
type: docs
url: /columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, Bulut API, sütunları göster, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API'sini kullanarak Excel çalışma sayfasında sütunları gösterme yöntemini öğrenin. İstek detaylarını, cURL örneğini ve birkaç programlama diline ait SDK kod örneklerini içerir."
weight: 50
---

Bu REST API, çalışma sayfası sütunlarını gösterir.

**Gereksinimler** – Aspose.Cells Cloud tüm uç noktaları HTTPS ve geçerli bir OAuth 2.0 erişim belirteci gerektirir. Bir erişim belirteci elde ettiğinizden ve isteklerinizin `Authorization` başlığına dahil ettiğinizden emin olun.

## PostUnhideWorksheetColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür      | Konum  | Açıklama                                     |
| ------------- | -------- | ------ | -------------------------------------------- |
| name          | string   | path   | Çalışma kitabının adı.                       |
| sheetName     | string   | path   | Çalışma sayfasının adı.                      |
| startColumn   | integer  | query  | İşlenecek ilk sütunun indeksi.              |
| totalColumns  | integer  | query  | İşlenecek sütun sayısı.                      |
| width         | number   | query  | İstenen sütun genişliği (varsayılan = 50.0). |
| folder        | string   | query  | Belgeyi içeren klasör.                       |
| storageName   | string   | query  | Depolama hizmetinin adı.                     |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**Tipik HTTP durum kodları**

| Kod | Açıklama                                       |
|-----|------------------------------------------------|
| 200 | OK – Sütunlar başarıyla gösterildi.           |
| 400 | Bad Request – Geçersiz parametreler.          |
| 401 | Unauthorized – Eksik veya geçersiz belirteç.  |
| 404 | Not Found – Çalışma kitabı veya çalışma sayfası bulunamadı. |
| 500 | Internal Server Error – Beklenmeyen hata.     |

## Bulut SDK Geliştirici Paketi

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, alt seviye ayrıntıları işler ve projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
---