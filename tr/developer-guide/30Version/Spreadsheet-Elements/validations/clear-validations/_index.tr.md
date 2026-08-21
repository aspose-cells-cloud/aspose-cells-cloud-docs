---
title: "Tüm Çalışma Sayfası Doğrulamalarını Sil – Aspose.Cells Cloud API"
second_title: "Dokümantasyon"
linktitle: "Sil"
type: docs
url: /tr/validations/clear/
keywords: "Aspose.Cells Cloud, Çalışma sayfası doğrulamalarını sil, Excel, REST API, Elektronik tablo doğrulaması, API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasındaki bir çalışma sayfasından tüm veri doğrulama kurallarını kaldırın. Kimlik doğrulama adımlarını, istek detaylarını, cURL örneğini, yanıt şemasını, hata işleme ve SDK snippet'lerini içerir."
weight: 10
---

**Ön Gereksinimler**

- Geçerli bir Aspose Cloud hesabı.
- Aspose Cloud kimlik doğrulama API'si (`/connect/token`) aracılığıyla alınmış geçerli bir JWT erişim belirteci.
- Çalışma kitabının Aspose Cloud depo alanınızda saklanması gerekir (veya uygun `folder`/`storageName` sorgu parametreleri sağlanmalıdır).

Bu REST API, bir Excel çalışma sayfasındaki tüm çalışma sayfası doğrulamalarını siler.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **İstek Parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama                                                 |
| ------------- | ----- | ----- | -------------------------------------------------------- |
| name          | string | path  | Excel belgesinin adı.                                    |
| sheetName     | string | path  | Doğrulamaların bulunduğu çalışma sayfasının adı.         |
| folder        | string | query | Belgenin saklandığı klasör.                              |
| storageName   | string | query | Depo hizmetinin adı.                                     |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation), herkese açık bir erişilebilir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, JWT belirteci elde ettikten sonra API'yi cURL ile nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Hata İşleme

| HTTP Durum Kodu | Anlamı                | Açıklama                                                   |
| --------------- | --------------------- | ---------------------------------------------------------- |
| 400             | Geçersiz İstek        | İstek bozuk veya gerekli parametreler eksik.               |
| 401             | Yetkisiz              | JWT belirteci eksik, geçersiz veya süresi dolmuş.          |
| 404             | Bulunamadı            | Belirtilen çalışma kitabı veya çalışma sayfası mevcut değil. |
| 500             | Sunucu İç Hatası      | Sunucu tarafında beklenmedik bir hata oluştu.              |

Hata yükü, `Code` ve `Message` alanlarını içeren aynı JSON yapısını takip eder; örneğin:

```json
{
  "Code": 401,
  "Message": "Geçersiz veya süresi dolmuş belirteç."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları soyutlayarak iş mantığına odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK'lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}