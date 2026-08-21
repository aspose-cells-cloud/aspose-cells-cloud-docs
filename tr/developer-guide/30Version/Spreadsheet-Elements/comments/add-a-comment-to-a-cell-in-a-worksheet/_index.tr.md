---
---
title: "Çalışma Sayfası Yorumu Ekle"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki belirli bir hücreye yorum ekleyin (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, Bulut API, Çalışma Sayfası Yorumu Ekle, Excel, Elektronik Tablo, Hücre Yorumu"
weight: 20
api_version: "v3.0"
---

# Çalışma Sayfası Yorumu Ekle

Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabının çalışma sayfasındaki belirli bir hücreye yorum ekleyin.

---

## Ön Gereksinimler / Kimlik Doğrulama

* Her istek için bir **Bearer JWT belirteci** gerekir.  
  *Belirteç edinin* **/connect/token** uç noktası aracılığıyla (bkz. [Kimlik Doğrulama Kılavuzu](/cells/authentication/)).  
* Belirteci `Authorization` başlığında sağlayın:

```http
Authorization: Bearer <jwt token>
```

* Tüm çağrılar, belirteci ve verileri korumak için **HTTPS** üzerinden yapılmalıdır.

---

## HTTP İsteği

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Yol Parametreleri

| Ad        | Tür    | Gerekli  | Açıklama |
|-----------|--------|----------|-------------|
| `name`    | string | ✔️ | Çalışma kitabının dosya adı (örn. `test.xlsx`). |
| `sheetName` | string | ✔️ | Çalışma sayfasının adı (örn. `Sheet1`). |
| `cellName` | string | ✔️ | Hedef hücrenin adresi (örn. `A1`). |

### Sorgu Parametreleri

| Ad            | Tür    | Gerekli  | Açıklama |
|---------------|--------|----------|-------------|
| `folder`      | string | isteğe bağlı | Çalışma kitabının bulunduğu klasör. |
| `storageName` | string | isteğe bağlı | Dosyanın bulunduğu depolama hizmetinin adı. |

### İstek Gövdesi

Gövde, JSON formatında bir **Comment** nesnesi içermelidir.

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Comment Nesne Alanları**

| Alan                      | Tür     | Gerekli  | Açıklama |
|---------------------------|---------|----------|-------------|
| `CellName`                | string  | ✔️ | Hücre adresi (`{cellName}` yol değeriyle eşleşmelidir). |
| `Author`                  | string  | isteğe bağlı | Yorum yazarının adı. |
| `HtmlNote`                | string  | isteğe bağlı | HTML formatında yorum metni. |
| `Note`                    | string  | isteğe bağlı | Düz metin yorumu. |
| `AutoSize`                | boolean | isteğe bağlı | Yorum kutusunu otomatik boyutlandırma. |
| `IsVisible`               | boolean | isteğe bağlı | Varsayılan olarak yorumu göster. |
| `Width` / `Height`        | number  | isteğe bağlı | Yorum kutusunun boyutu (nokta cinsinden). |
| `TextHorizontalAlignment`| string  | isteğe bağlı | Yatay hizalama (`Left`, `Center`, `Right`). |
| `TextOrientationType`     | string  | isteğe bağlı | Metin döndürme (`NoRotation`, `Rotate90`, vs.). |
| `TextVerticalAlignment`  | string  | isteğe bağlı | Dikey hizalama (`Top`, `Center`, `Bottom`). |

---

## cURL Örneği

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## Yanıt Şeması

| Alan     | Tür    | Açıklama |
|----------|--------|-------------|
| `Comment` | object | Oluşturulan yorum nesnesi (yukarıdaki **Comment Nesne Alanları**na ek olarak bağlantı meta verilerini içerir). |
| `Code`    | integer | API tarafından döndürülen HTTP durum kodu (örn. `200`). |
| `Status`  | string  | Metinsel durum mesajı (örn. `"OK"`). |

`Comment` nesnesi ayrıca bir **link** alt nesnesi içerir:

| Alt Alan  | Tür    | Açıklama |
|-----------|--------|-------------|
| `Href`    | string | Yorum kaynağı için kendini referans alan URL. |
| `Rel`     | string | İlişki türü (`self`). |
| `Title`   | string | İsteğe bağlı başlık (null olabilir). |
| `Type`    | string | İsteğe bağlı MIME türü (null olabilir). |

---

## Başarılı Yanıt Örneği

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Hata Yanıtları

| HTTP Kodu | Açıklama | Örnek |
|-----------|-------------|---------|
| **400**   | Geçersiz istek – eksik veya geçersiz parametreler. | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | Yetkisiz erişim – eksik veya geçersiz belirteç. | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**   | Bulunamadı – çalışma kitabısı, çalışma sayfası veya hücre mevcut değil. | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500**   | İç sunucu hatası – sunucuda beklenmeyen bir durum oluştu. | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## SDK Örnekleri

Aşağıdaki SDK’lar bu işlem için hazır sarmalayıcılar sağlar. Yer tutucu değerleri (`<YOUR_TOKEN>`, `<FILE_NAME>` vb.) gerçek verilerle değiştirin.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API istemcisini yapılandırın
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Yorum nesnesini hazırlayın
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("WorksheetsApi.PutWorksheetComment çağrısında istisna: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'WorksheetsApi->putWorksheetComment çağrısında istisna: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "WorksheetsApi->put_worksheet_comment çağrısında istisna: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("WorksheetsApi->put_worksheet_comment çağrısında istisna: %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "WorksheetsApi->put_worksheet_comment çağrısında istisna: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Hata: %v\\n", err)
    } else {
        fmt.Printf("Yanıt: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Ayrıntılı Bilgi

* **Çalışma Sayfası Yorumunu Al** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Çalışma Sayfası Yorumunu Güncelle** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Çalışma Sayfası Yorumunu Sil** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Tüm Yorumları Temizle** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## Ek Notlar

* Uç nokta yolu **v3.0** sürümünü içerir. Daha yeni bir sürüm (**v3.1**) mevcuttur; en son özelliklere ihtiyacınız varsa temel URL’yi buna göre güncelleyin.  
* Tam OpenAPI tanımı için [Aspose.Cells Cloud API referansına](/cells/#/Worksheets/PutWorksheetComment) bakın.  
* Ortağınızın hız sınırlamalarına (HTTP 429) göre işlem yapmalı ve API yönergelerine göre yeniden deneme yapmalısınız.  

---
---