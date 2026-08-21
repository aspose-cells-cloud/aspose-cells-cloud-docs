---
title: "Bir ListObject'ten Yineleyen Satırları Kaldır – Aspose.Cells Cloud API Dokümantasyonu"
second_title: "Belge"
linktitle: "Yineleyenleri kaldır"
type: docs
keywords: "yineleyenleri kaldır, listobject, Aspose.Cells Cloud API, Excel, REST"
url: /list-objects/remove-duplicates/
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki bir ListObject'ten yineleyen satırları nasıl sileceğinizi öğrenin. Endpoint, parametreler, kimlik doğrulama ve örnek istekler ile yanıtları içerir."
weight: 20
---

Bu REST API, bir Excel çalışma sayfasındaki bir **ListObject**'ten yineleyen satırları kaldırır.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **İstek parametreleri**

| Parametre Adı       | Tür     | Konum  | Açıklama                                               |
| ------------------- | ------- | ------ | ------------------------------------------------------ |
| **name**            | String  | Yol    | Excel dosyasının adı.                                  |
| **sheetName**       | String  | Yol    | Liste nesnesini içeren çalışma sayfasının adı.         |
| **listObjectIndex** | Integer | Yol    | İşlenecek liste nesnesinin sıfır tabanlı indeksi.      |
| **folder**          | String  | Sorgu  | (İsteğe bağlı) Dosyanın bulunduğu klasör yolu.         |
| **storageName**     | String  | Sorgu  | (İsteğe bağlı) Depolama hizmetinin adı.                |

### Örnek İstek (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
  -X POST \
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
  "DuplicateRowsRemoved": 12,
  "Message": "Yineleyen satırlar başarıyla kaldırıldı."
}
```

{{< /tab >}}
{{< /tabs >}}

### Yanıt

Başarılı durumda hizma, yukarıdaki örneğe benzer bir JSON nesnesi döndürür. Alanlar:

- **Code** – HTTP durum kodu (başarı durumunda `200`).
- **Status** – Durumun metinsel açıklaması.
- **DuplicateRowsRemoved** – Kaldırılan satır sayısı.
- **Message** – İşlemle ilgili ek bilgiler.

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

## Bulut SDK Geliştirme Kiti

Bir SDK kullanmak, geliştirme hızını en hızlı şekilde artıran en iyi yoldur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen GitHub deposunu kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}