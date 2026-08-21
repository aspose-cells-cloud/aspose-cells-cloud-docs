---
title: "Excel の ListObject にスライサーを挿入する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "スライサーの挿入"
type: docs
keywords: "Aspose.Cells, Excel スライサー, ListObject, REST API, クラウド SDK"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して、Excel の ListObject にスライサーを追加する方法を学びます。エンドポイント、パラメータ、認証、cURL リクエストのサンプル、およびレスポンス JSON を含みます。"
weight: 20
ArticleTitle: "Excel の ListObject にスライサーを挿入する – Aspose.Cells Cloud API"
---

この REST API は、Excel ワークシート上のリスト オブジェクトにスライサーを挿入します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### リクエスト パラメータ

| パラメータ名        | タイプ    | 位置   | 説明                                                                 |
| ------------------- | --------- | ------ | -------------------------------------------------------------------- |
| name                | 文字列    | パス   | Excel ファイルの名前。                                               |
| sheetName           | 文字列    | パス   | リスト オブジェクトを含むワークシートの名前。                        |
| listObjectIndex     | 整数      | パス   | スライサーを追加するリスト オブジェクトの 0 から始まるインデックス。  |
| columnIndex         | 整数      | クエリ | スライサーの基になる列の 0 から始まるインデックス。                   |
| destCellName        | 文字列    | クエリ | スライサーを配置するセル参照（例：**A1**）。                         |
| folder              | 文字列    | クエリ | Excel ファイルを含むストレージ内のフォルダ。                         |
| storageName         | 文字列    | クエリ | Aspose Cloud ストレージ サービスの名前。                             |

cURL コマンドライン ツールを使用して API を呼び出すことができます。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注:** このリクエストには、Aspose Cloud 認証サービスから取得した有効な JWT ベアラートークンが必要です。このエンドポイントはリクエスト ボディを必要としません。ただし、クライアント ライブラリがペイロードを必須とする場合は、空の JSON オブジェクト `{}` を送信してください。

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **レスポンス ヘッダー:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**HTTP ステータス コード**

| コード | 意味           | 説明                                                         |
| ------ | -------------- | ------------------------------------------------------------ |
| 200  | OK             | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request    | パラメータが不足しているか、無効である（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized   | 無効または不足している JWT トークン。                          |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えた。               |
| 500  | Internal Server Error | 予期しないサーバーエラーが発生した。                           |

### エラー処理

エラーが発生した場合、API は `ErrorMessage` フィールドを含む JSON オブジェクトを返し、問題の内容を説明します。HTTP ステータス コードと `ErrorMessage` を確認し、修正アクションを決定してください。

## クラウド SDK ファミリー

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、GitHub リポジトリをご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}