---
title: "Excel Çalışma Sayfasında Bir Doğrulamayı Güncelle"
second_title: "Belge"
linktitle: "Güncelle"
type: docs
url: /tr/validations/update/
keywords: "Aspose.Cells Cloud, Excel doğrulama güncelleme, REST API, çalışma sayfası doğrulaması, Excel API"
description: "Aspose.Cells Cloud REST API kullanılarak bir Excel dosyasındaki çalışma sayfası doğrulamasının nasıl güncelleneceği, cURL örnekleri ve birden fazla programlama dili için SDK kod parçacıklarıyla açıklanmıştır."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API Kullanılarak Çalışma Sayfası Doğrulamasını Güncelleme"
---

Bu REST API, bir Excel çalışma sayfasında belirtilen dizine göre bir doğrulamayı günceller.

Bu uç noktayı çağırmadan önce, uygun kapsamlara sahip (örneğin, `Cells.ReadWrite`) bir JWT erişim belirteci edinin. Belirteci örneklerde gösterildiği gibi `Authorization` başlığına ekleyin.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **İstek Parametreleri**

| Parametre Adı    | Tür      | Konum | Açıklama                                                               |
| ---------------- | -------- | ----- | ---------------------------------------------------------------------- |
| name             | string   | path  | Çalışma kitabının dosya adı.                                            |
| sheetName        | string   | path  | Doğrulamanın bulunduğu çalışma sayfasının adı.                         |
| validationIndex  | integer  | path  | Güncellenecek doğrulamanın sıfır tabanlı dizini.                       |
| validation       | object   | body  | Güncellenmiş doğrulama ayarlarını tanımlayan bir JSON nesnesi.         |
| folder           | string   | query | Çalışma kitabının bulunduğu bulut depolama klasörü.                    |
| storageName      | string   | query | Kullanılan özel bir depolama hizmetinin adı (eğer varsa).              |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web hizmetlerini kolayca çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**Olası HTTP durum kodları**

| Kod  | Anlamı                                  | Açıklama |
|------|-----------------------------------------|---------|
| 200  | OK                                      | Doğrulama başarıyla güncellendi. |
| 400  | Bad Request                             | İstek bozuk veya gerekli parametreler eksik. |
| 401  | Unauthorized                            | Geçersiz veya eksik JWT belirteci. |
| 403  | Forbidden                               | Belirtecin yeterli kapsamları yok. |
| 404  | Not Found                               | Belirtilen çalışma kitabı, çalışma sayfası veya doğrulama dizini mevcut değil. |
| 500  | Internal Server Error                   | Sunucuda beklenmeyen bir hata oluştu. |

Hata işlemeyle ilgili daha fazla bilgi için <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud hata belgelerine</a> bakınız.

Ayrıca, yeni bir doğrulama eklemek veya mevcut birini silmek gibi ilgili işlemleri de inceleyebilirsiniz:

- [Çalışma sayfası doğrulaması ekleme](https://docs.aspose.cloud/cells/validations/add/)
- [Çalışma sayfası doğrulaması silme](https://docs.aspose.cloud/cells/validations/delete/)

## Bulut SDK Geliştirme Paketi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviyeli ayrıntıları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakınız.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracığınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}