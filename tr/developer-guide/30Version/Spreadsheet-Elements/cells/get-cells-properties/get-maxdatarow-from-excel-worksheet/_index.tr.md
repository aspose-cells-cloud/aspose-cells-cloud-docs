---
title: "Excel Çalışma Sayfasından MaxDataRow'ı Al"
type: docs
url: /tr/get-maxdatarow-from-excel-worksheet/
weight: 50
keywords: "Excel, Aspose.Cells Cloud, REST API, MaxDataRow Al, Çalışma Sayfası"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabının belirtilen çalışma sayfasındaki veri içeren son satırın indeksini alır."
ArticleTitle: "Aspose.Cells Cloud API – Excel Çalışma Sayfasından MaxDataRow’ı Al"
---

Bu REST API, `cellOrMethodName` parametresi `maxdatarow` olarak ayarlandığında bir Excel dosyasındaki maksimum veri satırı indeksini döndürür.

- **cURL Örneği**

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatarow" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

*Not: İstek **HTTPS** üzerinden gönderilmeli ve geçerli bir OAuth2 bearer token içermelidir.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataRow": 57
}
```

**Olası HTTP durum kodları**

| Kod | Açıklama |
|------|-------------|
| 200 | Başarılı – maksimum veri satırı indeksini döndürür. |
| 401 | Yetkisiz – geçersiz veya eksik kimlik doğrulama jetonu. |
| 403 | Yetki Yok – çalışma kitabına erişim izni yetersiz. |
| 404 | Bulunamadı – belirtilen çalışma kitabı veya çalışma sayfası mevcut değil. |
| 500 | İç Sunucu Hatası – beklenmeyen sunucu koşulu. |

{{< /tab >}}

{{< /tabs >}}


- **Aspose.Cells Cloud SDK’larını Kullanma**

SDK kullanmak, geliştirme hızını en verimli şekilde artıran yoldur. Bir SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7b834250a25feb5b8a30500cf62cf7a9" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bkz.**

- <a href="https://docs.aspose.cloud/cells/get-maxrow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">Excel Çalışma Sayfasından MaxRow’ı Al</a>  
- <a href="https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">Excel Çalışma Sayfasından MaxColumn’u Al</a>  
- <a href="https://docs.aspose.cloud/cells/get-mindatarow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">Excel Çalışma Sayfasından MinDataRow’ı Al</a>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Aspose.Cells Cloud Get MaxDataRow",
  "description": "Belirtilen bir çalışma sayfasında veri içeren son satırın indeksini döndürür.",
  "url": "https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatarow",
  "method": "GET",
  "documentation": "https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/",
  "input": [
    {
      "name": "fileName",
      "valueRequired": true,
      "description": "Excel çalışma kitabının adı."
    },
    {
      "name": "sheetName",
      "valueRequired": true,
      "description": "Çalışma sayfasının adı."
    }
  ],
  "output": {
    "@type": "DataType",
    "name": "MaxDataRow",
    "description": "Veri içeren son satırın sıfıra tabanlı indeksi."
  }
}
</script>

*Son güncelleme: 2026-07-30*