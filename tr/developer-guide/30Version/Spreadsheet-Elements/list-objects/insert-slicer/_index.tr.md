---
title: "Bir Excel ListObject'a Süzgeç Ekleyin – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Süzgeç ekle"
type: docs
keywords: "Aspose.Cells, Excel süzgeci, ListObject, REST API, bulut SDK"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel ListObject'a süzgeç nasıl ekleyeceğinizi öğrenin.uç nokta, parametreler, kimlik doğrulama, örnek cURL isteği ve yanıt JSON'u içerir."
weight: 20
ArticleTitle: "Bir Excel ListObject'a Süzgeç Ekleyin – Aspose.Cells Cloud API"
---

Bu REST API, bir Excel çalışma sayfasındaki bir liste nesnesi için bir süzgeç ekler.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### İstek Parametreleri

| Parametre Adı     | Tür      | Konum  | Açıklama                                                                     |
| ----------------- | -------- | ------ | ---------------------------------------------------------------------------- |
| name              | String   | Yol    | Excel dosyasının adı.                                                        |
| sheetName         | String   | Yol    | Liste nesnesini içeren çalışma sayfasının adı.                               |
| listObjectIndex   | Integer  | Yol    | Süzgecin ekleneceği liste nesnesinin sıfır tabanlı dizini.                   |
| columnIndex       | Integer  | Sorgu  | Süzgecin temellendiği sütunun sıfır tabanlı dizini.                         |
| destCellName      | String   | Sorgu  | Süzgecin yerleştirileceği hücre başvurusu (örneğin, **A1**).                 |
| folder            | String   | Sorgu  | Excel dosyasını içeren depolama klasörü.                                     |
| storageName       | String   | Sorgu  | Aspose Cloud depolama hizmetinin adı.                                        |

API'yi çağırmak için cURL komut satırı aracını kullanabilirsiniz:

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Not:** İstek, Aspose Cloud kimlik doğrulama hizmetinden alınan geçerli bir JWT bearer token gerektirir. Bu uç nokta, bir istek gövdesi gerektirmez; istemci kitapluğunuz bir yük (payload) zorunlu kılıyorsa boş bir JSON nesnesi `{}` gönderin.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **Yanıt Başlığı:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK (Tamam)                  | Süzgeç başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT token.                          |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırını aşıyor.                |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                              |

### Hata İşleme

Bir hata oluştuğunda API, sorunu açıklayan bir `ErrorMessage` alanı içeren bir JSON nesnesi döndürür. Doğru eylemi belirlemek için HTTP durum kodunu ve `ErrorMessage` alanını inceleyin.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye ayrıntıları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen GitHub depomuzu inceleyin.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine istek nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}