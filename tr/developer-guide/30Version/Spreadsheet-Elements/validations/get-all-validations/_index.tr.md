---
title: "Bir Excel Çalışma Sayfasından Tüm Çalışma Sayfası Doğrulamalarını Alın"
second_title: "Belge"
linktitle: "Tümünü Al"
type: docs
url: /tr/validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, çalışma sayfası doğrulamaları, REST API, tüm doğrulamaları al, SDK'lar"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından tüm çalışma sayfası doğrulamalarını alın. Hızlı entegrasyon için birden fazla SDK'yi (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) destekler."
weight: 10
---

Çalışma sayfası doğrulamaları, hücrelere girilebilecek veri türünü veya aralığını kısıtlamak için kurallar tanımlamanızı sağlar. Veri bütünlüğünü sağlamak için yaygın olarak kullanılırlar; örneğin girişleri belirli bir değer listesine, belirli bir tarih aralığına veya sayısal sınırlara kısıtlamak gibi.

Bu REST API, bir Excel çalışma sayfasındaki tüm çalışma sayfası doğrulamalarını getirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **İstek Parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama                                |
| -------------- | ------ | -------- | ----------------------------------------- |
| name           | string | path     | Excel belgesinin adı.                    |
| sheetName      | string | path     | Çalışma sayfasının adı.                   |
| folder         | string | query    | Belgenin depolandığı klasör yolu.         |
| storageName    | string | query    | Depolama hizmetinin adı.                  |

**Yanıt durum kodları**

| Kod | Açıklama                                    |
|------|---------------------------------------------|
| 200  | Başarılı istek – doğrulamalar listesi      |
| 401  | Yetkisiz – geçersiz veya eksik belirteç     |
| 404  | Bulunamadı – belge veya çalışma sayfası eksik |
| 500  | İç sunucu hatası                           |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. **Önkoşul:** `Authorization` başlığına geçerli bir JWT belirteci eklemeniz gerekir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "Değer 1 ile 100 arasında olmalıdır."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Seçenek1,Seçenek2,Seçenek3\"",
      "showErrorMessage": true,
      "errorMessage": "Listeden bir değer seçin."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Paketi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları kendisi yöneterek sizin projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}
---