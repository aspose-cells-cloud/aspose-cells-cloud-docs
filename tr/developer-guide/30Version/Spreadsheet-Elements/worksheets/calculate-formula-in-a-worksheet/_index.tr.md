---
title: "Excel çalışma sayfasında bir formül hesaplayın"
second_title: "Belge"
linktitle: "Hesapla"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, formül hesaplama, REST API, SDK'lar, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında formülleri hesaplayın. Birden fazla SDK'yı (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) destekler ve kullanıma hazır örnekler sunar."
weight: 20
ArticleTitle: "Excel çalışma sayfasında bir formül hesaplayın – Aspose.Cells Cloud Dokümantasyonu"
---

Bu REST API, bir çalışma sayfasındaki **formülün hesaplanmış değerini** döndürür. Uygulamanızdan doğrudan bir Excel formülünü **değerlendirmek** için kullanılabilir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **İstek parametreleri**

| Parametre Adı | Tür     | Konum  | Açıklama                                               |
| ------------- | ------- | ------ | ------------------------------------------------------ |
| name          | string  | path   | Excel dosyasının adı.                                  |
| sheetName     | string  | path   | Formülü içeren çalışma sayfasının adı.                 |
| formula       | string  | query  | Değerlendirilecek formül (örneğin, `SUM(A5:A10)`).    |
| folder        | string  | query  | Belgenin depolandığı klasör.                           |
| storageName   | string  | query  | Depolama hizmetinin adı (uygulanabilirse).             |

[OpenAPI Specifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula), genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Kimlik Doğrulama

Tüm istekler, `Authorization` başlığında geçerli bir **Bearer JWT belirteci** içermelidir:

```
Authorization: Bearer <your_jwt_token>
```

Belirteci, Aspose.Cells Cloud kimlik doğrulama kılavuzunda açıklanan OAuth 2.0 akışını takip ederek edinebilirsiniz.

### Olası yanıt durum kodları

| Kod | Açıklama                                              |
|-----|-------------------------------------------------------|
| 200 | İstek başarılı; formül değeri döndürülür.             |
| 400 | Geçersiz istek – eksik veya geçersiz parametreler.    |
| 401 | Yetkisiz – geçersiz veya eksik JWT belirteci.         |
| 404 | Bulunamadı – belirtilen dosya veya çalışma sayfası yok. |
| 500 | Sunucu iç hatası – sunucuda beklenmeyen bir durum oluştu. |

Aspose.Cells Cloud web hizmetlerini kolayca çağırmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bir formül sonucu istemenin nasıl gerçekleştirileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Kiti

API entegrasyonu yapmanın en hızlı yolu, bir SDK kullanmaktır. Bir SDK, düşük seviye ayrıntıları işler, böylece iş mantığınıza odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**Ayrıca bakınız:**  
- [Çalışma Sayfasını Al](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [Çalışma Sayfasını Güncelle](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [Tüm Formülleri Hesapla](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---