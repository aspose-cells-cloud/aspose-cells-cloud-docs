---
title: "ワークシートのコメントを追加する"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートの特定のセルにコメントを追加します（PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}）。"
keywords: "Aspose.Cells, Cloud API, ワークシートのコメントを追加, Excel, スプレッドシート, セルコメント"
weight: 20
api_version: "v3.0"
---

# ワークシートのコメントを追加する

Aspose.Cells Cloud REST API を使用して、Excel ワークブックのワークシート内の特定のセルにコメントを追加します。

---

## 前提条件 / 認証

* 各リクエストには **Bearer JWT トークン** が必要です。  
  *トークンの取得* は **/connect/token** エンドポイントを通じて行います（[認証ガイド](/cells/authentication/) を参照）。  
* トークンを `Authorization` ヘッダーに含めてください：

```http
Authorization: Bearer <jwt token>
```

* すべての呼び出しは、トークンとデータを保護するために **HTTPS** 経由で行う必要があります。

---

## HTTP リクエスト

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### パスパラメーター

| 名前         | 型     | 必須 | 説明 |
|-------------|--------|------|------|
| `name`      | 文字列 | ✔️   | ワークブックのファイル名（例：`test.xlsx`） |
| `sheetName` | 文字列 | ✔️   | ワークシート名（例：`Sheet1`） |
| `cellName`  | 文字列 | ✔️   | 対象セルのアドレス（例：`A1`） |

### クエリパラメーター

| 名前           | 型     | 必須 | 説明 |
|---------------|--------|------|------|
| `folder`      | 文字列 | 任意 | ワークブックが配置されているフォルダー |
| `storageName` | 文字列 | 任意 | ファイルが配置されているストレージサービス名 |

### リクエストボディ

ボディには、JSON 形式の **Comment** オブジェクトを含める必要があります。

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

**Comment オブジェクトのフィールド**

| フィールド                     | 型      | 必須 | 説明 |
|------------------------------|---------|------|------|
| `CellName`                   | 文字列  | ✔️   | セルアドレス（パスパラメーターの `{cellName}` と一致している必要があります） |
| `Author`                     | 文字列  | 任意 | コメントの作成者名 |
| `HtmlNote`                   | 文字列  | 任意 | HTML 形式のコメントテキスト |
| `Note`                       | 文字列  | 任意 | 平文のコメント |
| `AutoSize`                   | 真偽値  | 任意 | コメントボックスの自動サイズ調整 |
| `IsVisible`                  | 真偽値  | 任意 | デフォルトでコメントを表示する |
| `Width` / `Height`           | 数値    | 任意 | コメントボックスのサイズ（ポイント単位） |
| `TextHorizontalAlignment`   | 文字列  | 任意 | 水平方向の配置（`Left`, `Center`, `Right`） |
| `TextOrientationType`       | 文字列  | 任意 | テキストの回転（`NoRotation`, `Rotate90`, …） |
| `TextVerticalAlignment`     | 文字列  | 任意 | 垂直方向の配置（`Top`, `Center`, `Bottom`） |

---

## cURL の例

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

## レスポンススキーマ

| フィールド  | 型     | 説明 |
|-----------|--------|------|
| `Comment` | オブジェクト | 作成されたコメントオブジェクト（上記の **Comment オブジェクトのフィールド** に加え、リンクメタデータを含む） |
| `Code`    | 整数   | API が返す HTTP ステータスコード（例：`200`） |
| `Status`  | 文字列 | テキスト形式のステータスメッセージ（例：`"OK"`） |

`Comment` オブジェクトには、サブオブジェクト **link** も含まれます：

| サブフィールド | 型     | 説明 |
|---------------|--------|------|
| `Href`        | 文字列 | コメントリソースの自己参照 URL |
| `Rel`         | 文字列 | 関係タイプ（`self`） |
| `Title`       | 文字列 | オプションのタイトル（`null` の場合あり） |
| `Type`        | 文字列 | オプションの MIME タイプ（`null` の場合あり） |

---

## 成功レスポンスの例

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

## エラーレスポンス

| HTTP コード | 説明 | 例 |
|------------|------|----|
| **400**    | 不正なリクエスト – パラメーターが不足または無効です。 | `{ "Error": { "Code": "InvalidParameter", "Message": "The 'cellName' parameter is missing or malformed." }, "Code": 400, "Status": "Bad Request" }` |
| **401**    | 認証エラー – トークンが不足または無効です。 | `{ "Error": { "Code": "InvalidToken", "Message": "Authentication failed." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**    | 見つかりません – ワークブック、ワークシート、またはセルが存在しません。 | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' not found." }, "Code": 404, "Status": "Not Found" }` |
| **500**    | サーバー内部エラー – サーバー上で予期しない状態が発生しました。 | `{ "Error": { "Code": "ServerError", "Message": "An unexpected error occurred." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## SDK の例

以下の SDK は、この操作用の既製ラッパーを提供しています。プレースホルダー（`<YOUR_TOKEN>`、`<FILE_NAME>` など）を実際のデータで置き換えてください。

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API クライアントの設定
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// コメントオブジェクトの準備
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
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
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
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
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
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
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
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
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
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
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
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## 関連項目

* **ワークシートのコメントを取得** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **ワークシートのコメントを更新** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **ワークシートのコメントを削除** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **すべてのコメントをクリア** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## 補足事項

* エンドポイントのパスには **v3.0** が含まれています。最新の機能が必要な場合は、新しいバージョン（**v3.1**）が利用可能であるため、ベース URL を適宜更新してください。  
* 完全な OpenAPI 定義については、[Aspose.Cells Cloud API リファレンス](/cells/#/Worksheets/PutWorksheetComment) を参照してください。  
* API のガイドラインに従い、レート制限（HTTP 429）およびリトライ処理を適切に実装してください。  

---