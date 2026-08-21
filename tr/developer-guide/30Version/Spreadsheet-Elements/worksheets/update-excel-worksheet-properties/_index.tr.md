---
title: "Çalışma Sayfası Özelliklerini Güncelle – Aspose.Cells Cloud API Referansı (v3.0)"
second_title: "Belge"
linktitle: "Güncelle"
type: docs
url: /tr/worksheets/update-properties/
aliases: [  /tr/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "çalışma sayfası",
    "özellikleri güncelle",
    "REST API",
    "bulut",
    "v3.0",
  ]
description: "Aspose.Cells Cloud REST API v3.0 kullanarak bir Excel çalışma sayfasının temel özelliklerini (örneğin, sıfırları gösterme, cetvel görünürlüğü) nasıl güncelleyeceğinizi öğrenin. cURL isteği, SDK örnekleri, parametreler ve hata işleme içerir."
ArticleTitle: "Çalışma Sayfası Özelliklerini Güncelle – Aspose.Cells Cloud API Referansı (v3.0)"
---

Bu REST API, çalışma sayfası temel özelliklerini günceller.

## REST API

**Önkoşullar:** Geçerli bir Aspose Cloud hesabınızın olması, bir JWT erişim belirteci almanız ve hedef çalışma kitabının desteklenen bir depolama konumunda bulunması gerekir. Tüm istekler **HTTPS** üzerinden yapılmalıdır.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **İstek parametreleri**

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                              |
| ------------- | ----- | ---------------------------- | ----------------------------------------------------------------------------------------------------- |
| name          | string | yol                          | Çalışma kitapması dosya adı (uzantı dahil).                                                          |
| sheetName     | string | yol                          | Güncellenecek çalışma sayfasının adı.                                                                 |
| sheet         | object | gövde                        | Çalışma sayfası özelliği anahtar/değer çiftlerini içeren JSON nesnesi (örn. `DisplayZeros`, `IsRulerVisible`). |
| folder        | string | sorgu                        | Çalışma kitabının bulunduğu depolamadaki klasör yolu.                                                |
| storageName   | string | sorgu                        | Kullanılacak depolamanın adı.                                                                        |

**sheet** nesnesi, istek gövdesinde JSON olarak gönderilir. Değiştirilebilecek örnek özellikler arasında `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible` ve API spesifikasyonunda tanımlanmış diğerleri yer alır.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

Tipik yanıt kodları:

- **200** – Başarılı. Çalışma sayfası özellikleri güncellendi.
- **400** – Geçersiz istek (örn., bozuk JSON veya gerekli parametre eksik).
- **401** – Yetkisiz – eksik veya geçersiz JWT belirteci.
- **404** – Çalışma kitabı veya çalışma sayfası bulunamadı.
- **500** – Sunucu iç hatası.

| Kod | Anlamı |
|-----|--------|
| 200 | Başarılı – çalışma sayfası özellikleri güncellendi. |
| 400 | Geçersiz istek – bozuk JSON veya gerekli parametre eksik. |
| 401 | Yetkisiz – eksik veya geçersiz JWT belirteci. |
| 404 | Bulunamadı – çalışma kitabı veya çalışma sayfası mevcut değil. |
| 500 | Sunucu iç hatası. |

## Bulut SDK Geliştirme Kiti

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. SDK, düşük seviye detayları kendisi yönetir; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}
---