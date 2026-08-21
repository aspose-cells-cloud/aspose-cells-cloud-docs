---
title: "Aspose.Cells Cloud API ile Excel'de Sütunu Otomatik Boyutlandırma – Hızlı Kılavuz"
second_title: "Belge"
linktitle: "Sütun"
type: docs
url: /tr/worksheets/autofit/column/
aliases: [  /tr/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, sütunu otomatik boyutlandırma, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında bir sütunu (veya sütun aralığını) otomatik olarak yeniden boyutlandırmayı öğrenin. cURL ve SDK örneklerini (C#, Java, Python vb.) ve tüm istek/yanıt detaylarını içerir."
weight: 10
---

Bu REST API, bir Excel çalışma sayfasındaki tek bir sütunu veya bitişik bir sütun aralığının genişliğini otomatik olarak ayarlar.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### İstek parametreleri

| Parametre Adı     | Tür     | Konum   | Açıklama                                                                                         |
| ----------------- | ------- | ------- | ------------------------------------------------------------------------------------------------ |
| name              | string  | path    | Excel dosyasının adı.                                                                            |
| sheetName         | string  | path    | Çalışma sayfasının adı.                                                                          |
| firstColumn       | integer | query   | Otomatik boyutlandırılacak ilk sütunun sıfır tabanlı indeksi.                                   |
| lastColumn        | integer | query   | Otomatik boyutlandırılacak son sütunun sıfır tabanlı indeksi.                                   |
| autoFitterOptions | object  | body    | Otomatik boyutlandırma davranışını kontrol eden seçenekler (bkz. [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow          | integer | query   | Sütun genişliği hesaplanırken dikkate alınacak ilk satırın sıfır tabanlı indeksi.                |
| lastRow           | integer | query   | Sütun genişliği hesaplanırken dikkate alınacak son satırın sıfır tabanlı indeksi.                |
| folder            | string  | query   | Dosyanın bulunduğu depolama klasörü.                                                             |
| storageName       | string  | query   | Depolama hizmetinin adı.                                                                         |

### Hata yanıtları

| HTTP Durum Kodu | Anlam                                       | Örnek JSON gövdesi                                          |
| --------------- | ------------------------------------------- | ----------------------------------------------------------- |
| 400             | Geçersiz parametre(ler)                     | `{"Code":400,"Message":"Geçersiz parametre 'firstColumn'."}` |
| 401             | Yetkisiz – eksik veya geçersiz JWT belirteci | `{"Code":401,"Message":"Yetkilendirme başarısız."}`         |
| 404             | Dosya veya çalışma sayfası bulunamadı        | `{"Code":404,"Message":"'Sheet1' çalışma sayfası bulunamadı."}` |
| 500             | İç sunucu hatası                            | `{"Code":500,"Message":"Beklenmeyen bir hata oluştu."}`     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells Cloud hizmetlerini çağırmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, sütun otomatik boyutlandırma uç noktasını nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
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

## Bulut SDK Ailesi

API’yi uygulamanıza entegre etmenin en hızlı yolu bir SDK kullanmaktır. SDK’lar düşük seviyeli ayrıntıları yöneterek size iş mantığına odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’larla sütun otomatik boyutlandırma uç noktasını nasıl çağıracağınızı göstermektedir:

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