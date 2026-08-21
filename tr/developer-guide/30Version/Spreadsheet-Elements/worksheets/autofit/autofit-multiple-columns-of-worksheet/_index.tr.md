---
title: "Excel Çalışma Sayfasında Birden Fazla Sütunu Otomatik Uyarlama"
second_title: "Belge"
linktitle: "Sütunlar"
type: docs
url: /worksheets/autofit/columns/
aliases: [/autofit-multiple-columns-of-worksheet/]
keywords: "Aspose.Cells, sütunları otomatik uyarlama, Excel API, bulut tablolu hesaplama, REST"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasında birden fazla sütunu otomatik uyarlamanın nasıl yapıldığını öğrenin. Uç nokta, parametreler, cURL örneği, hata yönetimi ve C#, Java, Python ve daha fazlası için SDK kod parçacıklarını içerir."
weight: 20
---

Bu REST API, bir Excel çalışma sayfasında **birden fazla sütunu** otomatik olarak ayarlar.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **İstek Parametreleri**

| Parametre Adı       | Tür      | Konum  | Açıklama                                                                                                                                   |
| ------------------- | -------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string   | path   | Dosya adı.                                                                                                                                  |
| sheetName           | string   | path   | Çalışma sayfası adı.                                                                                                                        |
| firstColumn         | integer  | query  | Başlangıç sütun indeksi.                                                                                                                    |
| lastColumn          | integer  | query  | Bitiş sütun indeksi.                                                                                                                        |
| autoFitterOptions\* | object   | body   | Otomatik uyarlama seçenekleri (bkz. [Otomatik Uyarlama Seçenekleri](/cells/auto-fitter-options/)). `AutoFitMergedCells`, `IgnoreHidden` ve `OnlyAuto` içerir. |
| firstRow            | integer  | query  | Otomatik uyarlama için başlangıç satır indeksi (**isteğe bağlı**).                                                                          |
| lastRow             | integer  | query  | Otomatik uyarlama için bitiş satır indeksi (**isteğe bağlı**).                                                                              |
| folder              | string   | query  | Depolama içindeki klasör yolu (**isteğe bağlı**).                                                                                          |
| storageName         | string   | query  | Depolama adı (**isteğe bağlı**).                                                                                                            |

\* Parametre adı, ilgili belgelendirmeye yönlendiren bir bağlantı olarak gösterilir.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istekte bulunmanın nasıl yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## Bulut SDK Geliştirme Grubu

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları işler; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerine çeşitli SDK'lar kullanarak nasıl istekte bulunacağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}