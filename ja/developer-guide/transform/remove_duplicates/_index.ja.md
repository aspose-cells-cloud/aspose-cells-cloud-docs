---
title: "重複の削除"
ArticleTitle: "重複の削除 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "重複の削除"
type: docs
url: /cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, 重複の削除, API"
description: "ワークシート、範囲、またはテーブル内の重複値を削除します。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスの重複削除機能

ワークシート、範囲、またはテーブル内の重複値を削除します。このメソッドは、指定された列を対象として重複する行を検出し、各重複セットについて最初の出現以外をすべて削除します。比較は通常、大文字・小文字を区別し、セルの値を正確に一致させます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス/クエリ文字列/HTTP ボディ | 説明 |
|--------------|--------|-------------------------------|------|
| Spreadsheet  | ファイル | FormData                      | スプレッドシートファイルをアップロードします。 |
| worksheet    | 文字列   | クエリ                        | ワークシート名。（オプション） |
| range        | 文字列   | クエリ                        | 重複削除対象の範囲名。（オプション） |
| table        | 文字列   | クエリ                        | 重複削除対象のテーブル名。（オプション） |
| outPath      | 文字列   | クエリ                        | （オプション）ワークブックが保存されるフォルダのパス。デフォルトは null です。 |
| outStorageName | 文字列 | クエリ                      | 出力ファイルのストレージ名。 |
| region       | 文字列   | クエリ                        | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式、日付の解析、ロケール固有の動作に影響を与えます。 |
| password     | 文字列   | クエリ                        | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明 |
| ------------ | ---- | ---- |
| [TBD]        | [TBD] | [TBD] |

### **レスポンス**

```json
{
  "File": "結果として得られたスプレッドシートのバイナリストリーム（例: .xlsx）"
}
```

**レスポンスのステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | 重複を削除した結果のスプレッドシートがファイルストリームとして返されます。 |
| 400 | Bad Request | 無効なリクエストパラメータ、または不正な URL です。 |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 413 | Payload Too Large | アップロードされたファイルが許容サイズ上限を超えています。 |
| 500 | Internal Server Error | データ取得中にスプレッドシートで異常が発生したか、その他のサーバーサイドエラーが発生しました。 |

## SDK を使用して重複削除を実行する方法

### 重複削除の仕様

[重複削除 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}) は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API を呼び出す方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "結果として得られたスプレッドシートのバイナリストリーム（例: .xlsx）"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：

```csharp
// C# 用 SDK サンプルコード
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Java 用 SDK サンプルコード
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Python 用 SDK サンプルコード
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception when calling TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---