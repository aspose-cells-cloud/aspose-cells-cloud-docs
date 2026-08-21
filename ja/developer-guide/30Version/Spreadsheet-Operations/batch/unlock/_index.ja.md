---
title: "バッチアンロック"
second: "ドキュメント"
type: docs
url: /batch/unlock
keywords: "バッチアンロック、Aspose.Cells Cloud、Excel、REST API、スプレッドシート、クラウドSDK"
description: "Aspose.Cells Cloud REST API を使用して複数の Excel ファイルをバッチでアンロックします。C#、Java、Python など複数の言語向けの SDK をサポートしています。"
weight: 100
---

この REST API は、対象となる Excel ファイルをバッチでアンロックします。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名 | 型 | 位置 | 説明 |
|----------------|------|----------|-------------|
| **BatchLockRequest** |  | body | アンロック設定を含むリクエストボディ。 |

### **BatchLockRequest** プロパティ

| 名前          | 型                     | 説明                                 | 備考 |
|---------------|--------------------------|---------------------------------------------|-------|
| SourceFolder  | string                   | ソース Excel ファイルを含むフォルダ。| [オプション] |
| MatchCondition| MatchConditionRequest    | アンロック対象ファイルを選択するための条件。| [オプション] |
| Password      | string                   | パスワードで保護されたワークブックに適用されるパスワード。   | [オプション] |
| OutFolder     | string                   | アンロックされたファイルの出力先フォルダ。 | [オプション] |

### **MatchConditionRequest** プロパティ

| 名前               | 型      | 説明                                 | 備考 |
|--------------------|-----------|---------------------------------------------|-------|
| RegexPattern       | string    | ファイル名に一致させる正規表現。    | [オプション] |
| FullMatchConditions| string[]  | 完全一致させるファイル名の条件。       | [オプション] |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | 作成するワークブックファイルのバイナリコンテンツ。 |
  
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

| コード | 意味                     | 返されるタイミング                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | ワークブックが正常に作成されました | 通常の処理フロー |
| 201 Created | ワークブックが作成されました（代替レスポンス） | API が作成済みステータスを返す場合 |
| 400 Bad Request | 無効なパラメータ | クライアント側エラー |
| 401 Unauthorized | トークンが不足している、または無効です | 認証エラー |
| 409 Conflict | ファイルが存在し、`isWriteOver=false` です | 既存のファイルとの競合 |

## SDK を使用した PostBatchLock API の利用方法

### PostBatchLock API 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクションを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、アンロック機能の開発を最速で行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}