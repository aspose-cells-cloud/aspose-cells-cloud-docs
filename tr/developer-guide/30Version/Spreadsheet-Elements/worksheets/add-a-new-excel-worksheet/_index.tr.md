---
title: "Bir Excel Çalışma Sayfası Ekleyin"
ArticleTitle: "Bir Excel Çalışma Sayfası Ekleyin - Aspose.Cells Cloud API Kılavuzu"
second_title: "Belge"
linktitle: "Ekle"
type: docs
url: /worksheets/add/
aliases: [/add-a-new-excel-worksheet/]
keywords: "Excel çalışma sayfası ekle, Aspose.Cells Cloud, REST API, çalışma sayfası ekle, Excel çalışma kitabı, API isteği"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabına yeni bir çalışma sayfası eklemenin adım adım kılavuzu; istek detaylarını, bir cURL örneğini ve birden fazla dil için SDK kod parçacıklarını içerir."
weight: 20
---

Bu REST API, mevcut bir çalışma kitabına yeni bir çalışma sayfası ekler.

**Önkoşullar**: Bu uç noktayı çağırmak için geçerli bir Aspose Cloud kimlik doğrulama belirteciniz olmalıdır, hedef çalışma kitabının Aspose Cloud depoya yüklenmiş olması gerekir ve özel bir depo kullanıyorsanız depo adını bilmelisiniz.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **İstek parametreleri**

| Parametre Adı | Tür      | Konum | Açıklama                                              |
| ------------- | -------- | ----- | ----------------------------------------------------- |
| name          | string   | path  | Çalışma kitabı dosyasının adı.                        |
| sheetName     | string   | path  | Oluşturulacak yeni çalışma sayfasının adı.           |
| position      | integer  | query | Sayfanın ekleneği sıfır tabanlı konum.                |
| sheettype     | string   | query | Yeni sayfanın türü (örn., **Chart**, **Dialog**).    |
| folder        | string   | query | Çalışma kitabının bulunduğu klasör.                   |
| storageName   | string   | query | Aspose Cloud deposunun adı.                           |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet), herkese açık bir erişilebilir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, Cloud API'ye cURL ile nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**Olası yanıt durum kodları**

| Durum Kodu | Açıklama                                             |
|-----------|------------------------------------------------------|
| 200       | Çalışma sayfası başarıyla eklendi.                   |
| 400       | Geçersiz istek – geçersiz parametreler.             |
| 401       | Yetkisiz erişim – kimlik doğrulama belirteci eksik/geçersiz. |
| 404       | Bulunamadı – çalışma kitabı veya klasör mevcut değil. |
| 500       | İç sunucu hatası – beklenmeyen durum.                |

## Bulut SDK Grubu

Bir SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK, düşük seviye detayları soyutlayarak projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---