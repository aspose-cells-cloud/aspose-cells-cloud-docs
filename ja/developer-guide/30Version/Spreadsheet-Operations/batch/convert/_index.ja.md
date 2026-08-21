---
title: "Excel ファイルの一括変換"
second_title: "ドキュメント"
type: docs
url: /ja/batch/convert
keywords: "一括変換, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, スプレッドシート"
description: "Aspose.Cells Cloud API を使用して、複数の Excel ファイルを PDF、CSV、JSON、Markdown などの形式に一括で変換する方法を学びます。このガイドには、REST エンドポイントの詳細、リクエストパラメータ、cURL の例、および various 言語向けの SDK コードスニペットが含まれています。"
weight: 100
---

この REST API は、対象となるファイルの**一括変換**を可能にします。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名       | 型     | 位置   | 説明                                           |
|------------------|--------|--------|------------------------------------------------|
| **batchConvertRequest** | オブジェクト | 本体   | 変換設定を含むリクエスト本体。                 |

#### BatchConvertRequest プロパティ

| 名前               | 型                    | 説明                                           | 備考 |
|--------------------|-----------------------|------------------------------------------------|------|
| **SourceFolder**   | 文字列                | 変換元の Excel ファイルが格納されているフォルダのパス。 | [省略可能] |
| **MatchCondition** | MatchConditionRequest | 変換対象ファイルを選択するために使用される条件。      | [省略可能] |
| **Format**         | 文字列                | 変換後の形式（例: `pdf`, `csv`）。               | [省略可能] |
| **OutFolder**      | 文字列                | 変換後のファイルが保存される宛先フォルダ。         | [省略可能] |
| **SaveOptions**    | SaveOptions           | ファイルの保存方法を制御する追加オプション。       | [省略可能] |

#### MatchConditionRequest プロパティ

| 名前                   | 型         | 説明                                          | 備考 |
|------------------------|------------|-----------------------------------------------|------|
| **RegexPattern**       | 文字列     | ファイル名をフィルタリングするために使用する正規表現。 | [省略可能] |
| **FullMatchConditions** | 文字列配列 | 完全一致させるファイル名の条件リスト。         | [省略可能] |


### リクエストボディパラメータ

| パラメータ名 | 型   | 説明                                    |
|------------|------|-----------------------------------------|
| data       | ファイル | 作成するワークブックファイルのバイナリコンテンツ。 |

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

**HTTP ステータスコード**

| コード | 意味                         | 返却タイミング                           |
|--------|------------------------------|------------------------------------------|
| 200 OK | ワークブックが正常に作成されました | 通常の処理フロー                         |
| 201 Created | ワークブックが作成されました（代替応答） | API が作成済みステータスを返す場合       |
| 400 Bad Request | 無効なパラメータ             | クライアント側エラー                      |
| 401 Unauthorized | トークンが不足しているか無効です | 認証エラー                                |
| 409 Conflict | ファイルが既に存在し、`isWriteOver=false` | 既存ファイルとの競合                      |

## SDK を使用した PostBatchConvert API の利用方法

### PostBatchConvert API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/PostBatchConvert)は、パブリックに利用可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスに呼び出しを行う方法を示しています。

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}