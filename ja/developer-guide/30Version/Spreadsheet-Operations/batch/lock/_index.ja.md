---
title: "Excel ファイルをバッチ処理でロックする"
second_title: "ドキュメント"
type: docs
url: /batch/lock
keywords: "バッチロック, Excel, Aspose.Cells, Cloud API, スプレッドシート, ファイル保護"
description: "Aspose.Cells Cloud API により、複数の Excel ファイルを一括でロックできます。REST エンドポイントまたはサポートされている SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go など）のいずれかを使用して、ファイルを一括でロックします。"
weight: 100
---

この REST API は、対象となる Excel ファイルの**バッチロック**を実行できます。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名         | 型                 | 位置   | 説明                           |
|----------------------|--------------------|--------|--------------------------------|
| BatchLockRequest     | BatchLockRequest   | body   | ロックパラメータを含む JSON 本体。 |

#### **BatchLockRequest** のプロパティ

| 名前             | 型                       | 説明                                      | 備考       |
|------------------|--------------------------|-------------------------------------------|------------|
| SourceFolder     | string                   | ソース Excel ファイルを含むフォルダ。     | オプション |
| MatchCondition   | MatchConditionRequest    | ロック対象ファイルを選択するための条件。  | オプション |
| Password         | string                   | ロックされたファイルに適用するパスワード。| オプション |
| OutFolder        | string                   | ロックされたファイルの出力先フォルダ。    | オプション |

#### **MatchConditionRequest** のプロパティ

| 名前               | 型        | 説明                                 | 備考       |
|--------------------|-----------|--------------------------------------|------------|
| RegexPattern       | string    | ファイル名にマッチする正規表現パターン。| オプション |
| FullMatchConditions| string[]  | ロック対象の完全一致ファイル名。       | オプション |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明                               |
|--------------|------|------------------------------------|
| data         | file | 作成するワークブックファイルのバイナリ内容。 |

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

| コード | 意味                         | 返されるタイミング                         |
|--------|------------------------------|--------------------------------------------|
| 200 OK | ワークブックが正常に作成された | 通常のフロー                               |
| 201 Created | ワークブックが作成された（代替レスポンス） | API が「作成済み」ステータスを返す場合 |
| 400 Bad Request | 無効なパラメータ | クライアント側エラー                       |
| 401 Unauthorized | トークンが不足または無効 | 認証エラー                                 |
| 409 Conflict | ファイルが存在し、`isWriteOver=false` | 既存ファイルとの競合                       |

## SDK を使用した PostBatchLock API の使用方法

### PostBatchLock API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用することで、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

SDK を使用すると、開発が最も速く行えます。SDK は低レベルの詳細を抽象化するため、ロックタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}