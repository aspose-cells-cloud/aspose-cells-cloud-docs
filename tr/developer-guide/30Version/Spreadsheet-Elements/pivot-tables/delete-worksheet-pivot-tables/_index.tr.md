---
title: "Bir Excel Çalışma Sayfasındaki Tüm Pivot Tabloları Sil"
description: "Aspose.Cells Cloud REST API kullanarak belirtilen bir çalışma sayfasındaki tüm pivot tabloları siler."
keywords: "Aspose.Cells, Pivot Tablo, Sil, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Bir Excel Çalışma Sayfasındaki Tüm Pivot Tabloları Sil

## Genel Bakış
Bu işlem, bir Excel dosyasındaki belirli bir çalışma sayfasından **tüm** pivot tabloları kaldırır. Bir çalışma sayfasının analizini sıfırlamak veya tek bir çağrıda kullanılmayan pivot tabloları temizlemek gerektiğinde kullanışlıdır.

## Ön Gereksinimler
API'yi çağırmadan önce aşağıdaki adımları tamamladığınızdan emin olun:

1. **Aspose Cloud Hesabı** – Henüz sahip değilseniz bir Aspose Cloud hesabına kaydolun.  
2. **JWT Token’ı** – Kimlik doğrulama için bir JSON Web Token (JWT) oluşturun. Detaylar için [Kimlik Doğrulama Kılavuzu](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bölümüne bakın.  
3. **Depo Kurulumu** – Hedef Excel dosyasını Aspose Cloud deposuna veya bağlı bir harici depoya yükleyin. Dosyanın bulunduğu **klasörü** ve gerekirse **depoların adını** not edin.

## Kimlik Doğrulama
Aspose.Cells Cloud API’leri **JWT token tabanlı kimlik doğrulama** gerektirir. Her isteğin `Authorization` başlığına token’ı ekleyin:

```
Authorization: Bearer <jwt token>
```

## HTTP İsteği

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Yol Parametreleri
| Ad | Tür | Gerekli | Açıklama |
|----|-----|---------|----------|
| `name` | string | Evet | Excel dosyasının adı (örneğin, `Sample.xlsx`). |
| `sheetName` | string | Evet | Tüm pivot tablolarının kaldırılacağı çalışma sayfasının adı (örneğin, `Sheet1`). |

### Sorgu Parametreleri
| Ad | Tür | Gerekli | Açıklama |
|----|-----|---------|----------|
| `folder` | string | Hayır | Dosyayı içeren klasör. |
| `storageName` | string | Hayır | Kullanılacak depo adı (dosya öntanımlı depoda değilse). |

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Başarılı Yanıt
Hizmet, işlemin durumunu gösteren standart `CellsCloudResponse` nesnesini döndürür.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Hata Yönetimi

| HTTP Durum Kodu | Anlamı | Örnek Yük |
|-----------------|--------|-----------|
| **400** | Geçersiz İstek – eksik veya geçersiz parametreler | `{ "Code": 400, "Message": "Eksik zorunlu parametre 'name'." }` |
| **401** | Yetkisiz – geçersiz veya süresi dolmuş JWT | `{ "Code": 401, "Message": "Geçersiz kimlik doğrulama token’ı." }` |
| **404** | Bulunamadı – dosya veya çalışma sayfası mevcut değil | `{ "Code": 404, "Message": "Çalışma sayfası bulunamadı." }` |
| **500** | Sunucu İç Hatası – beklenmeyen hata | `{ "Code": 500, "Message": "Beklenmeyen bir hata oluştu." }` |

## SDK Örnekleri

Aşağıdaki kod parçacıkları, birkaç Aspose.Cells Cloud SDK ile işlemin nasıl çağrılacağını göstermektedir.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API istemcisini başlat
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// İstek parametrelerini yapılandır
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Yanıt kodu: {response.Code}, durum: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("CellsApi.DeleteWorksheetPivotTables çağrısında istisna: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Kod: " + result.getCode() + ", Durum: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# API istemcisini yapılandır
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Kod: {response.code}, Durum: {response.status}')
except ApiException as e:
    print("CellsApi->delete_worksheet_pivot_tables çağrısında istisna: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Kod: ${result.code}, Durum: ${result.status}`);
    })
    .catch(err => {
        console.error('Hata:', err);
    });
```

*Ek SDK’lar (Go, PHP, Ruby, Swift, Perl, Android), [Aspose.Cells Cloud SDK deposunda](https://github.com/aspose-cells-cloud) mevcuttur.*

## Ayrıca Bakınız
- [Belirli Bir Pivot Tabloyu Sil](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Çalışma Sayfasındaki Tüm Pivot Tabloları Al](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Kimlik Doğrulama Genel Bakış](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [DeleteWorksheetPivotTables için OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*Belge son güncelleme tarihi: 2026-07-30. Tüm içerik UTF‑8 kodlamalıdır.*