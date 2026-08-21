---
title: "ピボットテーブルにピボットフィールドを追加する"
second_title: "Document"
linktitle: "ピボットフィールドの追加"
type: docs
url: /pivot-tables/add-pivot-field/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, ピボットテーブル, ピボットフィールドの追加, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して、既存のピボットテーブルにピボットフィールドを追加します。リクエストの詳細、cURL の例、SDK スニペットを含みます。"
weight: 40
ArticleTitle: "ピボットテーブルにピボットフィールドを追加する – Aspose.Cells Cloud ドキュメント"
---

この REST API は、既存のピボットテーブルに**ピボットフィールドを追加**します。

> **前提条件:** このエンドポイントを呼び出すには、`Authorization` ヘッダーに有効な JWT 認証トークンを含め、ワークブックが指定されたフォルダまたはデフォルトストレージに保存されていることを確認する必要があります。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### リクエストパラメータ

| パラメータ名        | 型       | 位置  | 説明                                                      |
| ------------------- | -------- | ----- | --------------------------------------------------------- |
| name                | string   | path  | ドキュメント名。                                          |
| sheetName           | string   | path  | シート名。                                                |
| pivotTableIndex     | integer  | path  | ピボットテーブルのインデックス。                          |
| pivotFieldType      | string   | query | フィールドエリアのタイプ（例: Row, Column）。             |
| request             | object   | body  | 追加するフィールドのインデックスを含む DTO。               |
| needReCalculate     | boolean  | query | 操作後にピボットテーブルを再計算する場合は **true** に設定。 |
| folder              | string   | query | ドキュメントが保存されているフォルダ。                    |
| storageName         | string   | query | ストレージ名。                                            |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST によるやり取りを可能にします。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスを呼び出すことができます。以下の例では、cURL を使用してピボットフィールドを追加する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

成功したレスポンスは `Code` および `Status` フィールドを含む JSON オブジェクトを返します。スキーマ例:

```json
{
  "Code": 0,        // HTTP ステータスコードを示す整数
  "Status": "OK"    // 文字列メッセージ
}
```

考えられるエラーレスポンスには、パラメータ不足の場合の **400 Bad Request**、トークンが無効な場合の **401 Unauthorized**、サーバー側の問題に対する **500 Internal Server Error** が含まれます。

## Cloud SDK Family

SDK を使用すると、この機能を統合する最も速い方法です。SDK は低レベルの詳細を処理し、ビジネスロジックの集中を可能にします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目:**  
- [ピボットテーブルの追加](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)  
- [ピボットフィールドの削除](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)