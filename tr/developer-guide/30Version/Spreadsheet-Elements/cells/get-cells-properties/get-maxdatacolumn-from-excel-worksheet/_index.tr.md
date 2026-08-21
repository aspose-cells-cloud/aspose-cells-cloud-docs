---
title: "Aspose.Cells Cloud API – Bir Excel Çalışma Sayfasının MaxDataColumn Değerini Alın (v3.0)"
type: docs
url: /get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, MaxDataColumn Al, Excel çalışma sayfası, REST API, v3.0, SDK"
description: "Belirtilen bir çalışma sayfasında veri içeren en yüksek sütun indeksini Aspose.Cells Cloud REST API’si (v3.0) kullanarak alın. İstek detaylarını, örnek yanıt ve SDK örneklerini içerir."
ArticleTitle: "Aspose.Cells Cloud API – Bir Excel Çalışma Sayfasının MaxDataColumn Değerini Alın (v3.0)"
---

Bu REST API, `cellOrMethodName` parametresi `maxdatacolumn` olarak ayarlandığında bir Excel çalışma sayfasındaki maksimum veri sütun indeksini döndürür.

## **cURL Örneği**

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**İstek Detayları**  
- **HTTP Yöntemi:** `GET`  
- **Uç nokta deseni:** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **Yol parametreleri:**  
  - `fileName` – Excel dosyasının adı (örneğin, `myWorkbook.xlsx`).  
  - `sheetName` – Çalışma sayfasının adı (örneğin, `Sheet1`).  
- **Başlıklar:**  
  - `Authorization: Bearer <access_token>` (zorunlu)  
  - `Accept: application/json` (önerilir)  

**Parametreler**

| Parametre | Konum | Tür   | Zorunlu | Açıklama |
|-----------|--------|--------|----------|-------------|
| `fileName` | Yol     | string | Evet      | Bulut depolama alanında saklanan Excel dosyasının adı. |
| `sheetName` | Yol   | string | Evet      | Maksimum veri sütununun alınacağı çalışma sayfası. |
| `cellOrMethodName` | Yol | string | Evet | Bu işlemi çağırmak için `maxdatacolumn` olarak ayarlanmalıdır. |

**Yanıtlar**

| Durum Kodu | Açıklama                     | Örnek Payload |
|-------------|---------------------------------|-----------------|
| 200         | Başarılı – maksimum veri sütun indeksini döndürür. | `{ "MaxDataColumn": 12 }` |
| 401         | Yetkisiz – geçersiz veya eksik erişim belirteci. | `{ "error": "Invalid authentication." }` |
| 404         | Bulunamadı – dosya veya çalışma sayfası mevcut değil. | `{ "error": "Resource not found." }` |
| 500         | İç Sunucu Hatası – beklenmedik bir durum oluştu. | `{ "error": "Server error." }` |

**Hata İşleme**  
İstek başarısız olursa, HTTP durum kodunu ve yanıt gövdesindeki `error` mesajını inceleyin. Erişim belirtecinizin geçerli olduğundan ve belirtilen dosya ile çalışma sayfasının Aspose Cloud depolama alanınızda mevcut olduğundan emin olun.

- **Aspose.Cells Cloud SDK’larını Kullanın**

SDK kullanmak, geliştirme sürecini hızlandırmak için en verimli yoldur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkânı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}