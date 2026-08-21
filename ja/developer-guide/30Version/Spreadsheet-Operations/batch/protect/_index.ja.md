---
title: "Excel ファイルを一括で保護する"
second_title: "ドキュメント"
type: docs
url: /batch/protect
keywords: "Excel ファイルを一括で保護, Aspose Cells Cloud, REST API, Excel 保護, 一括保護"
description: "Aspose.Cells Cloud REST API を使って複数の Excel ファイルを一括で保護する方法を学びます。リクエストの詳細、cURL の例、および various 言語向けの SDK コードサンプルを含みます。"
weight: 100
---

この REST API は、対応する Excel ファイルの**一括保護**を可能にします。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名            | 型                    | 位置   | 説明                                                                                                     |
|-------------------------|-----------------------|--------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest     | BatchProtectRequest   | body   | ソースフォルダ、マッチ条件、保護タイプ、パスワード、出力フォルダを指定する JSON ペイロード。              |

### BatchProtectRequest プロパティ

| 名前              | 型                       | 説明                                                                                     | 備考       |
|-------------------|--------------------------|------------------------------------------------------------------------------------------|------------|
| SourceFolder      | string                   | ソース Excel ファイルを含むフォルダ。                                                    | オプション |
| MatchCondition    | MatchConditionRequest   | 保護対象のファイルを選択するための条件。                                                 | オプション |
| ProtectionType    | string                   | 適用する保護のタイプ（例: `All`, `ReadOnly`）。                                          | オプション |
| Password          | string                   | 保護されたファイルに設定するパスワード。                                                 | オプション |
| OutFolder         | string                   | 保護されたファイルの出力先フォルダ。                                                     | オプション |

### MatchConditionRequest プロパティ

| 名前                | 型         | 説明                                     | 備考       |
|---------------------|------------|------------------------------------------|------------|
| RegexPattern        | string     | ファイル名にマッチさせる正規表現。      | オプション |
| FullMatchConditions | string[]   | 完全一致するファイル名の条件リスト。     | オプション |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明                              |
|--------------|------|-----------------------------------|
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

| コード | 意味                        | 返却タイミング                         |
|--------|-----------------------------|----------------------------------------|
| 200 OK | ワークブックが正常に作成された | 通常の処理フロー時                     |
| 201 Created | ワークブックが作成された（代替レスポンス） | API が作成ステータスを返す場合 |
| 400 Bad Request | 無効なパラメータ | クライアント側エラー                   |
| 401 Unauthorized | トークンが不足している、または無効 | 認証エラー                     |
| 409 Conflict | ファイルが存在し、`isWriteOver=false` | 既存ファイルとの競合             |

## SDK を使用した PostProtectConvert API の利用方法

### PostProtectConvert API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/PostProtectConvert) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細な処理を担当し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}