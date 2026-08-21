---
title: "Excel Çalışma Sayfasından OLE Nesnesini Alın – Aspose.Cells Cloud API"
secondtitle: "Belge"
linktitle: "Al"
type: docs
url: /tr/oleobjects/get/
aliases: [  /tr/get-oleobject-from-a-worksheet/ ]
keywords: "aspose, cells, ole nesnesi, excel, çalışma sayfası, ole nesnesi al, rest api"
description: "Aspose.Cells Cloud REST API kullanarak bir çalışma sayfasından bir OLE nesnesini (görüntü, grafik veya gömülü dosya) alın. HTTPS uç noktası, gerekli parametreler, örnek cURL ve birden fazla dilde SDK kodunu içerir."
ArtikelBaşlığı: "Excel Çalışma Sayfasından OLE Nesnesini Alın – Aspose.Cells Cloud API"
weight: 10
---

Bu REST API, bir Excel çalışma sayfasından bir **OLE nesnesi** alır.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### İstek Parametreleri

| Parametre Adı | Tür      | Konum | Açıklama                                                    |
| ------------- | -------- | ----- | ----------------------------------------------------------- |
| name          | string   | path  | Belge adı.                                                  |
| sheetName     | string   | path  | Çalışma sayfası adı.                                        |
| objectNumber  | integer  | path  | Çalışma sayfası içindeki nesne numarası.                   |
| format        | string   | query | Nesnenin istenen dışa aktarma formatı (örn., `png`, `jpeg`).|
| folder        | string   | query | Belgenin bulunduğu klasör.                                  |
| storageName   | string   | query | Kullanılacak depo adı.                                     |

### Depo Seçenekleri

- **folder** – Çalışma kitabının bulunduğu varsayılan depodaki alt klasörü belirtir.
- **storageName** – Çalışma kitabının başka bir yerde depolandığı durumda varsayılan depo adını geçersiz kılar.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject), genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını kullanarak Aspose.Cells web hizmetini çağırabilirsiniz. Aşağıdaki örnek, bir OLE nesnesini PNG görüntüsü olarak istemeyi nasıl yapacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### İkili Görüntü Yanıtı

`format` bir görüntü türüne (`png`, `jpeg` vb.) ayarlandığında, API başlıkla birlikte ikili görüntü verisini döndürür:

```
Content-Type: image/png
```

_(Görüntü dosyası doğrudan istemciye akışlanır.)_

### JSON Meta Veri Yanıtı

`format` atlanırsa veya `json` olarak ayarlanırsa, API OLE nesnesini açıklayan bir JSON yükü döndürür:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Hata Yanıtları

| HTTP Durumu | Hata Kodu    | Açıklama                                      |
| ----------- | ------------ | --------------------------------------------- |
| 400         | BadRequest   | Eksik veya geçersiz parametreler.             |
| 401         | Unauthorized | Geçersiz veya eksik JWT belirteci.            |
| 404         | NotFound     | Çalışma kitabı, çalışma sayfası veya OLE nesnesi bulunamadı. |
| 500         | ServerError  | Beklenmeyen sunucu hatası.                    |

**Örnek 404 Yanıtı**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "Sayfa 'Sheet1' içinde numarası 0 olan istenen OLE nesnesi bulunamadı."
}
```

## Bulut SDK Kullanımı

SDK kullanmak, API’yi entegre etmenin en hızlı yoludur. SDK’lar düşük seviyeli ayrıntıları yöneterek size iş mantığınız üzerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’larla Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}