---
title: "Klasör Sil – Aspose.Cells Cloud API | REST ile Klasörleri Kaldır"
description: "Aspose.Cells Cloud deposundan bir klasörü (isteğe bağlı olarak içindekileri de) silme yöntemini öğrenin. DELETE /v4.0/cells/storage/folder/{path} uç noktasını kullanın. İstek sözdizimi, parametreler, kimlik doğrulama, örnek kod ve hata yönetimi içerir."
keywords: "Aspose.Cells, klasör sil, bulut deposu, API, REST, Excel, dosya yönetimi"
slug: klasor-sil
date: 2026-07-30
---

# Klasör Sil – Aspose.Cells Cloud API

Aspose.Cells Cloud deposundan bir klasörü (ve isteğe bağlı olarak içindeki tüm içerikleri) kaldırın.

---

## Genel Bakış

**Klasör Sil** işlemi, Aspose.Cells Cloud tarafından kullanılan bir depo hesabından bir klasörü kalıcı olarak kaldırır.  
Boş bir klasörü veya `recursive` bayrağını `true` olarak ayarlayarak klasörün içerdiği tüm dosya ve alt klasörlerle birlikte silebilirsiniz. Bu uç nokta genellikle temizlik betiklerinde, otomatik iş akışlarında veya geçici dizinlere artık ihtiyaç duyulmadığında kullanılır.

---

## HTTP İsteği

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – Silinecek klasörün tam yolu (URL‑kodlu).

### Gerekli HTTP Başlıkları

| Başlık            | Değer                              | Açıklama                              |
|-------------------|------------------------------------|------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | Kimlik doğrulama hizmetinden alınan JWT belirteci. |
| `Accept`          | `application/json`                | Beklenen yanıt biçimi.                |
| `Content-Type`    | `application/json` *(isteğe bağlı)* | DELETE için gerekli değildir, ancak gönderilebilir. |

---

## Kimlik Doğrulama

Aspose.Cells Cloud, **JWT belirteci tabanlı kimlik doğrulama** kullanır.  
Bir erişim belirteci, [kimlik doğrulama uç noktasından](/authentication/) alın ve yukarıda gösterildiği gibi `Authorization` başlığına ekleyin.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Parametreler

| Ad            | Tür     | Konum   | Gerekli | Açıklama                                                               |
|---------------|---------|---------|---------|---------------------------------------------------------------------------|
| `path`        | string  | Yol     | Evet    | Silinecek klasörün yolu (URL‑kodlu).                               |
| `storageName` | string  | Sorgu   | Hayır   | Klasörü içeren deponun adı. Atlanırsa varsayılan depo kullanılır. |
| `recursive`   | boolean | Sorgu   | Hayır   | `true` → klasörü **ve tüm içeriğini** siler. Varsayılan değer `false`'tur. |

**Örnek sorgu dizisi**

```
?storageName=MyStorage&recursive=true
```

---

## İstek Örneği (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Yanıt

Başarılı bir istek, boş bir JSON nesnesiyle birlikte **HTTP 200 OK** döndürür:

```json
{}
```

İşlem sonucu ikili olduğu için (klasör silinir veya bir hata döndürülür) ek bir yük sağlanmaz.

---

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Süzgeç başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

Bir hata oluştuğunda, gövde `code` ve `message` alanlarını içeren bir JSON nesnesiyle birlikte hatayı açıklayacaktır.

---

## SDK Örnek Kodları

Aşağıdaki örnekler, resmi olarak desteklenen SDK’larla **Klasör Sil** işlemini nasıl çağıracağınızı göstermektedir. `{access_token}` ve parametre değerlerini kendi değerlerinizle değiştirin.

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API istemcisini yapılandır
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Klasörü sil (özyinelemeli)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// API istemcisini başlat
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// Yapılandır
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Klasörü özyinelemeli olarak sil
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Folder deleted.";
} catch (Exception $e) {
    echo 'Exception when calling FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Folder deleted.'
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Folder deleted'))
    .catch(err => console.error('Error:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Folder deleted")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Folder deleted.\n";
};
if ($@) {
    warn "Error deleting folder: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println("Folder deleted")
}
```
</details>

---

## Ayrıca Bakınız

- **[Klasör Oluştur](/create-folder/)** – Bulut deposunda yeni bir klasör oluşturun.  
- **[Klasör Kopyala](/copy-folder/)** – Bir klasörü ve içeriğini kopyalayın.  
- **[Klasör Taşı](/move-folder/)** – Bir klasörü farklı bir yola taşıyın.  
- **[OpenAPI Specification (OpenAPI Özellikleri)](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder)** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder işlemi</a> (etkileşimli API tarayıcısı).

---

## SEO & Erişilebilirlik Kontrol Listesi (iç)

- **Başlık ve H1**, doğru kısa çizgiyi (`–`) kullanır ve birincil anahtar kelime *Klasör Sil* içerir.  
- Tüm başlıklar mantıklı hiyerarşiyi takip eder (`H1 → H2 → H3`).  
- UTF‑8 kodlama hataları kalmamıştır.  
- Meta anahtar kelimeler tek bir temiz liste halinde birleştirilmiştir (tercihe bağlı olarak atlanabilir).  
- Harici bağlantılar güvenlik için `rel="noopener noreferrer"` içerir.  
- Arayüz simgeleri ve dil bayrakları (sayfada render ediliyorsa) `aria-label`/`alt` özniteliklerine sahip olmalıdır (örneğin, `aria-label="English (US)"`).  
- Sayfa `<head>` kısmında her dil sürümü için `<link rel="alternate" hreflang="xx" href="…">` etiketleri önerilir.

---