---
title: "Tüm Çalışma Sayfası Yorumlarını Sil"
description: "Aspose.Cells Cloud API kullanarak bir Excel dosyasındaki bir çalışma sayfasından tüm yorumları silin. DELETE uç noktasını, gerekli parametreleri, kimlik doğrulamayı, örnek cURL isteğini, yanıt formatını, hata kodlarını ve SDK örneklerini öğrenin."
keywords: "Aspose, Cells, yorumları sil, çalışma sayfası, API, REST, Excel, bulut"
url: /tr/comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Tüm Çalışma Sayfası Yorumlarını Sil

**API sürümü:** `v3.0`  
**Kaynak:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud, belirtilen bir çalışma sayfasından **tüm** yorumları kaldıran güçlü bir REST uç noktası sağlar. Bu işlem geri alınamaz; bir kez çalıştırıldığında yorumlar geri getirilemez.

---

## Ön Koşullar

| Gereksinim | Detaylar |
|-----------|----------|
| **Kimlik Doğrulama** | `Authorization` başlığında geçerli bir JWT erişim belirteci gerekir (`Bearer <jwt token>`). Belirteci [OAuth2 kimlik doğrulama akışı](https://docs.aspose.cloud/cells/authentication/) ile edinin. |
| **Depolama** | Dosyanın Aspose.Cells Cloud’un erişebildiği bir depolama alanındayol olması gerekir (`storageName` atlanırsa varsayılan depolama kullanılır). |
| **İzinler** | Belirtecin hedef dosyayı okuma ve yazma iznine sahip olması gerekir. |
| **SDK’lar (isteğe bağlı)** | .NET, Java, PHP, Ruby, Node.js, Python, Perl ve Go için SDK’lar mevcuttur (**SDK Örnekleri** bölümüne bakın). |

---

## HTTP İsteği

### Uç Nokta

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Yol Parametreleri

| Ad         | Tür    | Açıklama |
|------------|--------|----------|
| `name`     | string | Excel dosyasının adı (örneğin, `test.xlsx`). |
| `sheetName` | string | Çalışma sayfasının adı (örneğin, `Sheet1`). |

### Sorgu Parametreleri

| Ad            | Tür    | Gerekli | Açıklama |
|---------------|--------|---------|----------|
| `folder`      | string | isteğe bağlı | Dosyayı içeren klasörün yoludur. |
| `storageName` | string | isteğe bağlı | Dosyanın bulunduğu depolamanın adıdır. |

### İstek Başlıkları

| Başlık                | Değer                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer <jwt token>`               |
| `Accept`              | `application/json`                |
| `Content-Type`        | `application/json`                |

---

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*`test.xlsx`, `Sheet1`, `Documents`, `MyStorage` ve `<jwt token>` değerlerini kendi gerçek değerlerinizle değiştirin.*

---

## Yanıt

### Başarılı (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Yanıt gövdesi `CellsCloudResponse` modeline uygundur.

### Hata Yanıtları

| HTTP Kodu | Anlamı                          | Örnek Gövde |
|-----------|----------------------------------|-------------|
| **400**   | Geçersiz istek – geçersiz parametreler. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**   | Yetkisiz erişim – eksik/geçersiz JWT belirteci. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Bulunamadı – dosya veya çalışma sayfası mevcut değil. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**   | Sunucu iç hatası. | `{ "Code": 500, "Message": "Server error." }` |

---

## SDK Örnekleri

Aşağıdaki kod parçacıkları, resmi Aspose.Cells Cloud SDK’ları (sürüm 3.13.0) ile uç noktayı çağırma yöntemlerini göstermektedir. Yer tutucu değerleri (`<fileName>`, `<sheet>`, `<jwt token>` vb.) kendi verilerinizle değiştirin.

### C#

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | Dosya adı.
var sheetName = "Sheet1"; // string | Çalışma sayfası adı.
var folder = "Documents"; // string | Klasör yolu (isteğe bağlı)
var storageName = "MyStorage"; // string | Depolama adı (isteğe bağlı)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("WorksheetsApi.DeleteWorksheetComments çağrısında istisna: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'WorksheetsApi->deleteWorksheetComments çağrısında istisna: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # isteğe bağlı
storage_name = 'MyStorage'    # isteğe bağlı

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "WorksheetsApi->delete_worksheet_comments çağrısında istisna: #{e}"
end
```

### Node.js (TypeScript)

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Hata:", error));
```

### Python

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # isteğe bağlı
storage_name = "MyStorage"    # isteğe bağlı

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("WorksheetsApi->delete_worksheet_comments çağrısında istisna:", e)
```

### Perl

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "WorksheetsApi->delete_worksheet_comments çağrısında istisna: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Hata: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Notlar ve Sınırlamalar

* Bu işlem, belirtilen çalışma sayfasındaki **tüm yorumları siler**. Geri alınamayacağından dikkatli kullanın.
* İstek gövdesi **almaz**; tüm gerekli bilgiler URL ve başlıklar aracılığıyla iletilir.
* Hedef dosya **korunmuşsa** veya çalışma sayfası **salt okunur** durumdaysa, API altta yatan nedenlere bağlı olarak `400` veya `401` hatası döndürür.
* Uç nokta, **Aspose Cloud Depolama**’da bulunan dosyalarla ve doğru şekilde `storageName` ile başvurulan **Amazon S3**, **Azure Blob** veya **Google Cloud Storage** depolarıyla çalışır.

---

## İlgili Kaynaklar

* **OpenAPI Spesifikasyonu** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **Kimlik Doğrulama Rehberi** – [Aspose.Cells Cloud için OAuth2](https://docs.aspose.cloud/cells/authentication/)
* **SDK Deposu** – <https://github.com/aspose-cells-cloud>
* **Genel Çalışma Sayfası API’si** – <https://docs.aspose.cloud/cells/worksheets/>

---

*Son güncelleme: 2026‑07‑30*