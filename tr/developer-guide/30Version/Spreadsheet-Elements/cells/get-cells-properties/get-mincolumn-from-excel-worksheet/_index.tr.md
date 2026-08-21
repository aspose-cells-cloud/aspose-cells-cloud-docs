---
title: "Excel Çalışma Sayfasından MinColumn Değerini Alın"
type: docs
url: /tr/get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, MinColumn Al, Çalışma Sayfası, SDK, Bulut API
description: Aspose.Cells Cloud REST API aracılığıyla bir Excel dosyasının çalışma sayfasında veri içeren minimum sütun indeksini alın.
ArticleTitle: "Excel Çalışma Sayfasından MinColumn Değerini Alın - Aspose.Cells Cloud API"
---

Bu REST API, `cellOrMethodName` parametresi `mincolumn` olarak ayarlandığında bir Excel çalışma sayfasında veri içeren minimum sütun indeksini döndürür.

- **cURL Örneği**

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**İstek ayrıntıları**

| Parametre | Tür | Gerekli | Açıklama |
|-----------|------|----------|-------------|
| `cellOrMethodName` | string | Evet | İşlemi belirtmek için sabit değer `mincolumn`. |
| `folder` | string | Hayır | Çalışma kitabını içeren klasörün yolu (kök değilse). |
| `storageName` | string | Hayır | Kullanılacak Aspose Cloud depo adı. |

**Yanıt ayrıntıları**

API, tek bir özellik içeren bir JSON nesnesi döndürür:

```json
{
  "MinColumn": tamsayı   // Veri içeren en soldaki sütunun sıfır tabanlı indeksi.
}
```

Olası HTTP durum kodları:

- **200 OK** – Başarılı istek, `MinColumn` değerini döndürür.  
- **401 Yetkisiz** – Eksik veya geçersiz kimlik doğrulama jetonu.  
- **404 Bulunamadı** – Belirtilen çalışma kitabı, çalışma sayfası veya hücre aralığı mevcut değil.  
- **500 İç Sunucu Hatası** – Beklenmeyen sunucu hatası.

- **Aspose.Cells Cloud SDK’larını Kullanın**

SDK kullanmak, geliştirme yapmanın en verimli yoludur. SDK, düşük seviyeli ayrıntıları soyutlayarak projenizin mantığına odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}