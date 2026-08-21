---
title: "Excel Çalışma Sayfasında Dizine Göre Bir Şekil Alma"
second_title: "Belge"
linktype: "Get"
type: docs
url: /shapes/get/
aliases: [/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, Excel şekil API’si, dizine göre şekil alma, çalışma sayfası şekli, REST API, şekil alma, Aspose.Cells SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından dizine göre bir şekil (resim verileri veya meta veriler dahil) alın. İstek sözdizimi, parametreler, yanıt ayrıntıları ve SDK örneklerini içerir."
weight: 20
ArticleTitle: "Excel Çalışma Sayfasında Dizine Göre Bir Şekil Alma – Aspose.Cells Cloud Dokümantasyonu"
---

Bu REST API, bir Excel çalışma sayfasından bir şekli (resim verileri veya meta verileri dahil) alır.

## GetWorksheetShape API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Gereksinimler**  
- Geçerli bir Aspose Cloud erişim belirteci (Bearer JWT).  
- Çalışma kitabının Aspose Cloud deponuzda veya belirtilen bir klasörde saklanmalı.  

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür      | Konum  | Açıklama                                                |
| ------------- | -------- | ------ | ------------------------------------------------------- |
| name          | string   | path   | Excel belgesinin adı.                                   |
| sheetName     | string   | path   | Şeklin bulunduğu çalışma sayfasının adı.                |
| shapeindex    | integer  | path   | Çalışma sayfasındaki şeklin sıfır tabanlı dizini.      |
| folder        | string   | query  | Belgenin bulunduğu klasör yolu.                         |
| storageName   | string   | query  | Depolama hizmetinin adı.                                |

**Not:** `shapeindex` sıfır tabanlıdır; ilk şeklin dizini 0’dır. Varsayılan depolamayı kullanmıyorsanız, çalışma kitabının belirtilen `folder` ve `storageName` içinde saklandığından emin olun.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Düzeltildi: endpoint ve yol
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Olası HTTP durum kodları**

| Kod  | Açıklama                                                  |
|------|-----------------------------------------------------------|
| **200 OK** | Şekil başarıyla alındı.                                   |
| **400 Bad Request** | İstek bozuk veya gerekli parametreler eksik.              |
| **401 Unauthorized** | Kimlik doğrulama başarısız oldu veya belirteç eksik/geçersiz. |
| **404 Not Found** | Belirtilen çalışma kitabısı, çalışma sayfası veya şekil dizini mevcut değil. |
| **500 Internal Server Error** | Beklenmeyen bir sunucu hatası oluştu.                     |

**Yaygın hatalar:** Yanlış temet domaini (`api.aspose.com`) veya güncel olmayan `/autoshapes/` segmentinin kullanılması 404 hatasına neden olur. Her zaman `api.aspose.cloud` domaini ile `/shapes/` segmentini kullanın.

## Bulut SDK Geliştirme Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye detayları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

İlgili işlemler için lütfen **[Şekil Ekleme](/shapes/add/)** ve **[Şekil Güncelleme](/shapes/update/)** dokümantasyonuna bakın.