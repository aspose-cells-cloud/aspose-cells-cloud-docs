---
title: "Şablon Dosyası ile Bir Excel Çalışma Kitabı Nasıl Oluşturulur"
second_title: "Belge"
linktitle: "Şablon Dosyası"
type: docs
url: /tr/create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, şablon, API, Aspose.Cells, çalışma kitab, REST, Bulut"
description: "Aspose.Cells Cloud REST API kullanarak şablon dosyalarından Excel çalışma kitapları nasıl oluşturulacağını öğrenin. Önkoşullar, kimlik doğrulama adımları, cURL örnekleri, hata işleme ayrıntıları ve SDK kod snippet’leri içerir."
weight: 30
---

# Şablon Dosyası ile Bir Excel Çalışma Kitabı Nasıl Oluşturulur

Mevcut bir şablon dosyası ve isteğe bağlı olarak Smart‑Marker değerlerini sağlayan bir veri dosyası kullanarak yeni bir Excel çalışma kitabı oluşturun. İşlem, Aspose.Cells Cloud’un **PUT** `/cells/{name}` uç noktası aracılığıyla gerçekleştirilir.

---

## Önkoşullar

| Gereksinim | Açıklama |
|------------|----------|
| **Aspose.Cells Cloud hesabı** | https://dashboard.aspose.cloud/ adresinden kaydolun ve bir **Client Id** / **Client Secret** edinin. |
| **JWT erişim belirteci** | [Kimlik doğrulama kılavuzunda](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) açıklanan şekilde bir JWT belirteci oluşturun. |
| **Şablon dosyası** | Şablon Excel dosyasını (örn. `Calendar.xlsx`) seçtiğiniz depoya **Upload File** API’si veya kullanıcı arayüzü aracılığıyla yükleyin. |
| **Veri dosyası (isteğe bağlı)** | Smart‑Marker değerlerini içeren JSON veya XML dosyası (örn. `Sample_Data.xml`). |
| **Desteklenen depo** | Varsayılan depo (`Default`) veya Aspose hesabınızda yapılandırılmış özel depo. |

---

## Kimlik Doğrulama

Tüm Aspose.Cells Cloud istekleri, `Authorization` başlığında geçirilen bir **Bearer JWT belirteci** gerektirir:

```http
Authorization: Bearer {access_token}
```

Belirteç önceden alınmalı ve varsayılan olarak 1 saat geçerlidir.

---

## İstek

### HTTP İsteği

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Bileşen | Değer |
|---------|-------|
| **Yöntem** | `PUT` |
| **Yol** | `/cells/{name}` – `name`, yeni oluşturulacak çalışma kitabının istenen adıdır (uzantı dahil, örn. `newworkbook.xlsx`). |
| **İçerik Türü** | `multipart/form-data` (gövdede veri dosyası gönderildiğinde). |
| **Kabul** | `application/json` |

### Yol Parametresi

| Ad | Tür | Gerekli | Açıklama |
|----|----|---------|----------|
| `name` | string | **Evet** | Oluşturulacak çalışma kitabının adı (örn. `newworkbook.xlsx`). |

### Sorgu Parametreleri

| Parametre | Tür | Gerekli | Varsayılan | Açıklama |
|-----------|----|---------|-----------|----------|
| `templateFile` | string | Hayır | — | Bulutta saklanan şablon dosyasının adı. |
| `dataFile` | string | Hayır | — | Bulutta saklanan veri dosyasının (XML veya JSON) adı. |
| `isWriteOver` | boolean | Hayır | `false` | Hedef dosya zaten varsa üzerine yaz. `true` veya `false` değerini **tırnak işareti olmadan** geçirin. |
| `folder` | string | Hayır | — | Şablonun (ve isteğe bağlı olarak veri dosyasının) bulunduğu klasör yolu. |
| `storageName` | string | Hayır | — | Dosyaları içeren depo hizmetinin adı. |
| `checkExcelRestriction` | boolean | Hayır | `true` | Oluşturma öncesi çalışma kitabını Excel kısıtlamalarına göre doğrulayın. |

### İstek Gövdesi (isteğe bağlı)

Smart‑Marker yer tutucuları için veri doğrudan isteğe gönderilirse, bu veriyi **`data`** adlı multipart dosya parçası olarak ekleyin.

| Parça Adı | Tür | Açıklama |
|-----------|-----|----------|
| `data` | file | Smart‑Marker değerlerini içeren XML veya JSON dosyası. |

#### İstek gövdesi ile örnek cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*Eğer `dataFile` sorgu parametresi multipart gövdesi yerine kullanılıyorsa `-F` bayrağını atlayın.*

---

## Yanıt

Başarılı bir çağrı, oluşturulan çalışma kitabını açıklayan bir JSON yükü içeren **`200 OK`** (veya yeni bir dosya oluşturulduğunda **`201 Created`**) döndürür.

```json
{
    "Code": 200,
    "Status": "OK",
    "File": {
        "Name": "newworkbook.xlsx",
        "Size": 18234,
        "Path": "output/newworkbook.xlsx",
        "Url": "https://api.aspose.cloud/v3.0/storage/file/output/newworkbook.xlsx"
    }
}
```

### Yanıt Veri Türleri

| Özellik | Tür | Açıklama |
|---------|-----|----------|
| `Code` | integer | API tarafından döndürülen HTTP benzeri durum kodu. |
| `Status` | string | Durumun metinsel açıklaması. |
| `File` | object | Oluşturulan çalışma kitabının ayrıntıları. |
| `File.Name` | string | Oluşturulan çalışma kitabının dosya adı. |
| `File.Size` | integer | Bayt cinsinden boyut. |
| `File.Path` | string | Depoda göreli yol. |
| `File.Url` | string | Doğrudan indirme URL’si (aynı JWT belirtecini gerektirir). |

---

**HTTP Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | OK | Süzgeç başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error | Beklenmeyen sunucu hatası. |
---

## SDK Örnekleri

Aşağıdaki kod snippet’leri, resmi Aspose.Cells Cloud SDK’larıyla **PutWorkbookCreate**’ı nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | Yeni belge adı.
var templateFile = "Calendar.xlsx"; // string | Şablon dosyası adı.
var dataFile = "Sample_Data.xml"; // string | Veri dosyası adı (isteğe bağlı).
var isWriteOver = true; // bool? | Varsa üzerine yaz.
var folder = "templates"; // string | Dosyaların bulunduğu klasör.
var storageName = "MyStorage"; // string | Depo adı.

using (var dataStream = File.OpenRead("Sample_Data.xml"))
{
    var response = apiInstance.PutWorkbookCreate(
        name,
        templateFile: templateFile,
        dataFile: dataFile,
        isWriteOver: isWriteOver,
        folder: folder,
        storageName: storageName,
        data: dataStream);
    Console.WriteLine(response);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cloud.cells.api.WorkbookApi;
import com.aspose.cloud.cells.model.*;

import java.io.File;
import java.io.FileInputStream;

WorkbookApi api = new WorkbookApi();
String name = "newworkbook.xlsx";
String templateFile = "Calendar.xlsx";
String dataFile = "Sample_Data.xml";
Boolean isWriteOver = true;
String folder = "templates";
String storageName = "MyStorage";

FileInputStream dataStream = new FileInputStream(new File("Sample_Data.xml"));
CellsCloudResponse response = api.putWorkbookCreate(
        name,
        templateFile,
        dataFile,
        isWriteOver,
        folder,
        storageName,
        dataStream);
System.out.println(response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorkbookApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new WorkbookApi(null, $config);
$name = "newworkbook.xlsx";
$templateFile = "Calendar.xlsx";
$dataFile = "Sample_Data.xml";
$isWriteOver = true;
$folder = "templates";
$storageName = "MyStorage";

$data = fopen("Sample_Data.xml", "r");
$result = $apiInstance->putWorkbookCreate($name, $templateFile, $dataFile, $isWriteOver, $folder, $storageName, $data);
print_r($result);
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::WorkbookApi.new
api.config.access_token = '{access_token}'

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = true
folder = 'templates'
storage_name = 'MyStorage'

File.open('Sample_Data.xml', 'rb') do |data|
  response = api.put_workbook_create(name,
                                     template_file: template_file,
                                     data_file: data_file,
                                     is_write_over: is_write_over,
                                     folder: folder,
                                     storage_name: storage_name,
                                     data: data)
  puts response
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorkbookApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

let config = new Configuration();
config.accessToken = '{access_token}';
config.basePath = 'https://api.aspose.cloud';

let apiInstance = new WorkbookApi(config);

let name = 'newworkbook.xlsx';
let templateFile = 'Calendar.xlsx';
let dataFile = 'Sample_Data.xml';
let isWriteOver = true;
let folder = 'templates';
let storageName = 'MyStorage';

let data = fs.createReadStream('Sample_Data.xml');

apiInstance.putWorkbookCreate(name, templateFile, dataFile, isWriteOver, folder, storageName, data)
    .then(response => console.log(response))
    .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.apis import WorkbookApi
from asposecellscloud.models import CellsCloudResponse

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api_instance = WorkbookApi(asposecellscloud.ApiClient(config))

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = True
folder = 'templates'
storage_name = 'MyStorage'

with open('Sample_Data.xml', 'rb') as data:
    response = api_instance.put_workbook_create(
        name,
        template_file=template_file,
        data_file=data_file,
        is_write_over=is_write_over,
        folder=folder,
        storage_name=storage_name,
        data=data)
    print(response)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorkbookApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::Api::WorkbookApi->new($config);

my $name = 'newworkbook.xlsx';
my $template_file = 'Calendar.xlsx';
my $data_file = 'Sample_Data.xml';
my $is_write_over = 1;
my $folder = 'templates';
my $storage_name = 'MyStorage';

open my $fh, '<:raw', 'Sample_Data.xml' or die $!;
my $response = $api_instance->put_workbook_create(
    name => $name,
    template_file => $template_file,
    data_file => $data_file,
    is_write_over => $is_write_over,
    folder => $folder,
    storage_name => $storage_name,
    data => $fh);
print $response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "os"

    asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorkbookApi(cfg)

    name := "newworkbook.xlsx"
    templateFile := "Calendar.xlsx"
    dataFile := "Sample_Data.xml"
    isWriteOver := true
    folder := "templates"
    storageName := "MyStorage"

    data, _ := os.Open("Sample_Data.xml")
    defer data.Close()

    result, _, err := apiInstance.PutWorkbookCreate(name, &templateFile, &dataFile, &isWriteOver, &folder, &storageName, data)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Printf("Response: %+v\n", result)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Hata İşleme

| Durum Kodu | Durum | Önerilen Eylem |
|------------|-------|----------------|
| **400** | Gerekli parametreler eksik veya geçersiz dosya türü. | Sorgu parametrelerini doğrulayın, şablon ve veri dosyalarının mevcut olduğunu ve desteklendiğini kontrol edin (`.xlsx`, `.xml`, `.json`). |
| **401** | JWT belirteci eksik, süresi dolmuş veya hatalı biçimlendirilmiş. | Client Id/Secret kullanarak yeni bir erişim belirteci oluşturun. |
| **413** | Yüklenen dosya hizmet boyut sınırını aşıyor (varsayılan 50 MB). | Dosya boyutunu küçültün veya çalışma kitabını daha küçük parçalara bölün. |
| **500** | Beklenmeyen sunucu hatası. | Kısa bir gecikmeden sonra tekrar deneyin; sorun devam ederse, `Request‑Id` başlığı değerini belirterek Aspose desteğiyle iletişime geçin. |

---

## Ayrıca Bkz.

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Mevcut bir çalışma kitabını belirli bir formata kaydetme.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Çalışma kitabı bilgilerini alma veya dosyayı indirme.  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Şablon veya veri dosyalarını bulut deposuna yükleme.  

---
---