---
title: "Biçim Koşulu Ekle"
type: docs
url: /tr/conditional-formattings/add-format-condition/
aliases: [  /tr/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, Koşullu Biçimlendirme API'si, Biçim Koşulu Ekle, Excel REST API, Cells API"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasına nasıl biçim koşulu ekleneceğini öğrenin. İstek sözdizimi, parametreler, güvenli cURL örneği ve SDK kod parçacıklarını içerir."
ArticleTitle: "Biçim Koşulu Ekle – Aspose.Cells Cloud API Dokümantasyonu"
weight: 50
---

Bu REST API, bir çalışma sayfasına bir biçim koşulu ekler.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API'leri güvenlidir ve [JWT token tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### İstek Parametreleri

| Parametre Adı | Tür     | Konum  | Açıklama                                                                     |
| ------------- | ------- | ------ | ---------------------------------------------------------------------------- |
| name          | string  | path   | Excel çalışma kitabının adı.                                                  |
| sheetName     | string  | path   | Biçimlendirilecek aralığı içeren çalışma sayfasının adı.                      |
| index         | integer | path   | Eklenecek veya değiştirilecek biçim koşulunun sıfır tabanlı indeksi.         |
| cellArea      | string  | query  | Koşulun uygulanacağı hücre aralığı (örneğin, `A1:C3`).                        |
| type          | string  | query  | Koşul türü (örneğin, `Expression`, `CellValue`).                             |
| operatorType  | string  | query  | Koşul için operatör (örneğin, `Between`, `Equal`).                           |
| formula1      | string  | query  | Koşul tarafından kullanılan ilk formül veya değer.                            |
| formula2      | string  | query  | İkinci formül veya değer (özellikle `Between` gibi bazı operatörler için gerekli). |
| folder        | string  | query  | Çalışma kitabının bulunduğu depolama klasörü.                                 |
| storageName   | string  | query  | Depolama hizmetinin adı (örneğin, `Default`).                                |

### Hata Yanıtları

| HTTP Kodu | Neden                                              | Örnek Gövde                                                         |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Geçersiz İstek – eksik veya geçersiz parametreler. | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Yetkisiz – eksik veya geçersiz JWT token.         | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Bulunamadı – çalışma kitabı veya çalışma sayfası yok. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | İç Sunucu Hatası – beklenmeyen sunucu hatası.      | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

### Başarılı Yanıt

| HTTP Kodu | Neden              | Örnek Gövde                               |
| --------- | ------------------ | ------------------------------------------ |
| **200**   | Tamam – koşul başarıyla eklendi veya güncellendi. | `{ "Code": "200", "Status": "OK" }` |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells API'lerini çağırmak için **cURL** kullanabilirsiniz. Aşağıdaki örnek, boş bir JSON gövdesiyle birlikte tam bir isteği göstermektedir.

### cURL Örneği

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Paketi

Bir SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)'na bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}