---
title: "MinDataColumn'ı Alın – Aspose.Cells Cloud API Referansı (v3.0)"
type: docs
url: /get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, Excel çalışma sayfası, REST API, API referansı, v3.0, veri sütunu, bulut API"
description: "Aspose.Cells Cloud REST API (v3.0) aracılığıyla bir Excel çalışma sayfasındaki veri içeren en soldaki sütunu alın. Yetkilendirme ayrıntılarını, istek sözdizimini, JSON yanıt örneğini, hata kodlarını ve SDK snippet'lerini içerir."
ArticleTitle: "MinDataColumn'ı Alın – Aspose.Cells Cloud API Referansı (v3.0)"
---

**`mindatacolumn`** uç noktası, belirtilen bir çalışma sayfasında herhangi bir hücre verisi içeren en soldaki sütunun sıfır tabanlı indeksini döndürür.  
Yani, aslında veri içeren ilk sütunu gösterir.

> **Tanım** – `mindatacolumn`: Çalışma sayfasında veri içeren ilk sütunun indeksidir (0'dan başlar).

**Ön Gereksinimler**  
- Geçerli bir OAuth2 erişim belirteci gereklidir.  
- Excel dosyası Aspose Cloud depolama alanına yüklenmiş olmalıdır.

**İstek Parametreleri**

| Parametre      | Tür    | Gerekli  | Açıklama                                 |
|----------------|--------|----------|---------------------------------------------|
| `fileName`     | string | Evet      | Bulut depolama alanında saklanan Excel dosyasının adı. |
| `sheetName`    | string | Evet      | Sütun indeksinin alınacağı çalışma sayfasının adı. |
| `Authorization` (header) | string | Evet | OAuth2 kimlik doğrulaması için Bearer belirteci. |

- **cURL Örneği**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP Durum Kodları**

| Kod | Anlamı                     | Açıklama                                      |
|-----|----------------------------|-----------------------------------------------|
| 200 | Tamam                      | Süzgeç başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek               | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                   | Geçersiz veya eksik JWT belirteci. |
| 413 | İçerik Çok Büyük           | Yüklenen dosya boyutu sınırını aşıyor. |
| 500 | Sunucu İç Hatası           | Beklenmeyen sunucu hatası. |
---

- Aspose.Cells Cloud SDK'larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yönetir ve size proje mantığına odaklanma imkanı sunar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}
---