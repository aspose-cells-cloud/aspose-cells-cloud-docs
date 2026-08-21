---
title: "Excelワークシートの追加"
ArticleTitle: "Excelワークシートの追加 - Aspose.Cells Cloud API ガイド"
second_title: "ドキュメント"
linktype: "追加"
type: docs
url: /worksheets/add/
aliases: [/add-a-new-excel-worksheet/]
keywords: "Excelワークシートの追加, Aspose.Cells Cloud, REST API, PUTワークシート, Excelワークブック, APIリクエスト"
description: "Aspose.Cells Cloud REST API を使用してExcelワークブックに新しいワークシートを追加する手順ガイド。リクエストの詳細、cURLの例、および複数の言語向けのSDKコードスニペットを含みます。"
weight: 20
---

このREST APIは、既存のワークブックに新しいワークシートを追加します。

**前提条件**: このエンドポイントを呼び出すには、有効なAspose Cloud認証トークンが必要です。また、対象のワークブックはAspose Cloudストレージにアップロード済みであり、ストレージ名（カスタムストレージを使用する場合）を把握している必要があります。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **リクエストパラメータ**

| パラメータ名 | 型      | 位置   | 説明                                      |
| ------------ | ------- | ------ | ----------------------------------------- |
| name         | 文字列  | パス   | ワークブックファイルの名前。              |
| sheetName    | 文字列  | パス   | 作成する新しいワークシートの名前。        |
| position     | 整数    | クエリ | シートを挿入する0から始まる位置。         |
| sheettype    | 文字列  | クエリ | 新しいシートのタイプ（例: **Chart**, **Dialog**）。 |
| folder       | 文字列  | クエリ | ワークブックを含むフォルダ。              |
| storageName  | 文字列  | クエリ | Aspose Cloudストレージの名前。            |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**考えられるレスポンスステータスコード**

| ステータスコード | 説明                                         |
|----------------|----------------------------------------------|
| 200            | ワークシートの追加に成功しました。           |
| 400            | 不正なリクエスト – 無効なパラメータです。    |
| 401            | 認証エラー – 認証トークンが不足または無効です。 |
| 404            | 見つかりません – ワークブックまたはフォルダが存在しません。 |
| 500            | サーバー内部エラー – 予期しない状況です。     |

## Cloud SDKファミリー

SDKを使用するのが開発を進める最速の方法です。SDKは低レベルの詳細を抽象化し、プロジェクトに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}