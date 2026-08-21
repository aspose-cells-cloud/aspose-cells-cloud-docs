---
title: "Bir Excel çalışma sayfasını yeniden görünür hale getirme"
second_title: "Belge"
linktitle: "Görünür hale getir"
type: docs
url: /worksheets/unhide/
aliases: [/unhide-excel-worksheets/]
keywords: "Aspose.Cells, çalışma sayfasını görünür hale getir, Excel API, bulut elektronik tablo, REST, çalışma sayfası görünürlüğü, Excel çalışma kitabı"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabında bir çalışma sayfasını yeniden görünür hale getirmeyi öğrenin. İstek detaylarını, cURL örneklerini ve birden fazla programlama dili için SDK kod parçacıklarını içerir."
weight: 60
---

Bu REST API, bir Excel çalışma kitabında bir çalışma sayfasını **yeniden görünür hale getirmek** için bir uç nokta sağlar.

**Önkoşullar**  
Bu işlemi çağırmadan önce şunlara sahip olmalısınız:

* `Authorization` başlığına eklenmiş geçerli bir Aspose Cloud erişim belirteci (JWT).  
* `folder` ve `storageName` sorgu parametreleriyle belirttiğiniz desteklenen depolama konumunda depolanmış çalışma kitabı.  
* Çalışma kitabının Aspose.Cells tarafından desteklenen bir formatta olması gerekir (örneğin, `.xls`, `.xlsx`, `.xlsm`).  

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **İstek parametreleri**

| Parametre Adı | Tür      | Konum | Açıklama                                |
| ------------- | -------- | ----- | --------------------------------------- |
| name          | string   | path  | Belge adı.                              |
| sheetName     | string   | path  | Çalışma sayfası adı.                    |
| isVisible     | boolean  | query | Yeni çalışma sayfası görünürlük değeri (`true`). |
| folder        | string   | query | Belge klasörü.                          |
| storageName   | string   | query | Depo adı.                               |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet), web tarayıcınızdan doğrudan REST etkileşimlerinde bulunabilmeniz için genel olarak erişilebilir bir programlama arayüzü tanımlar.

Aspose.Cells web hizmetlerini kolayca çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # <jwt token> ifadesini erişim belirtecinizle değiştirin
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Olası yanıt kodları**

| HTTP Kodu | Anlamı                                      | Örnek Gövde (uygulanıyorsa)                               |
|-----------|---------------------------------------------|------------------------------------------------------------|
| 200       | Çalışma sayfası görünürlüğü başarıyla güncellendi | `{ "Code": 200, "Status": "OK" }`                          |
| 400       | Geçersiz istek – eksik veya geçersiz parametreler | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401       | Yetkisiz erişim – eksik veya geçersiz JWT belirteci | `{ "Code": 401, "Message": "Authentication failed." }`     |
| 404       | Bulunamadı – çalışma kitabı veya çalışma sayfası mevcut değil | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500       | Sunucu iç hatası                            | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Kiti

Bir SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları yöneterek projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}