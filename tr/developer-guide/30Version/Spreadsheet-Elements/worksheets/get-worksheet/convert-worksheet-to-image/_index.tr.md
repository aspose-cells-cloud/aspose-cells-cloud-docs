---
title: "Çalışma Sayfasını PDF, PNG, CSV ve Daha Fazlasına Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Çalışma sayfasını dönüştür"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, çalışma sayfası dönüştürme, REST API, cURL, SDK, PDF, PNG, CSV"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabındaki tek bir çalışma sayfasını PDF, PNG, CSV ve 15'ten fazla diğer forma dönüştürme yöntemini öğrenin. cURL örneği, SDK snippet'leri ve tam parametre referansını içerir."
weight: 130
ArticleTitle: "Çalışma Sayfasını PDF, PNG, CSV ve Daha Fazlasına Dönüştür – Aspose.Cells Cloud API"
---

**Çalışma Sayfası Dönüştürme API'si** – `GET /cells/{name}/worksheets/{sheetName}` uç noktası, bir Excel çalışma kitabının içindeki tek bir çalışma sayfasını (sheet) başka bir dosya türüne dönüştürür.

> **Önkoşul:** Bu uç noktayı çağırmadan önce geçerli bir JWT belirteci sahip olmanız ve çalışma kitabının desteklenen Aspose Cloud depolama konumunda saklanmış olması gerekir.

Desteklenen **içe aktarılabilir** formatlar (çalışma sayfası okunabilir):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

Desteklenen **yalnızca dışa aktarılabilir** formatlar (çalışma sayfası olarak kaydedilebilir):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## REST API

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat), herkese açık erişilebilir arayüzü açıklar.

### **İstek Parametreleri**

| Parametre                | Tür     | Gerekli | Varsayılan | İzin Verilen Değerler                                                  | Açıklama                                         |
| ------------------------ | ------- | ------- | ---------- | --------------------------------------------------------------------- | ------------------------------------------------ |
| **format**               | string  | Evet    | –          | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (desteklenen listeye bakın) | Hedef çıktı formatı.                             |
| **verticalResolution**   | integer | Hayır   | 96         | 72‑600                                                                | Görüntü çıktısı için dikey DPI değeri.           |
| **horizontalResolution** | integer | Hayır   | 96         | 72‑600                                                                | Görüntü çıktısı için yatay DPI değeri.           |
| **password**             | string  | Hayır   | –          | –                                                                     | Korumalı bir çalışma kitabını açmak için şifre.  |
| **folder**               | string  | Hayır   | –          | –                                                                     | Kaynak çalışma kitabının bulunduğu bulut klasörü.|
| **storage**              | string  | Hayır   | –          | –                                                                     | Depolama adı (örneğin, "Default").              |

### Yanıt

| Durum Kodu | Açıklama                                                         | Dönüş Türü                 |
| ---------- | ---------------------------------------------------------------- | -------------------------- |
| **200**    | Dönüştürme başarılı; dönüştürülen dosyanın ikili akışı döndürülür. | `application/octet-stream` |
| **400**    | Geçersiz istek – eksik veya geçersiz parametreler.              | JSON hata nesnesi          |
| **401**    | Yetkisiz erişim – geçersiz veya eksik JWT belirteci.            | JSON hata nesnesi          |
| **404**    | Bulunamadı – çalışma kitabını veya çalışma sayfasını bulunamadı. | JSON hata nesnesi          |
| **500**    | Sunucu iç hatası – beklenmeyen hata.                             | JSON hata nesnesi          |

#### Örnek İstek (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Örnek Yanıt

```
Dönüştürülmüş Görüntü (ikili akış)
```

## Bulut SDK Ailesi

SDK kullanmak geliştirmeyi en hızlı yoldur. SDK, düşük seviye ayrıntıları yöneterek size proje odaklanma imkanı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---