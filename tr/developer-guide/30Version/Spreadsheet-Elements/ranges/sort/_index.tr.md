---
title: Aralık Sıralama
second_title: "Belge"
linktitle: "Sırala"
type: docs
keywords: "Aralık Sıralama, Aspose.Cells Cloud, REST API, Elektronik Tablo, Excel, API"
url: /tr/ranges/sort/
description: Aspose.Cells Cloud kullanarak bir defter içindeki hücre aralığını sıralamak için bir API sağlar.
weight: 20
---

Bu REST API, belirli bir hücre aralığını sıralar.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort
```

İstek parametreleri:

| Parametre Adı | Tür   | Konum | Açıklama                                        |
|---------------|-------|-------|-------------------------------------------------|
| name          | String | Yol   | Defter adı.                                     |
| sheetName     | String | Yol   | Çalışma sayfası adı.                            |
| rangeOperate  | Class  | Gövde | Aralık Sıralama istek nesnesi.                  |
| folder        | String | Sorgu | Orijinal defterin bulunduğu klasör.             |
| storageName   | String | Sorgu | Depo adı.                                       |

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell
# (Yanıt örneği burada gösterilecektir)
```

{{< /tab >}}
{{< /tabs >}}

## Bulut SDK Geliştirme Seti

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen GitHub deposunu kontrol edin.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeSort.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeSort.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeSort.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeSort.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeSort.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeSort.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeSort.go" >}}

{{< /tab >}}

{{< /tabs >}}