---
title: "ワークシートのすべてのコメントを削除する"
description: "Aspose.Cells Cloud API を使用して Excel ファイル内のワークシートからすべてのコメントを削除します。DELETE エンドポイント、必要なパラメータ、認証、cURL リクエストのサンプル、応答形式、エラーコード、SDK の使用例を学びます。"
keywords: "Aspose, Cells, コメントの削除, ワークシート, API, REST, Excel, クラウド"
url: /comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# ワークシートのすべてのコメントを削除する

**API バージョン:** `v3.0`  
**リソース:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud は、指定されたワークシートから**すべての**コメントを削除するための強力な REST エンドポイントを提供します。この操作は元に戻すことができないため、実行後はコメントを復元できません。

---

## 前提条件

| 必要条件 | 詳細 |
|---------|------|
| **認証** | `Authorization` ヘッダーに有効な JWT アクセストークン (`Bearer <jwt token>`) が必要です。トークンは [OAuth2 認証フロー](https://docs.aspose.cloud/cells/authentication/) で取得できます。 |
| **ストレージ** | ファイルは Aspose.Cells Cloud からアクセス可能なストレージに配置されている必要があります（`storageName` を省略した場合はデフォルトストレージが使用されます）。 |
| **権限** | トークンには対象ファイルの読み取りおよび書き込み権限が必要です。 |
| **SDK（オプション）** | .NET、Java、PHP、Ruby、Node.js、Python、Perl、Go 向けの SDK が利用可能です（**SDK の使用例**のセクションを参照）。 |

---

## HTTP リクエスト

### エンドポイント

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### パスパラメータ

| 名前 | 型 | 説明 |
|------|----|------|
| `name` | string | Excel ファイル名（例: `test.xlsx`） |
| `sheetName` | string | ワークシート名（例: `Sheet1`） |

### クエリパラメータ

| 名前 | 型 | 必須 | 説明 |
|------|----|------|------|
| `folder` | string | オプション | ファイルが配置されているフォルダのパス |
| `storageName` | string | オプション | ファイルが配置されているストレージ名 |

### リクエストヘッダー

| ヘッダー | 値 |
|---------|----|
| `Authorization` | `Bearer <jwt token>` |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

---

## リクエスト例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*`test.xlsx`、`Sheet1`、`Documents`、`MyStorage`、および `<jwt token>` を実際の値に置き換えてください。*

---

## 応答

### 成功（200）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

応答本文は `CellsCloudResponse` モデルに準拠します。

### エラー応答

| HTTP コード | 意味 | 例（本文） |
|-------------|------|------------|
| **400** | 不正なリクエスト — 無効なパラメータ。 | `{ "Code": 400, "Message": "Invalid request." }` |
| **401** | 認証失敗 — JWT トークンが不足または無効。 | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | 見つからない — ファイルまたはワークシートが存在しない。 | `{ "Code": 404, "Message": "Resource not found." }` |
| **500** | サーバー内部エラー。 | `{ "Code": 500, "Message": "Server error." }` |

---

## SDK の使用例

以下のスニペットは、公式 Aspose.Cells Cloud SDK（バージョン 3.13.0）を使用してエンドポイントを呼び出す方法を示しています。プレースホルダー値（`<fileName>`、`<sheet>`、`<jwt token>` など）を実際のデータに置き換えてください。

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | ファイル名
var sheetName = "Sheet1"; // string | ワークシート名
var folder = "Documents"; // string | フォルダパス（オプション）
var storageName = "MyStorage"; // string | ストレージ名（オプション）

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("WorksheetsApi.DeleteWorksheetComments の呼び出し時に例外が発生しました: " + e.Message );
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
    echo 'WorksheetsApi->deleteWorksheetComments の呼び出し時に例外が発生しました: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # オプション
storage_name = 'MyStorage'    # オプション

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "WorksheetsApi->delete_worksheet_comments の呼び出し時に例外が発生しました: #{e}"
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
    .catch((error) => console.error("Error:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # オプション
storage_name = "MyStorage"    # オプション

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("WorksheetsApi->delete_worksheet_comments の呼び出し時に例外が発生しました:", e)
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
    print "WorksheetsApi->delete_worksheet_comments の呼び出し時に例外が発生しました: $@\n";
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
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## 注意事項と制限事項

* この操作は、指定されたワークシート内の**すべてのコメントを削除**します。元に戻せないため、注意して実行してください。
* このリクエストは**リクエストボディを受け取りません**。必要な情報はすべて URL とヘッダーで渡されます。
* 対象ファイルが**パスワード保護**されている場合、またはワークシートが**読み取り専用**の場合、原因に応じて API は `400` または `401` エラーを返します。
* エンドポイントは、**Aspose Cloud ストレージ**に加えて、`storageName` を介して正しく参照された **Amazon S3**、**Azure Blob**、**Google Cloud Storage** 上のファイルでも動作します。

---

## 関連リソース

* **OpenAPI スペック** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **認証ガイド** – [Aspose.Cells Cloud の OAuth2](https://docs.aspose.cloud/cells/authentication/)
* **SDK リポジトリ** – <https://github.com/aspose-cells-cloud>
* **一般的なワークシート API** – <https://docs.aspose.cloud/cells/worksheets/>

---

*最終更新日: 2026-07-30*
---