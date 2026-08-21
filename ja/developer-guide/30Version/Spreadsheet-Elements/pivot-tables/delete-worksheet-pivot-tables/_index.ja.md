---
title: "Excelワークシートからすべてのピボットテーブルを削除する"
description: "Aspose.Cells Cloud REST API を使用して、指定したワークシートからすべてのピボットテーブルを削除します。"
keywords: "Aspose.Cells, ピボットテーブル, 削除, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Excelワークシートからすべてのピボットテーブルを削除する

## 概要
この操作は、Excelファイル内の指定されたワークシートから**すべての**ピボットテーブルを削除します。ワークシートの分析をリセットしたり、単一の呼び出しで使用されていないピボットテーブルをクリーンアップしたりする場合に便利です。

## 前提条件
APIを呼び出す前に、以下の手順を完了していることを確認してください。

1. **Aspose Cloud アカウント** – まだお持ちでない場合は、Aspose Cloud アカウントにサインアップしてください。  
2. **JWT トークン** – 認証用の JSON Web トークン (JWT) を生成します。詳細については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を参照してください。  
3. **ストレージの設定** – 対象の Excel ファイルを Aspose Cloud ストレージまたは接続された外部ストレージにアップロードしてください。ファイルが配置されている**フォルダー**と**ストレージ名**（該当する場合）をメモしておいてください。

## 認証
Aspose.Cells Cloud API は **JWT トークンベースの認証** を要求します。各リクエストの `Authorization` ヘッダーにトークンを含めてください：

```
Authorization: Bearer <jwt token>
```

## HTTP リクエスト

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### パスパラメーター
| 名前 | 型     | 必須 | 説明 |
|------|--------|------|------|
| `name` | 文字列 | はい | Excel ファイルの名前（例: `Sample.xlsx`）。 |
| `sheetName` | 文字列 | はい | すべてのピボットテーブルを削除するワークシートの名前（例: `Sheet1`）。 |

### クエリパラメーター
| 名前 | 型     | 必須 | 説明 |
|------|--------|------|------|
| `folder` | 文字列 | いいえ | ファイルが配置されているフォルダー。 |
| `storageName` | 文字列 | いいえ | 使用するストレージ名（ファイルがデフォルトストレージにない場合）。 |

## リクエスト例 (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## 成功時のレスポンス
サービスは、操作のステータスを示す標準の `CellsCloudResponse` オブジェクトを返します。

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## エラー処理

| HTTP ステータス | 意味 | 例のペイロード |
|----------------|------|----------------|
| **400** | 不正リクエスト – 必須パラメーターが欠落している、または無効です | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | 認証エラー – 無効または期限切れの JWT です | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | 見つかりません – ファイルまたはワークシートが存在しません | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | サーバー内部エラー – 予期しないエラーが発生しました | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## SDK の例

以下のスニペットは、いくつかの Aspose.Cells Cloud SDK を使用して操作を呼び出す方法を示しています。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API クライアントを初期化
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// リクエストパラメーターを設定
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# API クライアントを設定
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*その他の SDK（Go、PHP、Ruby、Swift、Perl、Android）は、[Aspose.Cells Cloud SDK リポジトリ](https://github.com/aspose-cells-cloud)で利用できます。*

## 関連項目
- [特定のピボットテーブルを削除する](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [ワークシート内のすべてのピボットテーブルを取得する](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [認証の概要](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [DeleteWorksheetPivotTables の OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*最終更新日: 2026-07-30。すべてのコンテンツは UTF‑8 エンコードされています。*