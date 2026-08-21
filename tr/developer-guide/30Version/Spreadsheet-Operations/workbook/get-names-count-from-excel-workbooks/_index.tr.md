---
title: "Bir Excel Çalışma Kitabından İsimleri Alın"
second_title: "Belge"
linktitle: "İsimler"
type: docs
url: /tr/get-names-from-an-excel-file/
aliases:
  [
    /get-names-count-from-excel-workbooks/,
    /workbook/names/,
    /workbook/get/names/,
  ]
keywords: "Aspose.Cells, Bulut, Excel, Çalışma Kitabı, İsimler, REST API, SDK"
description: "Aspose.Cells Cloud REST API'sini kullanarak bir Excel çalışma kitabından tanımlı tüm isimleri alın. Kimlik doğrulama yönlendirmesini, cURL örneğini, yanıt şemasını, hata yönetimi ve SDK örneklerini içerir."
weight: 120
ArticleTitle: "Bir Excel Çalışma Kitabından İsimleri Alın – Aspose.Cells Cloud API"
---

Bu REST API, bir Excel çalışma kitabından tanımlı isimleri alır.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

## GetWorkbookNames API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

İstek parametreleri:

| Parametre Adı | Tür    | Konum | Açıklama                               |
| ------------- | ------ | ----- | -------------------------------------- |
| name          | string | path  | Çalışma kitabının dosya adı.           |
| folder        | string | query | Çalışma kitabını içeren klasör.        |
| storageName   | string | query | Kullanılacak depo adı.                |

İstek aşağıdaki HTTP başlıklarını içermelidir:

| Başlık         | Tür    | Açıklama                                 |
| -------------- | ------ | ---------------------------------------- |
| Authorization  | string | Bearer JWT belirteci (gerekli)           |
| Accept         | string | `application/json`                       |
| Content-Type   | string | `application/json` (gövde içeren istekler için) |

**Kimlik Doğrulama** – API, bir OAuth2/JWT bearer belirteci gerektirir. Belirteci, istemci kimliğiniz ve istemci sırrınız ile `https://api.aspose.cloud/connect/token` adresinden edinin ve her istekte `Authorization: Bearer <jwt token>` başlığını ekleyin.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, Aspose.Cells Cloud API’yi cURL ile nasıl çağıracığınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_Yanıt alanları_

- **Status** _(string)_ – İşlem durumu mesajı.
- **Names.link** _(object)_ – Koleksiyon için hyperlink bilgisi.
- **Names.Count** _(integer)_ – Döndürülen tanımlı isimlerin toplam sayısı.
- **Names.NameList** _(array)_ – İsim nesnelerinin listesi; her nesne gezinme ayrıntılarını içeren bir **link** nesnesi içerir.

**Hata yönetimi** – Hizmet aşağıdaki HTTP durum kodlarından birini döndürebilir:

| Kod | Anlam                 | Önerilen eylem                                                |
| --- | --------------------- | ------------------------------------------------------------- |
| 401 | Yetkisiz              | Geçerli bir JWT belirtecin sağlandığından emin olun.          |
| 404 | Bulunamadı            | Çalışma kitabının adı, klasörü ve deposunun doğru olduğunu kontrol edin. |
| 500 | Sunucu İç Hatası      | Sorun devam ederse daha sonra tekrar deneyin veya Aspose desteğine başvurun. |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK kullanmak, geliştirmenin en hızlı yoludur. SDK, düşük seviye detayları yönetir ve projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini farklı SDK’larla nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}