---
title: "範囲内の列幅を変更する"
ArticleTitle: "範囲内の列幅を変更する – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "Column width"
type: docs
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells, 列幅, REST API, Excel, SDK, 範囲, クラウド"
description: "Aspose.Cells Cloud REST API または SDK（C#、Java、Python など）を使用して範囲内の列幅を変更する方法について学びます。cURL、リクエスト/レスポンスの詳細、認証手順を含みます。"
weight: 74
---

この REST API は、範囲の列幅を設定します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**前提条件** – エンドポイントを呼び出す前に、以下の手順を実行してください：

1. Aspose Cloud アカウントを作成し、*クライアント ID* および *クライアント シークレット* を取得します。  
2. OAuth エンドポイント（`/connect/token`）を呼び出して JWT トークンをリクエストします。トークンは `access_token` フィールドで返されます。  
3. 対象のワークブックを Aspose Cloud ストレージにアップロードするか（または、既に指定されたフォルダ内に存在することを確認してください）。

リクエスト パラメータは以下の通りです：

| パラメータ名 | 型     | 位置   | 説明                     |
|--------------|--------|--------|---------------------------|
| name         | 文字列 | パス   | ワークブック ファイルの名前 |
| sheetName    | 文字列 | パス   | シート名                   |
| value        | 数値   | クエリ | 設定する列幅の値           |
| range        | オブジェクト | ボディ | 対象セルを定義する範囲オブジェクト |
| folder       | 文字列 | クエリ | ワークブックが格納されているフォルダのパス |
| storageName  | 文字列 | クエリ | ストレージ サービスの名前 |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth)はパブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドライン ツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

<h3 id="request">リクエスト</h3>

```bash
# ワークブック *test.xlsx* のシート *Sheet1* の列幅を 20 ポイントに設定するエンドポイントを呼び出します。
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">レスポンス</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*考えられるエラー レスポンス*

| HTTP コード | 説明                         |
|-------------|------------------------------|
| 400         | Bad Request – 無効な JSON またはパラメータ |
| 401         | Unauthorized – トークンが不足または無効      |
| 404         | Not Found – ワークブックまたはシートが存在しない |

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー
SDK を使用すると、開発を最速で加速できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q:** *Excel ワークブックの範囲の列幅を設定するために呼び出すエンドポイントはどこですか？*  
**A:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth` ここで `{name}` はワークブック ファイル名、`{sheetName}` は対象シート名です。

**Q:** *列幅 API を使用する際、リクエストの認証はどのように行いますか？*  
**A:** `Authorization: Bearer <jwt token>` ヘッダーを含めます。JWT トークンは、クライアント ID とクライアント シークレットを使用して Aspose Cloud の OAuth フロー（`/connect/token`）を介して取得してください。

**Q:** *列 A～C の幅を 25 ポイントに変更する場合、送信する JSON ボディはどのようになりますか？*  
**A:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

リクエスト URL にクエリパラメータ `value=25` を追加してください。