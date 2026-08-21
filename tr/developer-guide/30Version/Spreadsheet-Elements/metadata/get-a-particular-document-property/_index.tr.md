---
title: "Belirli Bir Belge Özelliğini Alın"
second_title: "Belge"
linktitle: "Al"
type: docs
url: /tr/document-properties/get/
aliases: [  /tr/get-a-particular-document-property/ ]
keywords: "Aspose.Cells, Bulut API, Belge Özelliğini Al, Excel meta verisi, REST GET, SDK örnekleri"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasından adı verilen bir belge özelliğini (örneğin Yazar, Başlık) alın. cURL örneği, SDK snippet’leri ve yanıt şemasını içerir."
weight: 20
---

Bu REST API, belirli bir adla belge özelliğini okur.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### İstek Parametreleri

| Parametre Adı  | Tür    | Konum  | Açıklama                                            |
| -------------- | ------ | ------ | --------------------------------------------------- |
| name           | string | path   | Excel dosyasının adı.                               |
| propertyName   | string | path   | Alınacak belge özelliğinin adı.                     |
| folder         | string | query  | Dosyayı içeren klasör (isteğe bağlı).               |
| storageName    | string | query  | Depo adı (isteğe bağlı).                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL komut satırı aracı**nı kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Yazar",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
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

### Yanıt Ayrıntıları

API tarafından döndürülen JSON nesnesi aşağıdaki alanları içerir:

| Alan                            | Tür     | Açıklama                                                       |
| ------------------------------- | ------- | -------------------------------------------------------------- |
| **DocumentProperty.Name**       | string  | Özelliğin adı (örneğin `Author`).                               |
| **DocumentProperty.Value**      | string  | Özelliğin değeri. Ayarlanmamışsa boş olabilir.                  |
| **DocumentProperty.BuiltIn**    | boolean | Özelliğin yerleşik Excel özelliği olup olmadığını gösterir.     |
| **DocumentProperty.link.Href**  | string  | Özellik kaynağına olan göreli URL.                             |
| **DocumentProperty.link.Rel**   | string  | İlişki türü; genellikle `self`.                                |
| **DocumentProperty.link.Title** | string  | İnsan tarafından okunabilir başlık (`null` olabilir).           |
| **DocumentProperty.link.Type**  | string  | Bağlantılı kaynağın MIME türü (`null` olabilir).               |
| **Code**                        | integer | Hizmet tarafından döndürülen HTTP durum kodu.                  |
| **Status**                      | string  | Durumun metinsel açıklaması (örneğin `OK`).                    |

### Hata Yanıtları

| HTTP Durumu | Kod                    | Açıklama                                          |
| ----------- | ---------------------- | ------------------------------------------------- |
| 400         | `InvalidParameter`     | Bir veya daha fazla istek parametresi geçersiz.  |
| 401         | `AuthenticationFailed` | Eksik veya geçersiz JWT jetonu.                  |
| 404         | `PropertyNotFound`     | Belirtilen belge özelliği mevcut değil.          |
| 500         | `InternalError`        | Sunucuda beklenmeyen bir hata oluştu.            |

Tipik bir hata gövdesi şu şekildedir:

```json
{
  "Code": 404,
  "Status": "Özellik bulunamadı"
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları kendisi yönetir, böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Bulut SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine farklı SDK’lar kullanılarak nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Terimler

| Terim                 | Tanım                                                                                      |
| --------------------- | ------------------------------------------------------------------------------------------ |
| **Belge Özelliği**    | Bir Excel defteriyle ilişkili meta veri parçası (örneğin Yazar, Başlık, Oluşturulma Tarihi). |
| **Meta Veri**         | Diğer verileri açıklayan veri için genel terim; bu bağlamda belge özellikleri kastedilir.   |
| **Özel Özellik**      | Yerleşik özellik setinde bulunmayan kullanıcı tanımlı bir özellik.                        |

### Sık Sorulan Sorular

**S:** _Aspose Cloud’da depolanan bir Excel dosyasının Yazar özelliğini nasıl alabilirim?_  
**C:** Geçerli bir Bearer jetonu ile `https://api.aspose.cloud/v3.0/cells/{dosyaAdı}/documentproperties/author` adresine bir GET isteği gönderin. Yanıt JSON’unda `DocumentProperty.Name = "Yazar"` ve `Value` alanı bulunur.

**S:** _İstenen özellik mevcut değilse hangi hata döndürülür?_  
**C:** API, HTTP 404 durumu ile birlikte `Code: 404` ve `Status: "Özellik bulunamadı"` içeren bir JSON gövdesi döndürür.

**S:** _Dosya varsayılan depoda bulunuyorsa `storageName` belirtmem gerekiyor mu?_  
**C:** Hayır. `storageName` sorgu parametresi isteğe bağlıdır; hesabınız için yapılandırılmış varsayılan depoyu kullanmak için bu parametreyi atlayın.

---