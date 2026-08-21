---
title: "空の Excel ワークブックを作成する"
second_title: "ドキュメント"
linktitle: "空のワークブック"
type: docs
url: /ja/create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, 空のワークブック, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して空の Excel ワークブックを作成する方法を学びます。cURL および SDK のサンプルを含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使用して空の Excel ワークブックを作成する"
---

この REST API は、**空のワークブック**を作成します。

## PutWorkbookCreate API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### クエリパラメータ

| パラメータ名 | 型     | 説明                                                |
| ------------ | ------ | --------------------------------------------------- |
| templateFile | string | ベースとして使用するテンプレートワークブックのパス（任意） |
| dataFile     | string | ワークブックを埋めるためのデータファイルのパス（任意）   |
| isWriteOver  | boolean | `true` の場合は既存のファイルを上書き、`false` の場合は上書きしない |
| folder       | string | 作成されたワークブックの保存先フォルダ（任意）         |
| storageName  | string | 使用するストレージサービスの名前。                     |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明                             |
| ------------ | ---- | -------------------------------- |
| data         | file | 作成するワークブックファイルのバイナリコンテンツ |

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

| コード | 意味                          | 返される状況                         |
|------|-------------------------------|--------------------------------------|
| 200 OK | ワークブックが正常に作成されました | 通常の処理フロー                    |
| 201 Created | ワークブックが作成されました（代替レスポンス） | API が作成済みステータスを返した場合 |
| 400 Bad Request | 無効なパラメータ              | クライアント側エラー                |
| 401 Unauthorized | トークンが不足している、または無効です | 認証エラー                         |
| 409 Conflict | ファイルが存在し、`isWriteOver=false` | 既存ファイルとの競合                |

## SDK を使用した PutWorkbookCreate API の利用方法

### PutWorkbookCreate API の仕様

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスにアクセスできます。`Authorization` ヘッダーに有効な OAuth2/JWT アクセストークンを含めてください。空のワークブックを作成する場合、リクエストボディは任意です。ファイルをアップロードする必要がある場合は、以下のように `--data-binary @empty.xlsx` を追加してください。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# newworkbook.xlsx という名前の空のワークブックを作成
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # 完全な空のワークブックの場合はこの行を省略
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速化できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---