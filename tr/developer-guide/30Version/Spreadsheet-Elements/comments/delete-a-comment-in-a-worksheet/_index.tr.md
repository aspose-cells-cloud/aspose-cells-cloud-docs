---
---
title: "Çalışma Sayfası Yorumunu Silme API’si – Aspose.Cells Cloud"
description: "Aspose.Cells Cloud REST API’sini (v3.0) kullanarak bir Excel çalışma sayfasındaki belirli bir hücre yorumunu silin. Uç nokta, parametreler, istek/yanıt örnekleri, SDK kod parçacıkları ve hata işleme içerir."
keywords: "Aspose.Cells, yorum sil, Excel API, REST, çalışma sayfası yorumu"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# Çalışma Sayfası Yorumunu Silme API’si – Aspose.Cells Cloud

> **Son güncelleme tarihi:** 30 Temmuz 2026  

## Genel Bakış
**Yorum**, bir Excel çalışma sayfasındaki belirli bir hücreye eklenen bir metin notudur.  
**Çalışma Sayfası Yorumunu Sil** işlemi, belirtilen hücreden yorumu kaldırır.

![Aspose.Cells Cloud – Çalışma Sayfası Yorumunu Silme illustration](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – Çalışma Sayfası Yorumunu Silme API’si")

## Kimlik Doğrulama
Tüm Aspose.Cells Cloud uç noktaları **JWT belirteci tabanlı kimlik doğrulama** gerektirir.  
Belirteci `Authorization` başlığına ekleyin:

```
Authorization: Bearer <jwt token>
```

JWT belirteci alma hakkında daha fazla bilgi için [Kimlik Doğrulama Kılavuzu’na](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakın.

## Ön Gereksinimler
- Geçerli bir JWT erişim belirteci.  
- Hedef çalışma kitabının (`{name}`) belirtilen depolama konumunda bulunması gerekir.  
- Opsiyonel: Tercih ettiğiniz dil için Aspose.Cells Cloud SDK’larından biri yüklü olmalı.

## HTTP İsteği

### Uç Nokta
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Yol Parametreleri
| Parametre | Tür   | Gerekli | Açıklama |
|-----------|--------|----------|-------------|
| `name`      | string | ✅ | Excel çalışma kitabının adı (örneğin, `test.xlsx`). |
| `sheetName` | string | ✅ | Yorumun bulunduğu çalışma sayfasının adı. |
| `cellName`  | string | ✅ | Yorumu silinecek hücrenin adresi (örneğin, `A1`). |

### Sorgu Parametreleri
| Parametre   | Tür   | Gerekli | Açıklama |
|-------------|--------|----------|-------------|
| `folder`      | string | ❌ | Çalışma kitabının bulunduğu klasör yolu. Atlanırsa kök klasör kullanılır. |
| `storageName` | string | ❌ | Depolama hizmetinin adı (örneğin, `MyCloud`). Atlanırsa varsayılan depolama kullanılır. |

## İstek Örneği

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Yanıt

### Başarılı (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                     | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (Tamam)                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)                | Geçersiz veya eksik JWT belirteci. |
| 413  | Payload Too Large (İçerik Çok Büyük)           | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | Internal Server Error (İç Sunucu Hatası)       | Beklenmeyen sunucu hatası. |
### Hata Yanıtları

| HTTP Kodu | Açıklama | Örnek |
|-----------|-------------|---------|
| 400 | Bad Request (Hatalı İstek) – Eksik veya hatalı parametreler. | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | Unauthorized (Yetkisiz) – Geçersiz veya eksik belirteç. | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | Not Found (Bulunamadı) – Dosya, çalışma sayfası veya yorum mevcut değil. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | Internal Server Error (İç Sunucu Hatası) – Sunucuda beklenmeyen bir durum oluştu. | `{ "Code": 500, "Message": "Server error." }` |

## SDK Örnekleri
Aşağıda, en yaygın diller için çalıştırılabilir kod parçacıkları verilmiştir. `<jwt token>`, `test.xlsx`, `Sheet1` ve `A1` değerlerini kendi değerlerinizle değiştirin.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// API istemcisini yapılandırın
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Comment deleted. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Deleted comment, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Exception when calling WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Comment deleted. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Comment deleted – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Comment deleted. Status:", response.status);
    })
    .catch((error) => {
        console.error("Error deleting comment:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comment deleted. Status:", response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comment deleted. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (optional)
        "MyStorage",   // storageName (optional)
    )
    if err != nil {
        fmt.Printf("Error when calling DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Comment deleted. Status: %s\n", result.Status)
}
```

## İlgili İşlemler
- [Çalışma Sayfası Yorumu Ekle](/comments/add/)  
- [Çalışma Sayfası Yorumunu Güncelle](/comments/update/)  

## Oran Sınırlaması
Aspose.Cells Cloud, varsayılan olarak **hesap başına dakikada 100 istek** sınırlaması uygular. Bu sınıra ulaşılırsa HTTP 429 Too Many Requests (Çok Fazla İstek) hatası döndürülür. Kısıtlamayı önlemek için üstel geri dönme uygulayın veya `Retry-After` başlığını dikkate alın.

## Ayrıca Bakınız
- **OpenAPI Spesifikasyonu:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Kimlik Doğrulama Kılavuzu:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **SDK Deposu:** <https://github.com/aspose-cells-cloud>  

---