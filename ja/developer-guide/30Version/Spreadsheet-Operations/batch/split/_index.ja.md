---
title: "バッチ分割"
second: "ドキュメント"
type: docs
url: /ja/batch/split
keywords: "バッチ分割、Aspose.Cells Cloud、REST API、Excel、PDF、CSV、JSON、スプレッドシート、クラウドSDK"
description: "スプレッドシートファイルをPDF、CSV、JSONなどの複数のフォーマットに分割するAspose.Cells Cloudのバッチ分割APIに関するドキュメント。リクエストの詳細、cURLコマンドの例、さまざまなプログラミング言語でのSDKの使用方法を含みます。"
weight: 100
---

このREST APIは、対象となるファイルの**バッチ分割**を実行します。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名       | 型                 | パス／クエリ／文字列／HTTPボディ | 説明                                     |
|------------------|--------------------|----------------------------|-----------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                       | 分割オプションを含むリクエストペイロード |

### **BatchSplitRequest** プロパティ

| 名前            | 型                  | 説明                                     | 備考       |
|----------------|---------------------|-----------------------------------------|------------|
| SourceFolder   | string              | ソースファイルを含むフォルダ             | [オプション] |
| SourceStorage  | string              | ソースファイルが存在するストレージ名     | [オプション] |
| MatchCondition | MatchConditionRequest| 分割対象ファイルを選択するために使用する条件 | [オプション] |
| Format         | string              | 出力フォーマット（例：pdf、csv）         | [オプション] |
| FromIndex      | integer             | 分割するページの開始インデックス         | [オプション] |
| ToIndex        | integer             | 分割するページの終了インデックス         | [オプション] |
| OutFolder      | string              | 分割されたファイルの保存先フォルダ       | [オプション] |
| SaveOptions    | SaveOptions         | 出力保存の追加オプション                 | [オプション] |

### **MatchConditionRequest** プロパティ

| 名前                | 型        | 説明                                     | 備考       |
|---------------------|-----------|-----------------------------------------|------------|
| RegexPattern        | string    | ファイル名にマッチする正規表現           | [オプション] |
| FullMatchConditions| string[]  | 完全一致条件のリスト                     | [オプション] |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明                               |
|------------|------|-----------------------------------|
| data       | file | 作成するワークブックファイルのバイナリコンテンツ |

### **レスポンス**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTPステータスコード**

| コード | 意味                   | 発生タイミング                     |
|--------|------------------------|----------------------------------|
| 200 OK | ワークブックが正常に作成されました | 通常の処理フロー                   |
| 201 Created | ワークブックが作成されました（代替レスポンス） | APIがCreatedステータスを返す場合 |
| 400 Bad Request | 無効なパラメータ           | クライアント側エラー               |
| 401 Unauthorized | トークンが不足または無効      | 認証エラー                         |
| 409 Conflict | ファイルが存在し、`isWriteOver=false` | 既存ファイルとの競合               |


## SDKを使用したPostBatchSplit APIの利用方法

### PostBatchSplit API仕様

[OpenAPI仕様](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit)はパブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLを使用してクラウドAPIにアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKの使用

SDKを使用することは、開発を高速化する最良の方法です。SDKが低レベルの詳細を処理し、分割タスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスにアクセスする方法を示しています：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}