---
title: "ワークシートのコメント削除 API – Aspose.Cells Cloud"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークシート内の特定のセルコメントを削除します。エンドポイント、パラメーター、リクエスト/レスポンスの例、SDK スニペット、エラーハンドリングを含みます。"
keywords: "Aspose.Cells, コメント削除, Excel API, REST, ワークシートコメント"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# ワークシートのコメント削除 API – Aspose.Cells Cloud

> **最終更新日:** 2026年7月30日  

## 概要
**コメント**は、Excel ワークシート内の特定のセルに付加されるテキストメモです。  
**コメント削除**操作は、指定されたセルからコメントを削除します。

![Aspose.Cells Cloud – ワークシートのコメント削除の図解](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – ワークシートのコメント削除 API")

## 認証
すべての Aspose.Cells Cloud エンドポイントは **JWT トークンベースの認証**を必要とします。  
`Authorization` ヘッダーにトークンを含めてください：

```
Authorization: Bearer <jwt token>
```

JWT トークンの取得方法については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。

## 前提条件
- 有効な JWT アクセストークン。  
- 対象のワークブック（`{name}`）が指定されたストレージ場所に存在していること。  
- オプション: 好みの言語向けの Aspose.Cells Cloud SDK のいずれかがインストールされていること。

## HTTP リクエスト

### エンドポイント
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### パスパラメーター
| パラメーター | 型     | 必須 | 説明 |
|-------------|--------|------|------|
| `name`      | 文字列 | ✅ | Excel ワークブックの名前（例: `test.xlsx`）。 |
| `sheetName` | 文字列 | ✅ | コメントを含むワークシートの名前。 |
| `cellName`  | 文字列 | ✅ | コメントを削除するセルのアドレス（例: `A1`）。 |

### クエリパラメーター
| パラメーター   | 型     | 必須 | 説明 |
|---------------|--------|------|------|
| `folder`      | 文字列 | ❌ | ワークブックが保存されているフォルダーのパス。省略した場合、ルートフォルダーが使用されます。 |
| `storageName` | 文字列 | ❌ | ストレージサービスの名前（例: `MyCloud`）。省略した場合、デフォルトのストレージが使用されます。 |

## リクエスト例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## レスポンス

### 成功 (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP ステータスコード**

| コード | 意味               | 説明 |
|--------|--------------------|------|
| 200    | OK                 | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request        | パラメーターが不足しているか、無効です（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized       | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large  | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバーで予期せぬエラーが発生しました。 |

### エラーレスポンス

| HTTP コード | 説明 |
|-------------|------|
| 400 | リクエストエラー – パラメーターが不足しているか、不正な形式です。 |
| 401 | 認証エラー – トークンが無効または不足しています。 |
| 404 | 見つかりません – ファイル、ワークシート、またはコメントが存在しません。 |
| 500 | サーバー内部エラー – サーバー上で予期せぬ状態が発生しました。 |

## SDK の例
以下は、最も人気のある言語用の実行可能なスニペットです。`<jwt token>`、`test.xlsx`、`Sheet1`、`A1` を各自の値に置き換えてください。

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// API クライアントを設定
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

## 関連する操作
- [ワークシートにコメントを追加](/comments/add/)  
- [ワークシートのコメントを更新](/comments/update/)  

## レート制限
Aspose.Cells Cloud は、デフォルトで **アカウントあたり1分間に 100 リクエスト**のレート制限を適用します。この制限を超えると HTTP 429 Too Many Requests が返されます。レート制限を回避するには、指数バックオフを実装するか、`Retry-After` ヘッダーを尊重してください。

## 関連リンク
- **OpenAPI スペック:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **認証ガイド:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **SDK リポジトリ:** <https://github.com/aspose-cells-cloud>  

---