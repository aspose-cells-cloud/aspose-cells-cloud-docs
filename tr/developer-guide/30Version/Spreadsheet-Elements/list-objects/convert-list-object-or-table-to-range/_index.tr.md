---
title: "Liste Nesnesini Aralığa Dönüştür – Aspose.Cells Cloud API"
ArticleTitle: "Aspose.Cells Cloud API ile Liste Nesnesini Aralığa Dönüştür"
second_title: "Belge"
linktype: "Dönüştürme"
type: docs
url: /tr/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "Aspose Cells API, liste nesnesini aralığa dönüştür, Excel REST API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel ListObject’ini (tabloyu) aralığa nasıl dönüştüreceğinizi öğrenin. İstek sözdizimi, parametreler, örnek cURL, yanıt şeması, kimlik doğrulama ayrıntıları, hata kodları ve SDK örneklerini içerir."
weight: 30
---

Bu REST API, bir Excel çalışma sayfası içindeki bir **ListObject (tablo)** nesnesini bir **Aralık** nesnesine dönüştürür.

**Ön Gereksinimler:**  
Uç noktayı çağırmadan önce, çalışma kitabının Aspose Cloud deponuza yüklenmiş olması, çalışma sayfasının hedef ListObject’i içeriyor olması ve desteklenen dosya formatını kullandığınızdan emin olun (örneğin, .xlsx, .xlsm).

## REST API

**Kimlik Doğrulama**  
Bu işlemi gerçekleştirmek için `Authorization` başlığında geçerli bir JWT jetonu bulundurmanız gerekir. Jetonu, istemci kimliğiniz ve istemci sırrınızla birlikte OAuth 2.0 jeton uç noktasına POST isteği göndererek edinin. Jeton, `Cells.ReadWrite` kapsamını içermeli ve jeton hizmeti tarafından döndürülen süre boyunca geçerlidir.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Ad                  | Tür      | Konum | Gerekli | Varsayılan | Açıklama                                                   |
| ------------------- | -------- | ----- | ------- | ---------- | ----------------------------------------------------------- |
| **name**            | string   | path  | Evet    | –          | Excel dosyasının adı.                                      |
| **sheetName**       | string   | path  | Evet    | –          | ListObject’i içeren çalışma sayfasının adı.               |
| **listObjectIndex** | integer  | path  | Evet    | –          | Dönüştürülecek ListObject’in (tablonun) sıfır tabanlı indeksi. |
| **folder**          | string   | query | Hayır   | –          | Dosyanın bulunduğu klasör yolu.                            |
| **storageName**     | string   | query | Hayır   | –          | Depolama hizmetinin adı.                                  |

> **Not:** Bu işlem yalnızca **.xlsx** ve **.xlsm** gibi modern Excel formatlarıyla çalışır. ListObject korunmamış olmalıdır. ListObject’ler hakkında daha fazla bilgi için [ListObjects genel bakışına](/tr/list-objects/) bakın. Aralıklarla çalışma hakkında detaylı bilgi için [Aralıklar belgelerine](/tr/ranges/) başvurun.

### cURL Örneği (İstek)

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### Yanıt Şeması

API, yeni oluşturulan aralıkla ilgili ayrıntıları içeren **200 OK** yanıtını döndürür.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| Alan            | Tür     | Açıklama                                          |
| --------------- | ------- | ------------------------------------------------- |
| **Code**        | integer | HTTP benzeri durum kodu (200, başarılı olduğunu gösterir). |
| **Status**      | string  | Metinsel durum iletisi.                           |
| **RangeName**   | string  | Oluşturulan aralığa atanan ad.                    |
| **Address**     | string  | Çalışma sayfası adını içeren aralığın tam adresi.  |
| **FirstRow**    | integer | Aralıktaki ilk satırın sıfır tabanlı indeksi.     |
| **FirstColumn** | integer | Aralıktaki ilk sütunun sıfır tabanlı indeksi.     |
| **RowCount**    | integer | Aralıktaki satır sayısı.                          |
| **ColumnCount** | integer | Aralıktaki sütun sayısı.                          |

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT jetonu.                   |
| 413 | Payload Too Large           | Yüklenen dosya boyut limitini aşıyor.             |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                        |

**Hata Yanıt Şeması (örnek):**

```json
{
  "Code": 400,
  "Message": "Geçersiz listObjectIndex. İndeks 0 ile 5 arasında olmalıdır."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Paketi

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl istek atılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}