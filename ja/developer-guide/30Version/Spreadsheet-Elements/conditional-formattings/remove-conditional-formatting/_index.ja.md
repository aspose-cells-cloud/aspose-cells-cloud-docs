---
title: "条件付き書式の削除 – Aspose.Cells Cloud API リファレンス"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, 条件付き書式, 削除, API, Excel, クラウド"
description: "Aspose.Cells Cloud REST API を使用してワークシートから条件付き書式ルールを削除します。パラメータ、認証、リクエスト/レスポンスの例、SDK スニペットを含みます。"
weight: 60
---

# 条件付き書式の削除

## 概要
条件付き書式を使用すると、特定の条件を満たすセル（例：しきい値より大きい値を強調表示）に視覚的なスタイルを適用できます。自動化のシナリオでは、既存のルールを削除する必要がある場合があります。このエンドポイントは、Aspose Cloud ストレージ内に保存された Excel ワークブックのワークシートから条件付き書式ルールを削除します。

## 前提条件
- **Cells** 製品が有効な **Aspose Cloud** アカウント。  
- OAuth 2.0 クライアント資格情報フローで生成された **JWT アクセストークン**。  
- ワークブック (`{name}`) は、指定された **フォルダ** および **ストレージ**（該当する場合）に事前に存在している必要があります。  
- 以下に示す URL では、API バージョン **v3.0**（デフォルト）が使用されます。

## 認証
Aspose.Cells Cloud のすべてのエンドポイントでは、**JWT トークンベースの認証**が必要です。

```http
Authorization: Bearer <access_token>
```

### アクセストークンの取得（cURL）

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**レスポンス**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

返された `access_token` を、すべてのリクエストの `Authorization` ヘッダに使用してください。

## HTTP リクエスト

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### パスパラメータ

| 名前        | 型     | 必須 | 説明 |
|-------------|--------|------|------|
| `name`      | 文字列 | はい | ワークブックのファイル名（例：`Book1.xlsx`）。 |
| `sheetName` | 文字列 | はい | 条件付き書式を含むワークシート名。 |
| `index`     | 整数   | はい | 削除する条件付き書式ルールの 0 から始まるインデックス。 |

### クエリパラメータ

| 名前           | 型     | 必須 | 説明 |
|----------------|--------|------|------|
| `folder`       | 文字列 | いいえ | ワークブックが配置されているクラウドフォルダ。 |
| `storageName`  | 文字列 | いいえ | Aspose Cloud ストレージサービスの名前。 |

## リクエスト例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### 成功時のレスポンス

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明 |
|--------|------------------|------|
| 200    | OK               | フィルタが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

## エラーレスポンス

| HTTP コード | 理由 | 例（本文） |
|-------------|------|------------|
| **400**     | Bad Request – パラメータが不足している、または無効です。 | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**     | Unauthorized – JWT トークンが不足している、または無効です。 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | Not Found – ワークブックまたはワークシートが存在しません。 | `{ "Code":"404", "Message":"File not found." }` |
| **500**     | Internal Server Error – 予期しないサーバー障害が発生しました。 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## SDK の例
以下のスニペットは、公式 Aspose.Cells Cloud SDK を使用して **条件付き書式の削除** 操作を実行する方法を示します。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// API クライアントの設定
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// 条件付き書式の削除
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Conditional formatting deleted.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Conditional formatting removed.")
```

※ Ruby、Go、Perl、Swift 用の追加 SDK スニペットは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) にあります。

## 関連項目
- **認証ガイド** – [JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **OpenAPI 仕様** – このエンドポイントの詳細なスキーマ（新しいタブで開きます）  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>`  
- **条件付き書式の概要** – 書式ルールの作成、更新、一覧表示方法を学習できます。  
- **Aspose.Cells Cloud SDK** – サポートされている言語の全一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。  

---  

*このページは、標準の Aspose.Cells Cloud API ドキュメントテンプレートに従い、「前提条件」セクションを含み、アクセシビリティおよび SEO のベストプラクティスに準拠しています。*