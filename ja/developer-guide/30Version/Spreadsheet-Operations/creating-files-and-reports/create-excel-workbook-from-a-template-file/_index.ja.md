---
title: "テンプレートファイルを使用して Excel ワークブックを作成する方法"
second_title: "ドキュメント"
linktitle: "テンプレートファイル"
type: docs
url: /ja/create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, テンプレート, API, Aspose.Cells, ワークブック, REST, クラウド"
description: "Aspose.Cells Cloud REST API を使用して、テンプレートファイルから Excel ワークブックを生成する方法を学びます。前提条件、認証手順、cURL の使用例、エラー処理の詳細、および SDK のコードスニペットを含みます。"
weight: 30
---

# テンプレートファイルを使用して Excel ワークブックを作成する方法

既存のテンプレートファイルと、オプションで Smart-Marker の値を提供するデータファイルを使用して、新しい Excel ワークブックを作成します。この操作は、Aspose.Cells Cloud の **PUT** `/cells/{name}` エンドポイントを介して実行されます。

---

## 前提条件

| 必要条件 | 説明 |
|---------|------|
| **Aspose.Cells Cloud アカウント** | https://dashboard.aspose.cloud/ にサインアップし、**Client Id** / **Client Secret** を取得してください。 |
| **JWT アクセストークン** | [認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)に従って JWT トークンを生成してください。 |
| **テンプレートファイル** | テンプレート Excel ファイル (例: `Calendar.xlsx`) を、選択したストレージに **Upload File** API または UI を使用してアップロードしてください。 |
| **データファイル (オプション)** | Smart-Marker の値を含む JSON または XML ファイル (例: `Sample_Data.xml`)。 |
| **サポートされるストレージ** | デフォルトストレージ (`Default`) または、Aspose アカウントで設定されたカスタムストレージ。 |

---

## 認証

Aspose.Cells Cloud のすべてのリクエストは、`Authorization` ヘッダーに **Bearer JWT トークン** を含める必要があります：

```http
Authorization: Bearer {access_token}
```

トークンは事前に取得する必要があり、デフォルトでは有効期間は 1 時間です。

---

## リクエスト

### HTTP リクエスト

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| コンポーネント | 値 |
|---------------|-----|
| **メソッド** | `PUT` |
| **パス**   | `/cells/{name}` – `name` は新規作成するワークブックの名前 (拡張子を含む、例: `newworkbook.xlsx`)。 |
| **Content-Type** | `multipart/form-data` (ボディにデータファイルを送信する場合)。 |
| **Accept** | `application/json` |

### パスパラメータ

| 名前 | 型 | 必須 | 説明 |
|------|----|------|------|
| `name` | 文字列 | **はい** | 作成するワークブックの名前 (例: `newworkbook.xlsx`)。 |

### クエリパラメータ

| パラメータ | 型 | 必須 | デフォルト | 説明 |
|------------|----|------|-----------|------|
| `templateFile` | 文字列 | いいえ | — | クラウドに保存されているテンプレートファイルの名前。 |
| `dataFile` | 文字列 | いいえ | — | クラウドに保存されているデータファイル (XML または JSON) の名前。 |
| `isWriteOver` | 真偽値 | いいえ | `false` | 対象ファイルが既に存在する場合に上書きするかどうか。`true` または `false` を**引用符なし**で指定してください。 |
| `folder` | 文字列 | いいえ | — | テンプレート (およびオプションでデータファイル) が存在するフォルダのパス。 |
| `storageName` | 文字列 | いいえ | — | ファイルを含むストレージサービスの名前。 |
| `checkExcelRestriction` | 真偽値 | いいえ | `true` | 作成前にワークブックを Excel 制限に対して検証するかどうか。 |

### リクエストボディ (オプション)

Smart-Marker のプレースホルダに使用するデータをリクエスト内で直接送信する場合、**`data`** という名前の multipart ファイルパートとして含めてください。

| パート名 | 型 | 説明 |
|----------|----|------|
| `data` | ファイル | Smart-Marker の値を含む XML または JSON ファイル。 |

#### リクエストボディを使用した cURL の例

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*代わりに `dataFile` クエリパラメータを使用する場合、`-F` フラグは省略してください。*

---

## レスポンス

成功した呼び出しは、作成されたワークブックを説明する JSON ペイロードを含む **`200 OK`** (または新規ファイル生成時は **`201 Created`**) を返します。

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

### レスポンスデータの型

| プロパティ | 型 | 説明 |
|------------|----|------|
| `Code` | 整数 | API が返す HTTP 的なステータスコード。 |
| `Status` | 文字列 | ステータスのテキストによる説明。 |
| `File` | オブジェクト | 生成されたワークブックの詳細。 |
| `File.Name` | 文字列 | 作成されたワークブックのファイル名。 |
| `File.Size` | 整数 | サイズ (バイト単位)。 |
| `File.Path` | 文字列 | ストレージ内の相対パス。 |
| `File.Url` | 文字列 | 直接ダウンロード用 URL (同じ JWT トークンが必要)。 |

---

**HTTP ステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | フィルターが正常に適用され、レスポンスに操作の詳細が含まれています。 |
| 400 | 不正リクエスト | 必須パラメータが不足している、または無効なファイルタイプです。 |
| 401 | 認証されていません | JWT トークンが無効または不足しています。 |
| 413 | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。 |
| 500 | サーバー内部エラー | 予期しないサーバーエラーが発生しました。 |
---

## SDK の使用例

以下のスニペットは、公式 Aspose.Cells Cloud SDK を使用して **PutWorkbookCreate** を呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | 新規ドキュメント名。
var templateFile = "Calendar.xlsx"; // string | テンプレートファイル名。
var dataFile = "Sample_Data.xml"; // string | データファイル名 (オプション)。
var isWriteOver = true; // bool? | 存在する場合は上書き。
var folder = "templates"; // string | ファイルが存在するフォルダ。
var storageName = "MyStorage"; // string | ストレージ名。

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

## エラー処理

| ステータスコード | 状況 | 推奨対応 |
|----------------|------|----------|
| **400** | 必須パラメータが不足している、または無効なファイルタイプです。 | クエリパラメータを確認し、テンプレートおよびデータファイルが存在し、対応している形式 (`.xlsx`, `.xml`, `.json`) であることを確認してください。 |
| **401** | JWT トークンが不足している、期限切れ、または不正な形式です。 | Client Id / Secret を使用して、新しいアクセストークンを再生成してください。 |
| **413** | アップロードされたファイルがサービスのサイズ制限 (デフォルト 50 MB) を超えています。 | ファイルサイズを縮小するか、ワークブックを smaller parts に分割してください。 |
| **500** | 予期しないサーバーエラーが発生しました。 | 一時的な遅延後に再試行してください。問題が解決しない場合は、`Request-Id` ヘッダーの値とともに Aspose サポートに連絡してください。 |

---

## 関連項目

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – 既存のワークブックを指定された形式で保存します。  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – ワークブックの情報を取得するか、ファイルをダウンロードします。  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – テンプレートまたはデータファイルをクラウドストレージにアップロードします。  

---