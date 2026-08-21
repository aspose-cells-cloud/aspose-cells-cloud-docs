---
title: "Excel çalışma sayfasından satır bilgilerini alın"
second_title: "Belge"
linktitle: "Satırlar"
type: docs
url: /tr/rows/get/rows/
aliases: [  /tr/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Satırları Al API, Excel çalışma sayfası satırları, REST API, cURL örneği, SDK örnekleri, .NET, Java, Python"
description: "Aspose.Cells Cloud REST API (v3.0) ile bir Excel çalışma sayfasından satır bilgilerini nasıl alacağınızı öğrenin. C#, Java, Python ve daha fazlası için uç nokta, parametreler, kimlik doğrulama, cURL ve SDK kod örneklerini içerir."
weight: 10
ArticleTitle: "Excel çalışma sayfasından satır bilgilerini alın – Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, bir Excel çalışma sayfasından satır bilgilerini alır.

**Önkoşullar**  
Bu uç noktayı çağırmak için `Authorization` başlığında geçerli bir JWT belirteci sağlamalısınız. Belirteç, Aspose.Cloud kimlik doğrulama akışı kullanılarak elde edilmeli ve Hücre işlemleri için gerekli kapsamları içermelidir. API, v3.0 sürümleme şemasını takip eder ve standart hız sınırlama politikalarına tabidir.

## GetWorksheetRows API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama                 |
| -------------- | ------ | -------- | -------------------- |
| name           | string | path     | Çalışma kitabının adı.   |
| sheetName      | string | path     | Çalışma sayfasının adı.  |
| folder         | string | query    | Çalışma kitabının klasörü. |
| storageName    | string | query    | Depo adı.    |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRows), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Yanıt kodları**

| Kod | Anlam                       | Açıklama                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK (Tamam)                          | İstek başarılı oldu ve satır bilgileri döndürüldü.                |
| 400  | Bad Request (Hatalı İstek)                 | İstek bozuk (örneğin, gerekli parametreler eksik).              |
| 401  | Unauthorized (Yetkisiz)                | Geçersiz veya eksik JWT belirteci.                                               |
| 404  | Not Found (Bulunamadı)                   | Belirtilen çalışma kitabı veya çalışma sayfası mevcut değil.                         |
| 500  | Internal Server Error (İç Sunucu Hatası)       | Sunucuda beklenmeyen bir hata oluştu.                                 |

## Cloud SDK Family (Bulut SDK Ailesi)

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları ele aldığı için projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl istek yapılacağını göstermektedir:

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```java
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family (Bulut SDK Ailesi)

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları ele aldığı için projenizin görevlerine odaklanabilirsiniz. Çalışma sayfası satırlarını alma için dil özelinde kod örnekleri aşağıdadır.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}