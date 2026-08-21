---
title: 条件付き書式に条件を追加する
description: Aspose.Cells Cloud REST API（v3.0）を使用して、ワークシートの条件付き書式に条件を追加する方法を学びます。エンドポイント、パラメータ、認証、cURL の例、SDK スニペット、エラー処理を含みます。
keywords: "Aspose.Cells Cloud, 条件付き書式, 条件の追加, REST API, Excel, ワークシート"
type: docs
url: /ja/conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# 条件付き書式に条件を追加する

Aspose.Cells Cloud REST API（v3.0）を使用して、ワークシート内の既存の条件付き書式ルールに条件を追加します。

---

## 前提条件

| 必要条件 | 詳細 |
|----------|------|
| **認証** | OAuth 2.0 フローにより取得した有効な JWT アクセストークン（Bearer） |
| **API バージョン** | v3.0 – エンドポイント URL には `/v3.0/` が含まれます |
| **ストレージ** | ワークブックは Aspose.Cells Cloud がアクセス可能なストレージの場所に配置されている必要があります（デフォルトは `Default`） |
| **権限** | 対象ワークブックに対する読み書き権限 |
| **対応フォーマット** | Aspose.Cells がサポートする任意のワークブックフォーマット（例：`.xlsx`、`.xls`、`.xlsm`） |

---

## エンドポイント

**HTTP メソッド:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| パラメータ | 位置 | 型 | 必須 | 説明 |
|------------|------|----|------|------|
| `name` | パス | 文字列 | **はい** | ワークブックファイル名（拡張子を含む） |
| `sheetName` | パス | 文字列 | **はい** | 条件付き書式を含むワークシート名 |
| `index` | パス | 整数 | **はい** | 修改する条件付き書式コレクションの 0 から始まるインデックス |
| `type` | クエリ | 文字列 | **はい** | 条件の種類。許可される値：`CellValue`、`Expression`、`ColorScale`、`DataBar`、`IconSet`、`Top10`、`UniqueValues`、`DuplicateValues`、`ContainsText`、`NotContainsText`、`BeginsWith`、`EndsWith`、`ContainsBlanks`、`NotContainsBlanks`、`ContainsErrors`、`NotContainsErrors`、`TimePeriod`、`AboveAverage` |
| `operatorType` | クエリ | 文字列 | **はい** | 条件の演算子。許可される値：`Between`、`Equal`、`GreaterThan`、`GreaterOrEqual`、`LessThan`、`None`、`NotBetween`、`NotEqual` |
| `formula1` | クエリ | 文字列 | **はい** | 条件に関連付けられた最初の数式または値 |
| `formula2` | クエリ | 文字列 | いいえ | 2 番目の数式または値（`Between` など、2 つの値を必要とする演算子の場合に必要） |
| `folder` | クエリ | 文字列 | いいえ | ワークブックが配置されているストレージ内のフォルダ |
| `storageName` | クエリ | 文字列 | いいえ | ストレージサービスの名前 |

> **注意:** すべてのパスパラメータ（`name`、`sheetName`、`index`）およびクエリパラメータ `type`、`operatorType`、`formula1` は必須です。`formula2`、`folder`、`storageName` は任意です。

---

## リクエスト例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*`<jwt_token>` を有効なアクセストークンに置き換え、必要に応じて `name`、`sheetName`、`index`、およびクエリ値を調整してください。*

---

## 成功時の応答

```json
{
  "Code": "200",
  "Status": "OK"
}
```

この応答は条件が正常に追加されたことを示します。操作は、HTTP ステータスコードと短いステータスメッセージを含む汎用的な `CellsCloudResponse` オブジェクトを返します。

---

## エラー応答

| HTTP コード | 理由 | 例（ボディ） |
|-------------|------|--------------|
| **400** | 不正なリクエスト – パラメータが不足または無効です | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | 認証エラー – JWT トークンが不足または無効です | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | 見つかりません – ワークブック、ワークシート、または条件付き書式のインデックスが存在しません | `{ "Code":"404", "Message":"File not found." }` |
| **500** | サーバー内部エラー – 予期しないサーバー障害 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## 注意事項およびよくある落とし穴

* **パラメータのエンコード** – `formula1`／`formula2` 内の特殊文字は URL エンコードしてください（例：スペース → `%20`）。  
* **演算子の互換性** – 一部の演算子（例：`Between`）では `formula1` と `formula2` の両方が必要です。単一の値のみを必要とする演算子の場合は `formula2` を省略してください。  
* **条件付き書式のインデックス** – インデックスは 0 から始まります。不確かな場合は **条件付き書式の取得** エンドポイントを使用して正しいインデックスを取得してください。  
* **ストレージフォルダ** – ワークブックがデフォルト以外のフォルダにある場合は、`folder` クエリパラメータを指定してください。指定しない場合、API はルートフォルダにあるとみなします。  
* **レート制限** – Aspose.Cells Cloud はアカウントごとにリクエスト数の制限を設けています。429 応答を受けた場合は、バックオフして短い遅延の後に再試行してください。  

---

## SDK の例

以下は、最も人気のある SDK 用の実行可能なスニペットです。プレースホルダー値（`YOUR_FILE`、`YOUR_SHEET` など）を各自のデータに置き換えてください。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // optional
        string storageName = null;     // optional

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
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
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **SDK が未対応の場合** – 必要な言語がリストにない場合は、汎用の **API リファレンス** を参照して HTTP リクエストを手動で構築してください。

---

## 関連項目

- **[条件付き書式の取得](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – ワークシートの条件付き書式ルール一覧を取得します。  
- **[条件付き書式の削除](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – 既存の条件付き書式ルールを削除します。  
- **[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – 本操作の完全な機械可読定義です。  

---