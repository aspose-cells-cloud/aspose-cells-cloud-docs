---
title: "Excel çalışma sayfasından arka planı silme"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /tr/worksheets/background/delete/
aliases: [  /tr/delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Çalışma sayfası arka planını sil, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasının arka plan resmini silin. SDK’lar C#, Java, PHP, Ruby, Node.js, Python, Perl ve Go dilleri için mevcuttur."
weight: 210
ArticleTitle: "Aspose.Cells Cloud API kullanarak Excel çalışma sayfasından arka planı silme"
---

Bu REST API, bir çalışma sayfasının arka plan resmini siler.

**Önkoşullar:** Çalışma kitabının Aspose Cloud deposunda saklanmış olması ve kimlik doğrulama için geçerli bir JWT erişim belirteçine sahip olmanız gerekir.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **İstek parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama                                         |
|---------------|-------|--------|--------------------------------------------------|
| name          | string | path   | Excel dosyasının adı.                            |
| sheetName     | string | path   | Arka planı silinecek çalışma sayfasının adı.     |
| folder        | string | query  | Dosyanın bulunduğu depodaki klasör.              |
| storageName   | string | query  | Depo adı (varsayılan depo değilse).              |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Tüm istekler geçerli bir JWT belirteci gerektirir. Belirteci, Kimlik Doğrulama kılavuzunda açıklanan OAuth2 belirteç uç noktası üzerinden edinin.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
  -X DELETE \
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

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek (Bad Request)| Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT belirteci.              |
| 413 | İstek Gövdesi Çok Büyük     | Yüklenecek dosya boyut sınırlarını aşıyor.       |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                       |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}