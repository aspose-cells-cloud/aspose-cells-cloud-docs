---
title: "Excel Çalışma Sayfasından MaxRow Değerini Alın"
type: docs
url: /tr/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Excel Çalışma Sayfasında Maksimum Satır Numarasını Alın – Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, Bulut SDK, Elektronik Tablo, Çalışma Sayfası, GetMaxRow"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasındaki çalışma sayfasının maksimum satır numarasını nasıl alacağınızı öğrenin. İsteğin sözdizimi, yanıt şeması, SDK örnekleri ve kullanım notlarını içerir."
---

Bu REST API, `cellOrMethodName` parametresi `maxrow` olarak ayarlandığında bir Excel çalışma sayfasındaki **maksimum satır numarasını** döndürür.

- **cURL Örneği**

{{< tabs tabTotal="2" tabID="11" tabName11="İsteğin" tabName12="Yanıtın" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Aspose.Cells Cloud SDK’larını Kullanın**

SDK kullanmak, geliştirme sürecini hızlandırmanın en verimli yoldur. SDK, düşük seviye ayrıntıları yöneterek projenizin mantığına odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**API Referansı**

| Öğe | Detaylar |
|------|---------|
| **Metod** | `GET` |
| **Uç Nokta** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **Yol Parametreleri** | `fileName` – Excel dosyasının adı (zorunludur) <br> `sheetName` – çalışma sayfasının adı (zorunludur) |
| **Sorgu Parametreleri** | `folder` – depoda bulunan klasör yolu (isteğe bağlı) <br> `storageName` – depo adı (isteğe bağlı) |
| **Başarılı Yanıt** | `200 OK` <br> ```json { "MaxRow": integer } ``` |
| **Hata Yanıtları** | `400 Bad Request` – geçersiz parametreler <br> `401 Unauthorized` – kimlik doğrulama hatası <br> `404 Not Found` – dosya veya çalışma sayfası bulunamadı |

**Ön Gereksinimler**

- Geçerli bir Aspose Cloud kimlik doğrulama belirteci.  
- Hedef çalışma kitabının Aspose Cloud deposuna yüklenmiş olması veya herkese açık bir URL üzerinden erişilebilir olması gerekir.  

**Notlar**

- İşlem, API sürümünde **v3.0** ve sonraki sürümlerde kullanılabilir.  
- Döndürülen `MaxRow` değeri, kullanılan en yüksek satır indeksine (1‑tabanlı) karşılık gelir. Boş bir çalışma sayfası için bu değer genellikle `1`’dir.  

Aşağıdaki SDK örnekleri, farklı programlama dillerinde bu işlemi nasıl çağıracağınızı göstermektedir.