---
title: "Excel Çalışma Sayfasının Son Hücresini Alın – Aspose.Cells Cloud API (v4.0)"
type: docs
url: /tr/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, son hücreyi al, elektronik tablo, bulut"
description: "Aspose.Cells Cloud REST API v4.0 kullanarak bir Excel çalışma sayfasının son hücre adresini alın. İstek detaylarını, cURL örneğini, JSON yanıtını ve SDK örneklerini içerir."
ArticleTitle: "Excel Çalışma Sayfasının Bitiş Hücresini Alın – Aspose.Cells Cloud API v4.0"
---

Bu REST API, `cellOrMethodName` parametresi `endcell` olarak ayarlandığında bir Excel çalışma sayfasının **bitiş hücresini (endcell)** döndürür.

**Genel Bakış**  
**Son Hücreyi Al** işlemi, belirtilen bir çalışma sayfasındaki son kullanılan hücrenin adresini döndürür. Çalışma kitabının tamamını taramadan sayfanın etkin veri aralığını belirlemek için kullanışlıdır.

- **cURL Örneği.**

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<More Info>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Parametreler
| Parametre            | Tür    | Gerekli  | Açıklama |
|----------------------|--------|----------|----------|
| `fileName`           | string | Evet     | Bulutta depolanan Excel dosyasının adı. |
| `worksheetName`      | string | Evet     | Son hücrenin alınacağı çalışma sayfasının adı. |
| `cellOrMethodName`   | string | Evet     | Bu işlemin çağrılması için **`endcell`** olarak ayarlanmalıdır. |
| `folder` *(isteğe bağlı)*| string | Hayır  | Çalışma kitabının bulunduğu bulut klasör yolu. |
| `storageName` *(isteğe bağlı)*| string | Hayır | Depolama adı. Belirtilmezse varsayılan depolama kullanılır. |

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (Tamam)                  | Süzgeç başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (İçerik Çok Büyük) | Yüklenen dosya boyut sınırını aşar. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

- **Aspose.Cells Cloud SDK’larını Kullanın**

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerinin çeşitli SDK’lar kullanılarak nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_Yakında açılacak._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

Hücre gezinmesiyle ilgili diğer işlemler için lütfen **[İlk Hücreyi Alın](/tr/get-first-cell-of-excel-worksheet/)** ve **[Maksimum Satırı Alın](/tr/get-max-row-of-worksheet/)** konularına bakın.
---