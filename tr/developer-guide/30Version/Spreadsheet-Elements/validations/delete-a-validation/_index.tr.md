---
title: "Çalışma Sayfası Doğrulamasını Sil – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /tr/validations/delete/
keywords: "Sil, çalışma sayfası doğrulaması, Aspose.Cells Cloud, Excel API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasından çalışma sayfası doğrulamasını nasıl sileceğinizi öğrenin. Uç nokta, parametreler, kimlik doğrulama ayrıntıları, cURL örneği, hata işleme ve SDK kod parçacıklarını içerir."
weight: 10
---

Bu REST API, bir Excel çalışma sayfasındaki sıfır‑tabanlı dizine göre bir çalışma sayfası doğrulamasını siler.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **İstek Parametreleri**

| Parametre Adı    | Tür      | Konum  | Açıklama                                          |
| ---------------- | -------- | ------ | ------------------------------------------------- |
| name             | string   | path   | Excel dosyasının adı.                             |
| sheetName        | string   | path   | Çalışma sayfasının adı.                           |
| validationIndex  | integer  | path   | Silinecek doğrulamanın sıfır‑tabanlı indeksi.     |
| folder           | string   | query  | Belgenin bulunduğu klasör.                        |
| storageName      | string   | query  | Depolama hizmetinin adı.                          |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetini çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bir doğrulamayı silmeyi göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                          |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.               |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.          |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                   |

## Bulut SDK Ailesi

Bu işlemi uygulamanıza entegre etmenin en hızlı yolu bir SDK kullanmaktır. SDK’lar düşük seviye ayrıntıları yöneterek size iş mantığına odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub Deposu](https://github.com/aspose-cells-cloud)'na bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak bir çalışma sayfası doğrulamasını nasıl sileceğinizi göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}