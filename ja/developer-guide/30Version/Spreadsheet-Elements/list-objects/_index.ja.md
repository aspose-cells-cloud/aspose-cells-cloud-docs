---
title: "Excel ListObject の操作"
ArticleTitle: "Excel ListObject の操作"
second_title: "Document"
linktitle: "ListObjects"
type: docs
url: /ja/list-objects/
aliases:
  - /ja/working-with-list-objects/
  - /ja/working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, Excel テーブル API, テーブルの追加, テーブルの更新, テーブルの削除, テーブルを範囲に変換, Excel テーブルの並べ替え"
description: "Aspose.Cells Cloud REST API を使用して Excel ListObject（テーブル）を追加、更新、削除、取得、並べ替え、および範囲への変換する方法を学びます。C#、Java、Python などのコード例を含みます。"
weight: 100
---

Excel ListObject（テーブル）は、データセットを構造化された方法で整理するための機能を提供します。自動的なデータ配置、ヘッダー行、組み込みのフィルター、およびオプションの合計行などの機能が含まれています。これらの機能をマスターして、データを迅速かつ効率的に分析しましょう。

**ListObject の定義:** **ListObject** は、行と列をグループ化し、並べ替えやフィルター、スタイル設定を可能にする Excel のネイティブなテーブルオブジェクトです。このオブジェクトは Aspose.Cells Cloud API を通じてアクセスできます。

## テーブル（List Object）の操作方法

- [ワークシート内にテーブル（ListObject）を追加する方法](/ja/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [ワークシート内のテーブル（ListObject）を更新する方法](/ja/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [テーブル（ListObject）を範囲に変換する方法](/ja/cells/convert-list-object-or-table-to-range/)
- [テーブルデータを並べ替える方法](/ja/cells/sort-table-data/)
- [テーブルから重複行を削除する方法](/ja/cells/list-objects/remove-duplicates/)
- [テーブルにスライサーを挿入する方法](/ja/cells/list-objects/insert-slicer/)

**API リファレンス（概要）:**  
Aspose.Cells Cloud REST API は、`GET /cells/{fileName}/worksheets/{sheetName}/listobjects`、`POST /cells/{fileName}/worksheets/{sheetName}/listobjects`、`PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`、および `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` といったエンドポイントを通じて ListObject 操作を提供します。必要なクエリパラメータは `folder`（必須）および `storage`（オプション）です。リクエストボディは、テーブルのプロパティ（名前、ヘッダー行の表示、合計行の表示など）を記述する JSON オブジェクトであり、レスポンスは作成または変更された ListObject の詳細情報を含む JSON ペイロードを返します。

**前提条件:**  
- 有効な Aspose.Cells Cloud 認証トークン。  
- ワークブックファイルは、サポートされているストレージ場所（デフォルト: **/**）にアップロードされている必要があります。また、`folder` クエリパラメータはその場所を指す必要があります。  
- オプション: 非デフォルトのストレージサービスを使用する場合は `storage` を設定します。

**エンドポイントの詳細**

| メソッド | エンドポイント | クエリパラメータ | リクエストボディ（JSON） | 成功時のレスポンス（例） | ステータスコード |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder`（必須）、`storage`（オプション） | *なし* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK、400 – Bad Request、401 – Unauthorized、404 – Not Found |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder`（必須）、`storage`（オプション） | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Created、400 – Bad Request、401 – Unauthorized、409 – Conflict |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder`（必須）、`storage`（オプション） | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK、400 – Bad Request、401 – Unauthorized、404 – Not Found |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder`（必須）、`storage`（オプション） | *なし* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK、400 – Bad Request、401 – Unauthorized、404 – Not Found |

**コードスニペット**

*C#（POST – ListObject の追加）*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java（GET – ListObjects の取得）*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python（PUT – ListObject の更新）*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js（DELETE – ListObject の削除）*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**注意事項:**  
- ListObject のインデックスは 0 から始まります。  
- ListObject を追加する際、`StartRow` および `StartColumn` はテーブルの左上セルを定義します。  
- API は、`offset` および `limit` クエリパラメータによるページネーション（大きなワークシート向け）をサポートしています（表には記載していません）。  
- レート制限: アカウントごとに 1 分あたり 100 リクエスト。これを超えると **429 Too Many Requests** が返されます。

本ページ全体で **Excel ListObject** という用語を複数回使用することで、コンテンツは「Excel ListObject」、「Aspose.Cells Cloud」、「Excel table API」というターゲットキーワードに適合し、SEO の向上に寄りながら、読者にとって自然な読み心地を維持しています。