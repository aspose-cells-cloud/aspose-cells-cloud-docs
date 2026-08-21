---
title: "Excel Çalışma Sayfasından MinDataRow Değerini Alın"
type: docs
url: /tr/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, Bulut SDK"
description: "Aspose.Cells Cloud API v3.0 kullanarak bir çalışma sayfasının minimum veri satırı indeksini alın. İstek şablonu, parametreler, örnek cURL, yanıt örneği, HTTP durum kodları ve SDK kod parçacıklarını içerir."
ArticleTitle: "Excel Çalışma Sayfasından MinDataRow Değerini Alın – Aspose.Cells Cloud API"
---

**Aspose.Cells Cloud API v3.0**'ın **Get MinDataRow** uç noktası, belirtilen bir çalışma sayfasında veri içeren ilk satırın indeksini döndürür. İşlem, geçerli bir erişim belirteci (Bearer kimlik doğrulaması) ve sorgu parametresi `cellOrMethodName`'in `mindatarow` olarak ayarlanması gerekir.

**API sürümü: 3.0**

### cURL Örneği

İstek HTTP GET yöntemini kullanır. `{fileName}` ve `{sheetName}` yer tutucularını gerçek çalışma kitabının ve çalışma sayfasının adlarıyla değiştirin.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**İstek Parametreleri**

| Parametre          | Konum | Tür   | Zorunlu | Açıklama                                                   |
|--------------------|-------|-------|---------|---------------------------------------------------------------|
| `fileName`         | Yol   | string | Evet      | Excel çalışma kitabının adı (dosya uzantısı dahil).            |
| `sheetName`        | Yol   | string | Evet      | Çalışma kitabındaki çalışma sayfasının adı.                    |
| `cellOrMethodName` | Sorgu | string | Evet      | İşlemi çalıştırmak için `mindatarow` olarak ayarlanmalıdır.        |

**Yanıt Örneği**

```json
{
  "MinDataRow": 5
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Hatalı İstek (Bad Request)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT belirteci. |
| 413 | İçerik Çok Büyük (Payload Too Large) | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500 | İç Sunucu Hatası (Internal Server Error) | Beklenmeyen sunucu hatası. |
### SDK Örnekleri

SDK kullanmak, geliştirmenin en hızlı yoludur. SDK, düşük seviyeli ayrıntıları kendisi yönetir, böylece proje mantığına odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bkz.**

- [Get MaxDataRow](https://docs.aspose.cloud/cells/tr/get-maxdatarow-from-excel-worksheet/)
- [Get MinColumn](https://docs.aspose.cloud/cells/tr/get-mincolumn-from-excel-worksheet/)
- [Get MaxColumn](https://docs.aspose.cloud/cells/tr/get-maxcolumn-from-excel-worksheet/)