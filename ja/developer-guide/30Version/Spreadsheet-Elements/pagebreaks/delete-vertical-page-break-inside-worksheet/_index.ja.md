---
title: 縦改ページ区切りを削除する – Aspose.Cells Cloud REST API
description: Aspose.Cells Cloud REST API（v3.0）を使用して Excel ワークシートから縦改ページ区切りを削除します。リクエスト構文、パラメータ、使用例、レスポンスコード、SDK スニペットを含みます。
keywords: 縦改ページ区切りの削除, Aspose.Cells Cloud, REST API
slug: delete-vertical-page-break
api_version: v3.0
---

# 縦改ページ区切りを削除する

Aspose.Cells Cloud REST API を使用して、Excel ワークブックのワークシートから縦改ページ区切りを削除します。

---

## 前提条件

* `Authorization` ヘッダーに **JWT 認証トークン** を指定する必要があります。  
* ワークブック（`{name}`）は、指定された **フォルダー** または **ストレージ** に保存されており、API クライアントからアクセス可能である必要があります。

---

## HTTP リクエスト

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| パラメータ     | 型      | 位置   | 必須 | 説明 |
|---------------|---------|--------|------|------|
| **name**      | 文字列  | パス   | はい  | Excel ファイルの名前。 |
| **sheetName** | 文字列  | パス   | はい  | 改ページ区切りを含むワークシートの名前。 |
| **index**     | 整数    | パス   | はい  | 削除する縦改ページ区切りの 0 から始まるインデックス。 |
| **folder**    | 文字列  | クエリ | いいえ | ファイルが保存されているフォルダーのパス。 |
| **storageName**| 文字列 | クエリ | いいえ | ストレージサービスの名前。 |

---

## リクエストの例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## 成功レスポンス

| コード | 説明 |
|--------|------|
| **200** | 縦改ページ区切りが正常に削除されました。 |

**ペイロードの例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## エラーレスポンス

| HTTP コード | 説明 |
|-------------|------|
| **401** | 認証エラー – トークンが不足しているか、無効です。 |
| **404** | 見つかりません – 指定されたファイル、ワークシート、または改ページ区切りのインデックスが存在しません。 |
| **400** | 不正なリクエスト – リクエスト構文が不正、またはパラメータが無効です。 |
| **500** | サーバー内部エラー – 予期しない状態が発生しました。 |

**エラーペイロードの例**

*401 – 認証エラー*

```json
{
  "Code": 401,
  "Message": "Invalid authentication token."
}
```

*404 – 見つかりません*

```json
{
  "Code": 404,
  "Message": "The specified file, worksheet, or page‑break index was not found."
}
```

*400 – 不正なリクエスト*

```json
{
  "Code": 400,
  "Message": "The request parameters are invalid or malformed."
}
```

*500 – サーバー内部エラー*

```json
{
  "Code": 500,
  "Message": "An unexpected server error occurred."
}
```

---

## SDK コードサンプル

以下の例は、さまざまな Aspose.Cells Cloud SDK を使用して **DeleteVerticalPageBreak** 操作を呼び出す方法を示しています。

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(PHP、Ruby、Perl およびその他の言語向けの SDK スニペットも同様のパターンで提供されており、公式 GitHub リポジトリから入手可能です。)*

---

## 関連リソース

* **OpenAPI スペック** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **Aspose.Cells Cloud SDK** – <https://github.com/aspose-cells-cloud>  
* **認証ガイド** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*最終更新日: 2026‑07‑30*