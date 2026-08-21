---
title: "フォルダーの削除 – Aspose.Cells Cloud API | REST 経由でフォルダーを削除"
description: "Aspose.Cells Cloud ストレージからフォルダー（オプションで再帰的に）を削除する方法を学びます。DELETE /v4.0/cells/storage/folder/{path} エンドポイントを使用します。リクエスト構文、パラメーター、認証、サンプルコード、エラー処理を含みます。"
keywords: "Aspose.Cells, フォルダー削除, クラウドストレージ, API, REST, Excel, ファイル管理"
slug: delete-folder
date: 2026-07-30
---

# フォルダーの削除 – Aspose.Cells Cloud API

Aspose.Cells Cloud ストレージからフォルダー（およびその内容すべて）を削除します。

---

## 概要

**フォルダーの削除**操作は、Aspose.Cells Cloud が使用するストレージアカウントからフォルダーを完全に削除します。  
空のフォルダーを削除することも、`recursive` フラグを `true` に設定することで、フォルダー内に含まれるすべてのファイルおよびサブフォルダーとともにフォルダーを削除できます。このエンドポイントは、クリーンアップスクリプト、自動ワークフロー、または一時ディレクトリが不要になった場合に一般的に使用されます。

---

## HTTP リクエスト

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – 削除するフォルダーの完全なパス（URL エンコード済み）。

### 必須 HTTP ヘッダー

| ヘッダー名          | 値                                 | 説明                                   |
|---------------------|------------------------------------|----------------------------------------|
| `Authorization`     | `Bearer {access_token}`            | 認証サービスから取得した JWT トークン。 |
| `Accept`            | `application/json`                | 期待されるレスポンス形式。             |
| `Content-Type`      | `application/json` *（任意）*     | DELETE では不要ですが、送信可能です。  |

---

## 認証

Aspose.Cells Cloud では **JWT トークンベースの認証**を使用します。  
[認証エンドポイント](/authentication/) からアクセストークンを取得し、上記のように `Authorization` ヘッダーに含めてください。

```bash
-H "Authorization: Bearer {access_token}"
```

---

## パラメーター

| 名前            | 型      | 位置   | 必須 | 説明                                                                 |
|-----------------|---------|--------|------|----------------------------------------------------------------------|
| `path`          | 文字列  | パス   | はい  | 削除するフォルダーのパス（URL エンコード済み）。                      |
| `storageName`   | 文字列  | クエリ | いいえ | フォルダーを含むストレージ名。省略された場合、デフォルトストレージが使用されます。 |
| `recursive`     | 真偽値  | クエリ | いいえ | `true` → フォルダーを**およびそのすべての内容**を削除します。デフォルトは `false` です。 |

**クエリ文字列の例**

```
?storageName=MyStorage&recursive=true
```

---

## リクエスト例（cURL）

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## レスポンス

成功したリクエストは、空の JSON オブジェクトを含む **HTTP 200 OK** を返します：

```json
{}
```

操作の結果は「削除された／されなかった」の二値であるため、追加のペイロードは提供されません。

---

**HTTP ステータスコード**

| コード | 意味             | 説明                                               |
|--------|------------------|----------------------------------------------------|
| 200    | OK               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメーターが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。            |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバー側で予期しないエラーが発生しました。     |

エラーが発生した場合、レスポンスボディには `code` と `message` フィールドを含む JSON オブジェクトが含まれ、問題の内容が説明されます。

---

## SDK サンプルコード

以下の例は、公式にサポートされている SDK を使用して **フォルダーの削除** を呼び出す方法を示しています。`{access_token}` とパラメーター値は、各自の環境に合わせて置き換えてください。

<details><summary>🟦 C# (.NET)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API クライアントを設定
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// フォルダーを再帰的に削除
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

// API クライアントを初期化
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

// 設定
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// フォルダーを再帰的に削除
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

## 関連項目

- **[フォルダーの作成](/create-folder/)** – クラウドストレージに新しいフォルダーを作成します。  
- **[フォルダーのコピー](/copy-folder/)** – フォルダーとその内容を複製します。  
- **[フォルダーの移動](/move-folder/)** – フォルダーを別のパスに移動します。  
- **[OpenAPI 仕様]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder 操作</a>（対話型 API エクスプローラー）。

---

## SEO とアクセシビリティチェックリスト（内部用）

- **タイトルと H1** は正しいen-dash（–）を使用し、主要キーワード「フォルダーの削除」を含んでいます。  
- すべての見出しは論理的な階層（`H1 → H2 → H3`）に従っています。  
- UTF-8 エンコーディングのアーティファクトは残っていません。  
- メタキーワードは単一のクリーンなリストに統合されています（または、必要に応じて省略されています）。  
- 外部リンクにはセキュリティのために `rel="noopener noreferrer"` が含まれています。  
- UI アイコンおよび言語フラグ（ページ上で表示される場合）には `aria-label` / `alt` 属性が付与されている必要があります（例：`aria-label="English (US)"`）。  
- 各言語版に対して、ページの `<head>` 内に `<link rel="alternate" hreflang="xx" href="…">` タグを挿入することが推奨されます。  

---