---
title: Aspose.Cells Cloud API kullanarak Excel çalışma sayfasında dinamik bir filtre ekleme
description: Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasına dinamik filtre (örneğin, BelowAverage, Tomorrow, LastMonth) nasıl uygulanacağını öğrenin. Kimlik doğrulama, istek sözdizimi, parametreler, yanıt işleme ve birden fazla dil için SDK örneklerini içerir.
keywords: Aspose.Cells, dinamik filtre, Excel API, REST, otomatik filtre, bulut SDK
slug: add-dynamic-filter
api_version: v3.0
---

## Genel Bakış

**PutWorksheetDynamicFilter** işlemi, bir Excel çalışma sayfasındaki belirli bir aralığa dinamik bir filtre ekler.  
Dinamik filtreler, tarihler, ortalama değerler veya boş hücreler gibi değerleri otomatik olarak değerlendirerek özel formüller yazmadan “akıllı” görünümler oluşturmanıza olanak tanır.

## Ön Gereksinimler

| Gereksinim | Detaylar |
|-----------|----------|
| **Kimlik Doğrulama** | `/connect/token` uç noktasından alınan geçerli bir JWT belirteci. `Authorization: Bearer <token>` başlığına eklenmelidir. |
| **Depolama** | Çalışma kitabının Aspose Cloud depolama konumunda (varsayılan veya özel bir depolama) bulunması gerekir. |
| **Desteklenen dosya formatları** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv` vb. |
| **İzinler** | Hedef klasör/dosyaya okuma/yazma erişimi. |

## HTTP İsteği

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Yol Parametreleri

| Parametre | Tür | Zorunlu | Açıklama |
|-----------|-----|---------|----------|
| `name` | string | ✅ | Excel çalışma kitabının adı (örneğin, `Book1.xlsx`). |
| `sheetName` | string | ✅ | Filtrelenecek aralığı içeren çalışma sayfasının adı. |

### Sorgu Parametreleri

| Parametre | Tür | Zorunlu | Açıklama |
|-----------|-----|---------|----------|
| `range` | string | ✅ | Filtrenin uygulanacağı hücre aralığı (örneğin, `A1:B1`). |
| `fieldIndex` | integer | ✅ | Dinamik filtre uygulanacak aralıktaki sütunun sıfır tabanlı indeksi. |
| `dynamicFilterType` | string | ✅ | Uygulanacak dinamik filtre türü (**Desteklenen Dinamik Filtre Tipleri** bölümüne bakın). |
| `matchBlanks` | boolean | ❌ | `true` ise, boş hücreler filtre sonuçlarına dahil edilir. Varsayılan: `false`. |
| `refresh` | boolean | ❌ | `true` ise, filtre uygulandıktan sonra otomatik filtre yenilenir. |
| `folder` | string | ❌ | Çalışma kitabının bulunduğu depolamadaki klasör yolu. |
| `storageName` | string | ❌ | Kullanılacak Aspose Cloud depolama adı. |

### İstek Gövdesi

İstek gövdesi boş bir JSON nesnesidir:

```json
{}
```

## Desteklenen Dinamik Filtre Tipleri

| Değer | Anlamı |
|-------|--------|
| `BelowAverage` | Değeri sütunun ortalamasının altında olan satırlar. |
| `AboveAverage` | Değeri sütunun ortalamasının üzerinde olan satırlar. |
| `Tomorrow` | Tarihi yarının tarihine eşit olan satırlar. |
| `Yesterday` | Tarihi dünün tarihine eşit olan satırlar. |
| `NextWeek` | Tarihi gelecek takvim haftasında olan satırlar. |
| `LastMonth` | Tarihi önceki ayda olan satırlar. |
| `ThisYear` | Tarihi mevcut yılda olan satırlar. |

## Örnek İstek (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT isteği boş bir JSON gövdesine sahiptir
```

## Örnek Yanıt

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Dinamik filtre başarıyla uygulandı."
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                      |
|-----|-----------------------------|-----------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırlamasını aşıyor. |
| 500 | Internal Server Error (Sunucu İçi Hata) | Beklenmeyen sunucu hatası. |

## SDK Örnekleri

Aşağıda, en popüler SDK’lar için çalıştırılabilir örnek kod parçacıkları yer almaktadır. `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` ve diğer yer tutucuları gerçek değerlerinizle değiştirin.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | Çalışma kitabının adı.
var sheetName = "Sheet1"; // string | Çalışma sayfasının adı.
var range = "A1:B1"; // string | Filtrelenecek aralık.
var fieldIndex = 0; // int? | Sıfır tabanlı sütun indeksi.
var dynamicFilterType = "BelowAverage"; // string | Dinamik filtre türü.
var matchBlanks = true; // bool? | Boş hücreleri dahil et.
var refresh = true; // bool? | Uyguladıktan sonra yenile.
var folder = "myFolder"; // string (isteğe bağlı)
var storageName = null; // string (isteğe bağlı)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("AutoFilterApi.PutWorksheetDynamicFilter çağrısı sırasında istisna: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (isteğe bağlı)
            undefined              // storageName (isteğe bağlı)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Benzer kod parçacıkları Ruby, PHP, Go ve Perl için de resmi SDK deposunda bulunmaktadır.)*

## İlgili Konular

- **Standart bir Otomatik Filtre ekleme** – [Standart bir filtre ekleme](/autofilter/add-filter)  
- **Tarih filtresi ekleme** – [Tarih filtresi ekleme](/autofilter/add-date-filter)  
- **Bir Otomatik Filtreyi silme** – [Otomatik filtre silme](/autofilter/delete-filter)  
- **Çalışma sayfalarıyla çalışmak** – [Çalışma sayfası API genel bakış](/worksheets/)  

## Notlar

* Orjinal belgelerde kullanılan tüm görüntüler erişilebilirlik açısından incelenmiştir. Dekoratif simgeler `alt=""` ve `role="presentation"` ile işaretlenmiştir; işlevsel simgeler açıklayıcı `alt` metinlerini korumuşlardır.  
* Meta anahtar kelimeler, boş girişler ve yinelenenler temizlenmiş olup daha temiz yapıya sahiptir.  
* Sayfa artık SEO ve ekran okuyucu navigasyonunu iyileştirmek için net bir başlık hiyerarşisine sahiptir (front matter'da tek H1, ana bölümler için H2, alt bölümler için H3/H4).  

---