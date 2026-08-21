---
title: "Aspose.Cells Cloud API – ドキュメント プロパティの更新（設定）"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークブック内のドキュメント プロパティを設定または作成します。"
keywords: "Aspose.Cells, Cloud API, ドキュメント プロパティの更新, Excel メタデータ, REST API, SDK サンプル"
api_version: "v3.0"
---

# 概要
**ドキュメント プロパティの更新（設定）** 操作により、Aspose Cloud ストレージに保存された Excel ワークブック内で、新しいドキュメント プロパティを作成または既存のものを変更できます。

*エンドポイント*  
`PUT https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}`  

このリクエストは、設定するプロパティを記述する JSON ペイロードを受け取ります。

---

## 前提条件
- 有効な **JWT アクセストークン**（**認証**セクションを参照）。  
- 対象のワークブック（`{name}`）は、Aspose Cloud ストレージ（または指定したフォルダ）に既に存在している必要があります。  
- ストレージ名（`storageName`）は任意です。省略した場合、デフォルトのストレージが使用されます。

---

## 認証
Aspose.Cells Cloud は **JWT トークンベースの認証**を使用します。トークンは `Authorization` ヘッダに含めてください：

```http
Authorization: Bearer <jwt-token>
```

JWT トークンの取得方法の詳細については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。

---

## HTTP リクエスト

| 要素             | 値 |
|------------------|-----|
| **メソッド**     | `PUT` |
| **URI**          | `/cells/{name}/documentproperties/{propertyName}` |
| **Content-Type**| `application/json` |
| **Accept**       | `application/json` |

### パスパラメータ

| 名前            | タイプ   | 必須 | 説明 |
|-----------------|----------|------|------|
| `name`          | 文字列   | ✅ | Excel ファイル名（拡張子を含む）。 |
| `propertyName`  | 文字列   | ✅ | 設定または作成するドキュメント プロパティの名前。 |

### クエリパラメータ

| 名前            | タイプ   | 必須 | 説明 |
|-----------------|----------|------|------|
| `folder`        | 文字列   | ❌ | ワークブックが存在するストレージ内のフォルダパス。 |
| `storageName`   | 文字列   | ❌ | ストレージサービスの名前。省略した場合、デフォルトのストレージが使用されます。 |

### リクエストボディ – ドキュメント プロパティ オブジェクト

```json
{
  "Name": "author",
  "Value": "aspose",
  "BuiltIn": "string",          // 任意（例: "true" または "false"）
  "Link": {                     // 任意
    "Href": "string",
    "Rel": "string",
    "Title": "string",
    "Type": "string"
  }
}
```

| フィールド | タイプ   | 必須 | 説明 |
|-----------|----------|------|------|
| **Name**   | 文字列   | ✅ | プロパティ名（例: `author`）。 |
| **Value**  | 文字列   | ✅ | プロパティの値。 |
| **BuiltIn**| 文字列   | ❌ | プロパティが組み込みかどうかを示します。 |
| **Link**   | オブジェクト | ❌ | ハイパーリンク情報（`Href`、`Rel`、`Title`、`Type`）。 |

---

## 例：リクエスト（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author?folder=Docs&storageName=MyStorage" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -d '{
        "Name": "author",
        "Value": "aspose",
        "BuiltIn": "false",
        "Link": {
          "Href": "https://example.com",
          "Rel": "self",
          "Title": "Author link",
          "Type": "text/html"
        }
      }'
```

### 例：成功時のレスポンス

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|--------|------------------------------|--------------------------------------------------|
| 200    | OK                           | フィルタが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request                  | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error        | サーバーで予期しないエラーが発生しました。 |
|        |                              |                                                  |

---

## SDK サンプル
以下のコードスニペットは、公式の Aspose.Cells Cloud SDK を使用してこの操作を呼び出す方法を示しています。

| 言語      | サンプル |
|-----------|----------|
| **C#** | <details><summary>C# の例を表示</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new DocumentPropertiesApi();\nvar request = new PutDocumentPropertyRequest(\n    name: "test.xlsx",\n    propertyName: "author",\n    property: new CellsDocumentProperty {\n        Name = "author",\n        Value = "aspose",\n        BuiltIn = "false",\n        Link = new Link {\n            Href = "https://example.com",\n            Rel = "self",\n            Title = "Author link",\n            Type = "text/html"\n        }\n    },\n    folder: "Docs",\n    storageName: "MyStorage"\n);\nvar response = apiInstance.PutDocumentProperty(request);\nConsole.WriteLine(response.Status);\n```\n</details> |
| **Java** | <details><summary>Java の例を表示</summary>```java\nimport com.aspose.cells.cloud.api.DocumentPropertiesApi;\nimport com.aspose.cells.cloud.model.*;\n\nDocumentPropertiesApi api = new DocumentPropertiesApi();\nCellsDocumentProperty prop = new CellsDocumentProperty();\nprop.setName("author");\nprop.setValue("aspose");\nprop.setBuiltIn("false");\nLink link = new Link();\nlink.setHref("https://example.com");\nlink.setRel("self");\nlink.setTitle("Author link");\nlink.setType("text/html");\nprop.setLink(link);\n\nPutDocumentPropertyRequest request = new PutDocumentPropertyRequest("test.xlsx", "author", prop, "Docs", "MyStorage");\nCellsCloudResponse response = api.putDocumentProperty(request);\nSystem.out.println(response.getStatus());\n```\n</details> |
| **Python** | <details><summary>Python の例を表示</summary>```python\nfrom asposecellscloud import DocumentPropertiesApi, CellsDocumentProperty, Link\n\napi = DocumentPropertiesApi()\nprop = CellsDocumentProperty(name="author", value="aspose", built_in="false")\nprop.link = Link(href="https://example.com", rel="self", title="Author link", type="text/html")\nresponse = api.put_document_property(name="test.xlsx", property_name="author", property=prop, folder="Docs", storage_name="MyStorage")\nprint(response.status)\n```\n</details> |
| **Node.js** | <details><summary>Node.js の例を表示</summary>```javascript\nconst { DocumentPropertiesApi, CellsDocumentProperty, Link } = require('asposecellscloud');\n\nconst api = new DocumentPropertiesApi();\nconst prop = new CellsDocumentProperty({\n  name: 'author',\n  value: 'aspose',\n  builtIn: 'false',\n  link: new Link({ href: 'https://example.com', rel: 'self', title: 'Author link', type: 'text/html' })\n});\n\napi.putDocumentProperty({\n  name: 'test.xlsx',\n  propertyName: 'author',\n  property: prop,\n  folder: 'Docs',\n  storageName: 'MyStorage'\n}).then(res => console.log(res.status));\n```\n</details> |
| **Go** | <details><summary>Go の例を表示</summary>```go\nimport (\n    "context"\n    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\napi := cells.NewDocumentPropertiesApi()\nprop := cells.CellsDocumentProperty{Name: "author", Value: "aspose", BuiltIn: "false"}\nprop.Link = &cells.Link{Href: "https://example.com", Rel: "self", Title: "Author link", Type: "text/html"}\nreq := cells.PutDocumentPropertyRequest{Name: "test.xlsx", PropertyName: "author", Property: &prop, Folder: "Docs", StorageName: "MyStorage"}\nresp, _, err := api.PutDocumentProperty(context.Background(), req)\nif err != nil { panic(err) }\nfmt.Println(resp.Status)\n```\n</details> |
| **Ruby** | <details><summary>Ruby の例を表示</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::DocumentPropertiesApi.new\nprop = AsposeCellsCloud::CellsDocumentProperty.new(\n  name: 'author',\n  value: 'aspose',\n  built_in: 'false',\n  link: AsposeCellsCloud::Link.new(\n    href: 'https://example.com',\n    rel: 'self',\n    title: 'Author link',\n    type: 'text/html'\n  )\n)\nresponse = api.put_document_property('test.xlsx', 'author', prop, folder: 'Docs', storage_name: 'MyStorage')\nputs response.status\n```\n</details> |
| **PHP** | <details><summary>PHP の例を表示</summary>```php\n<?php\nuse Aspose\Cells\DocumentPropertiesApi;\nuse Aspose\Cells\Model\CellsDocumentProperty;\nuse Aspose\Cells\Model\Link;\n\n$api = new DocumentPropertiesApi();\n$prop = new CellsDocumentProperty([\n    'Name' => 'author',\n    'Value' => 'aspose',\n    'BuiltIn' => 'false',\n    'Link' => new Link([\n        'Href' => 'https://example.com',\n        'Rel' => 'self',\n        'Title' => 'Author link',\n        'Type' => 'text/html'\n    ])\n]);\n$response = $api->putDocumentProperty('test.xlsx', 'author', $prop, 'Docs', 'MyStorage');\necho $response->getStatus();\n?>\n```\n</details> |
| **Perl** | <details><summary>Perl の例を表示</summary>```perl\nuse AsposeCellsCloud::DocumentPropertiesApi;\nuse AsposeCellsCloud::Object::CellsDocumentProperty;\nuse AsposeCellsCloud::Object::Link;\n\nmy $api = AsposeCellsCloud::DocumentPropertiesApi->new();\nmy $prop = AsposeCellsCloud::Object::CellsDocumentProperty->new(\n    Name    => 'author',\n    Value   => 'aspose',\n    BuiltIn => 'false',\n    Link    => AsposeCellsCloud::Object::Link->new(\n        Href  => 'https://example.com',\n        Rel   => 'self',\n        Title => 'Author link',\n        Type  => 'text/html'\n    )\n);\nmy $response = $api->put_document_property(name => 'test.xlsx', property_name => 'author', property => $prop, folder => 'Docs', storage_name => 'MyStorage');\nprint $response->{Status}, \"\\n\";\n```\n</details> |

---

## 関連リンク
- **OpenAPI スペック**: <https://apireference.aspose.cloud/cells/#/Properties/PutDocumentProperty>（新しいタブで開く、`rel="noopener noreferrer"`）。  
- **認証ガイド**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>（新しいタブで開く、`rel="noopener noreferrer"`）。  
- **Aspose.Cells Cloud SDK**: <https://github.com/aspose-cells-cloud>（新しいタブで開く、`rel="noopener noreferrer"`）。

---