---
title: "Excel Çalışma Sayfasından MinRow Değerini Alın – Aspose.Cells Cloud API Referansı"
type: docs
url: /tr/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, Excel çalışma sayfası, REST API, minimum satır indeksi, bulut SDK'sı"
description: "Aspose.Cells Cloud REST API’si (v3.0) ile bir çalışma sayfasının minimum satır indeksini nasıl alacağınızı öğrenin. Tam kimlik doğrulamalı cURL isteği, yanıt şeması ve birden fazla dil için SDK örnekleri içerir."
ArticleTitle: "Excel Çalışma Sayfasından MinRow Değerini Alın – Aspose.Cells Cloud API Referansı"
---

Bu REST API, `cellOrMethodName` parametresi `minrow` olarak ayarlandığında bir Excel çalışma sayfasındaki minimum satır indeksini döndürür. Bu uç nokta, belirli bir çalışma sayfasındaki ilk dolu olmayan satırı (sıfır tabanlı) belirlemek için kullanılabilir.

- **cURL Örneği:**

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**İstek**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| Özellik          | Tür    | Gerekli | Açıklama                                              |
|-------------------|--------|---------|-------------------------------------------------------|
| `fileName`        | string | Evet    | Çalışma kitabının adı (örneğin `myWorkbook.xlsx`).   |
| `sheetName`       | string | Evet    | Hedef çalışma sayfası (örneğin `Sheet1`).            |
| `cellOrMethodName`| string | Evet    | Sabit değer `minrow`.                                 |
| `folder`          | string | Hayır   | Bulut depolama klasör yolu.                          |
| `storageName`     | string | Hayır   | Varsayılan olmayan bir depo kullanılıyorsa depo adı.|

**Yanıt**

Hizmet, `MinRow` özelliğini içeren bir JSON nesnesi döndürür; bu özellik, ilk dolu olmayan satırın indeksini (sıfır tabanlı) gösterir.

| HTTP Durum Kodu | Anlam                                   |
|-----------------|------------------------------------------|
| 200             | Başarılı – `MinRow` içeren JSON yükü.   |
| 401             | Yetkisiz – geçersiz veya eksik belirteç.|
| 404             | Çalışma kitabı veya çalışma sayfası bulunamadı. |
| 500             | Sunucu iç hatası.                        |

`MinRow` değeri, bir sayfadaki verilerin başlangıç noktasını hızlıca belirlemek gerektiğinde faydalıdır.

- **Aspose.Cells Cloud SDK'larını Kullanın**

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları yönetir, böylece projenize odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}
---