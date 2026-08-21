---
title: "Excel Çalışma Sayfası İçin Yakınlaştırma Ayarla – Aspose.Cells Cloud API v3.0"
second_title: "Belge"
linktitle: "Yakınlaştırma"
type: docs
url: /worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel yakınlaştırma, çalışma sayfası yakınlaştırma, REST API, bulut SDK, Excel otomasyonu"
description: "Aspose.Cells Cloud API v3.0 ile çalışma sayfası yakınlaştırmasını (10‑400 %) nasıl ayarlayacağınızı öğrenin. cURL, SDK örnekleri ve hata yönetimi içerir."
weight: 20
ArticleTitle: "Excel Çalışma Sayfası İçin Yakınlaştırma Ayarla – Aspose.Cells Cloud API v3.0"
---

Bu REST API, bir Excel çalışma sayfasının yakınlaştırma değerini ayarlar. **Kimlik doğrulama** gerekli; her isteğin `Authorization` başlığına geçerli bir Bearer JWT jetonu ekleyin.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT jeton tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **İstek Parametreleri**

| Parametre   | Tür      | Konum | Açıklama                                                               |
| ----------- | -------- | ----- | ---------------------------------------------------------------------- |
| name        | string   | path  | Excel dosyasının (çalışma kitabının) adı.                               |
| sheetName   | string   | path  | Değiştirilecek çalışma sayfasının adı.                                  |
| value       | integer  | query | Yakınlaştırma yüzdesi (izin verilen aralık **10 – 400**, örneğin `%40` için `40`). |
| folder      | string   | query | Dosyanın bulunduğu klasör yolu.                                         |
| storageName | string   | query | Depolama hizmetinin adı.                                               |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye bir istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
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

**Hata Yanıt Bilgileri**  
Mümkün HTTP durum kodları şunları içerir:

- `400 Bad Request` – eksik veya geçersiz parametreler.
- `401 Unauthorized` – eksik veya geçersiz JWT jetonu.
- `404 Not Found` – belirtilen dosya veya çalışma sayfası mevcut değil.
- `500 Internal Server Error` – beklenmeyen sunucu tarafı hata.

Her hata yanıtı, bir `Code` ve açıklayıcı bir `Message` içeren JSON gövdesi döndürür.

## Bulut SDK Ailesi
SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları kendisi yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}