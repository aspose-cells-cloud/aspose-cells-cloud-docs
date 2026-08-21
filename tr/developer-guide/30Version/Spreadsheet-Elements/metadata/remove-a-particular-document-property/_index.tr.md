---
title: "Belirli Bir Belge Özelliğini Silme"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /tr/document-properties/delete/
aliases: [  /tr/remove-a-particular-document-property/ ]
keywords: "Aspose.Cells, belge özelliği silme, Excel meta verisi API'si, REST, bulut SDK'sı, cURL örneği"
description: "Aspose.Cells Cloud REST API v3.0 ile bir Excel çalışma kitabından belirli bir belge özelliğini silin. C#, Java, Python ve diğerleri için hem cURL hem de SDK örneklerini içerir."
weight: 50
---

Bu REST API, bir çalışma kitabından bir belge özelliğini siler.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### İstek Parametreleri

| Parametre Adı | Tür     | Konum  | Gerekli | Açıklama                                           |
|---------------|---------|--------|---------|----------------------------------------------------|
| name          | string  | path   | Evet    | Excel çalışma kitabının adı.                       |
| propertyName  | string  | path   | Evet    | Silinecek belge özelliğinin adı.                   |
| folder        | string  | query  | Hayır   | Çalışma kitabının bulunduğu klasör yolu.           |
| storageName   | string  | query  | Hayır   | Depolama hizmetinin adı.                           |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty), herkese açık erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Hata Yanıtları

| HTTP Durumu | Açıklama                                                       | Örnek JSON                                                     |
|-------------|----------------------------------------------------------------|----------------------------------------------------------------|
| 400         | Geçersiz istek – gerekli parametreler eksik veya geçersiz değerler. | `{"Code":400,"Message":"Eksik gerekli parametre 'name'."}`     |
| 401         | Yetkisiz erişim – geçersiz veya eksik JWT belirteci.            | `{"Code":401,"Message":"Geçersiz erişim belirteci."}`          |
| 404         | Bulunamadı – çalışma kitabı veya belirtilen özellik mevcut değil. | `{"Code":404,"Message":"Belge özelliği bulunamadı."}`          |
| 500         | Sunucu iç hatası – sunucuda beklenmedik bir durum oluştu.       | `{"Code":500,"Message":"Beklenmedik bir hata oluştu."}`        |

## Bulut SDK Ailesi

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları ele alır ve böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine çeşitli SDK'lar kullanılarak nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}