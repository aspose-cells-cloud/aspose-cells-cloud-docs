---
title: "Excel Çalışma Sayfasına Bir Şekil Ekleyin"
second_title: "Belge"
linktitle: "Ekle"
type: docs
url: /shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: "Aspose.Cells, şekil ekle, Excel, REST API, bulut SDK, shapeDTO, çizim türü"
description: "Aspose.Cells Cloud REST API v3.0 kullanarak Excel çalışma sayfasına şekil (yay, çizgi, dikdörtgen vb.) nasıl ekleneceğini öğrenin. İstek sözdizimi, gerekli parametreler, kimlik doğrulama adımları ve örnek SDK kodunu içerir."
weight: 30
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Sayfasına Bir Şekil Ekleyin"
---

Bu REST API, Excel çalışma sayfasına bir şekil ekler.  
Uç nokta **API sürümü v3.0**’a aittir; Aspose Cloud OAuth2 akışı (istemci kimliği/istemci sırrı) ile alınan bir JWT erişim belirteci kullandığınızdan ve bunu `Authorization: Bearer <token>` başlığında kullandığınızdan emin olun.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **İstek parametreleri**

| Parametre Adı   | Tür    | Konum | Açıklama                                                                                           |
| ---------------- | ------ | ----- | -------------------------------------------------------------------------------------------------- |
| name             | string | path  | Belge adı.                                                                                         |
| sheetName        | string | path  | Çalışma sayfası adı.                                                                               |
| shapeDTO         | object | body  | Eklenecek şekli açıklayan JSON nesnesi (tam şema için OpenAPI spesifikasyonuna bakın).           |
| drawingType      | string | query | Şekil nesne türü (örneğin, `arc`, `line`, `rectangle`).                                            |
| upperLeftRow     | integer| query | Şeklin sol üst köşesinin satır indeksi.                                                            |
| upperLeftColumn  | integer| query | Şeklin sol üst köşesinin sütun indeksi.                                                            |
| top              | integer| query | Şeklin üst kenarından itibaren dikey ofset (piksel cinsinden).                                     |
| left             | integer| query | Şeklin sol kenarından itibaren yatay ofset (piksel cinsinden).                                     |
| width            | integer| query | Şeklin genişliği (piksel cinsinden).                                                               |
| height           | integer| query | Şeklin yüksekliği (piksel cinsinden).                                                              |
| folder           | string | query | Belgeyi içeren klasör.                                                                             |
| storageName      | string | query | Depo adı.                                                                                          |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape), herkese açık erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
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
  "Status": "OK",
  "ShapeId": 5
}
```

_Başarılı yanıt, HTTP durum kodunu, metinsel durumu ve yeni oluşturulan şeklin tanımlayıcısını (`ShapeId`) döndürür._

{{< /tab >}}

{{< /tabs >}}

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.              |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırnını aşıyor.          |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                   |

Typical error responses include:

- **400 Bad Request** – eksik veya geçersiz parametreler.  
- **401 Unauthorized** – geçersiz veya eksik JWT belirteci.  
- **404 Not Found** – belirtilen çalışma sayfası veya belge mevcut değil.

Her hata, `Code` ve `Message` alanlarını içeren bir JSON nesnesi olarak döndürülür.

## Cloud SDK Family

Bir SDK kullanmak, geliştirme hızını en hızlı yoldan artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları ele alır böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini farklı SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}