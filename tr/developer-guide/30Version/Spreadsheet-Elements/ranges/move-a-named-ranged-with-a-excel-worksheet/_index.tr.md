---
title: "Excel çalışma sayfası ile adlandırılmış bir aralığı taşıma"
second_title: "Belge"
linktitle: "Taşı"
type: docs
url: /ranges/move/
aliases: [/move-a-named-range-with-an-excel-worksheet/]
keywords: "Aspose.Cells Cloud, adlandırılmış aralığı taşı, Excel çalışma sayfası, REST API, aralık taşıma, SDK örnekleri"
description: "Aspose.Cells Cloud REST API v3.0 kullanarak bir Excel çalışma sayfasında adlandırılmış bir aralığı nasıl taşıyacağınızı öğrenin. Uç nokta ayrıntıları, kimlik doğrulama, örnekler ve SDK kod örnekleri içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API kullanarak Excel çalışma sayfası ile adlandırılmış bir aralığı taşıma"
---

Adlandırılmış bir aralığı taşımak, verileri programlı olarak yeniden düzenlemeniz gerektiğinde yaygın olarak karşılaşılan bir görevdir. Bu bölüm, bir tanımlanmış aralığı aynı çalışma sayfası üzerinde yeni bir konuma taşımayı Aspose.Cells Cloud REST API ile nasıl yapacağınızı açıklar.

Bu REST API, belirli bir aralığı bir Excel çalışma sayfasındaki hedef aralığa taşır.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Kimlik Doğrulama
API, Aspose Cloud OAuth akışı aracılığıyla elde edilen bir **Bearer JWT belirteci** gerektirir. Belirteci `Authorization` başlığına ekleyin:

```
Authorization: Bearer <jwt token>
```

Belirtecin **Cells** kapsamına sahip olması gerekir.

### Ön Gereksinimler
- Çalışma kitabının Aspose Cloud deposunda depolanmış olması gerekir.  
- Dosya kök dizinde değilse depo adını (`storageName`) ve klasör yolunu (`folder`) sağlayın.  
- API sürümünü **v3.0** destekleyen en son Aspose.Cells Cloud SDK sürümünü kullanın.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Ad             | Tür    | Konum  | Açıklama |
|----------------|--------|--------|----------|
| **name**       | string | path   | Çalışma kitabının dosya adı |
| **sheetName**  | string | path   | Çalışma sayfasının adı |
| **destRow**    | integer| query  | Hedef aralığın başlangıç satır indeksi (0‑tabanlı) |
| **destColumn**| integer| query  | Hedef aralığın başlangıç sütun indeksi (0‑tabanlı) |
| **range**      | object | body   | Taşınacak kaynak aralığın tanımı |
| **folder**     | string | query  | Çalışma kitabının depolandığı klasör yolu |
| **storageName**| string | query  | Aspose Cloud deposunun adı |

### İstek Gövdesi

| Alan           | Tür    | Gerekli | Açıklama |
|----------------|--------|---------|----------|
| **ColumnCount**| integer| Hayır | Kaynak aralıktaki sütun sayısı |
| **ColumnWidth**| integer| Hayır | Her sütunun genişliği (nokta cinsinden) |
| **FirstColumn**| integer| Hayır | Kaynak aralığın ilk sütununun sıfır tabanlı indeksi |
| **FirstRow**   | integer| Hayır | Kaynak aralığın ilk satırının sıfır tabanlı indeksi |
| **Name**       | string | Hayır | Aralığın adı (adlandırılmış aralık ise) |
| **RefersTo**   | string | Hayır | Aralığı tanımlayan A‑1 stili başvuru |
| **RowCount**   | integer| Hayır | Kaynak aralıktaki satır sayısı |
| **RowHeight**  | integer| Hayır | Her satırın yüksekliği (nokta cinsinden) |
| **Worksheet**  | string | Hayır | Kaynak aralığı içeren çalışma sayfası |

### İş Akışı

1. Çalışma kitabını Aspose Cloud deposuna **yükleme** (zaten mevcut değilse).  
2. OAuth uç noktası kullanarak bir JWT belirteci **oluşturma**.  
3. Kaynak aralığı tanımlayan JSON yükünü **oluşturma**.  
4. Gerekli yol, sorgu parametreleri ve JSON gövdesi ile `moveto` uç noktasını **çağırma**.  
5. Yanıtı **doğrulama**; başarılı çağrı `200 OK` durum kodunu döndürür.

### Örnek İstek / Yanıt

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Hata oluşursa, yanıt başarısızlıkla ilgili ek ayrıntılar sağlayan isteğe bağlı bir `ErrorMessage` alanı içerir.

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                        |
|-----|-----------------------------|-------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

**Yanıt Şeması**

| Alan | Tür    | Açıklama |
|------|--------|----------|
| **Code** | integer | API tarafından döndürülen HTTP benzeri durum kodu (örn., 200) |
| **Status** | string | Sonucun metinsel açıklaması (örn., "OK") |
| **ErrorMessage** | string (isteğe bağlı) | Çağrı başarısız olduğunda insan okuyabilir hata ayrıntıları |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en hızlı şekilde artırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yöneterek proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub Deposu</a>'na bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}