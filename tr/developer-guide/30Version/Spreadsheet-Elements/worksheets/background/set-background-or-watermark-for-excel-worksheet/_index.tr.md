---
title: "Excel çalışma sayfasına arka plan ekleme"
ArticleTitle: "Excel çalışma sayfasına arka plan ekleme – Aspose.Cells Cloud API Kılavuzu"
second_title: "Belge"
linktype: "Add"
type: docs
url: /tr/worksheets/background/add/
aliases: [  /tr/set-background-or-watermark-for-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, çalışma sayfası, arka plan, REST API, SDK, resim ekleme"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasına arka plan resmi (PNG, JPEG, BMP) nasıl ekleyeceğinizi öğrenin.uç nokta, gerekli parametreler, kimlik doğrulama adımları, cURL örneği ve SDK kod örneklerini içerir."
weight: 180
---

Bu REST API, bir çalışma sayfasına bir arka plan resmi ekler.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **İstek parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama                                                       |
| ------------- | ----- | ----- | -------------------------------------------------------------- |
| name          | string | path  | Excel çalışma kitabının adı.                                   |
| sheetName     | string | path  | Resmin uygulanacağı çalışma sayfasının adı.                    |
| imageFile     | file   | body  | Arka plan olarak ayarlanacak ikili resim dosyası (PNG, JPEG, BMP, vb.). |
| folder        | string | query | Çalışma kitabının bulunduğu depolama klasörü.                  |
| storageName   | string | query | Aspose Cloud depolama adı.                                     |

**Desteklenen formatlar ve sınırlamalar**

- Kabul edilen resim uzantıları: **PNG, JPEG, BMP, GIF**.
- Maksimum dosya boyutu: **5 MB**.
- Resim, tüm çalışma sayfası arka planını doldurmak için döşenir.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
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

_Olası hata yanıtları_

| HTTP Kodu | Açıklama                                                     |
| --------- | ------------------------------------------------------------ |
| 400       | Geçersiz istek – eksik veya geçersiz parametreler.          |
| 401       | Yetkisiz erişim – geçersiz veya süresi dolmuş JWT belirteci. |
| 404       | Bulunamadı – çalışma kitabı veya çalışma sayfası mevcut değil. |
| 500       | Sunucu iç hatası – sunucuda beklenmedik bir koşul oluştu.    |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Kiti

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve sizin projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}