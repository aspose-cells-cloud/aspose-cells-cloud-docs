---
title: "セルの値を設定 – Aspose.Cells Cloud API リファレンス (v3.0)"
type: docs
url: /ja/set-value-of-a-cell-in-a-worksheet/
weight: 70
keywords: "Aspose Cells API セルの値設定、Excel セル更新 REST、Aspose.Cells Cloud cURL 例"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークシート内の特定のセルの値を設定する方法を学習します。リクエスト構文、パラメータ、HTTPS cURL の例、および SDK のコードサンプルを含みます。  "
---

この REST API は、Excel ファイル内の**セルの値**を設定します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を要求します。

**リクエストパラメータ**

| 名前        | 型     | 位置   | 説明                                                 |
| ----------- | ------ | ------ | ---------------------------------------------------- |
| name        | 文字列 | パス   | Excel ドキュメントの名前（拡張子を含む）。           |
| sheetName   | 文字列 | パス   | ワークシートの名前（大文字・小文字を区別）。         |
| cellName    | 文字列 | パス   | 対象セルの A1 形式のアドレス（例: `A1`）。           |
| value       | 文字列 | クエリ | セルに設定する値。                                   |
| type        | 文字列 | クエリ | 値のデータ型（`int`、`string`、`float` など）。      |
| formula     | 文字列 | クエリ | セルに適用する数式（オプション）。                   |
| folder      | 文字列 | クエリ | ドキュメントが配置されているフォルダ（オプション）。 |
| storageName | 文字列 | クエリ | ファイルが存在するストレージの名前（オプション）。   |

## **レスポンス**

CellResponse を返します。

- **レスポンスフィールド概要**

| フィールド      | 型           | 説明                                               |
| --------------- | ------------ | -------------------------------------------------- |
| `Name`          | 文字列       | セルのアドレス（例: `F341`）。                     |
| `Row`           | 整数         | 0 から始まる行インデックス。                       |
| `Column`        | 整数         | 0 から始まる列インデックス。                       |
| `Value`         | 文字列       | セルに表示される値。                               |
| `Type`          | 文字列       | セルのデータ型（例: `IsString`）。                 |
| `Formula`       | 文字列       | セルに数式が含まれている場合の数式テキスト。       |
| `IsFormula`     | 真偽値       | セルに数式が含まれているかどうかを示します。       |
| `IsMerged`      | 真偽値       | セルが結合範囲の一部かどうかを示します。           |
| `IsArrayHeader` | 真偽値       | セルが配列のヘッダーかどうかを示します。           |
| `IsInArray`     | 真偽値       | セルが配列に属しているかどうかを示します。         |
| `IsErrorValue`  | 真偽値       | セルにエラー値が含まれているかどうかを示します。   |
| `IsInTable`     | 真偽値       | セルがテーブル内にあるかどうかを示します。         |
| `IsStyleSet`    | 真偽値       | セルにスタイルが適用されているかどうかを示します。 |
| `HtmlString`    | 文字列       | セルの値の HTML エンコードされた表現。             |
| `Style.link`    | オブジェクト | スタイルリソースへのハイパーリンク。               |

```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                                                           |
| ------ | ------------------------ | ------------------------------------------------------------------------------ |
| 200    | OK                       | フィルタが正常に適用された。レスポンスには操作の詳細が含まれます。             |
| 400    | 不正リクエスト           | パラメータが不足している、または無効（例: サポートされていないファイル形式）。 |
| 401    | 認証エラー               | JWT トークンが無効または不足している。                                         |
| 413    | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。                         |
| 500    | 内部サーバーエラー       | 予期しないサーバーエラーが発生しました。                                       |

## SDK を使用して PostWorksheetCellSetValue API を利用する方法

### PostWorksheetCellSetValue API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue)は、開発者がブラウザや任意の HTTP クライアントから直接 REST エンドポイントを呼び出せる、パブリックにアクセス可能なプログラミングインタフェースを定義しています。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスを呼び出すことができます。以下の例は、cURL を使用してセルの値を設定する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細な処理が自動的に管理されるため、開発速度が向上し、プロジェクトに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}