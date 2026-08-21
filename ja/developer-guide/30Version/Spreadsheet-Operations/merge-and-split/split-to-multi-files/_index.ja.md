---
title: "Excel ファイルを複数のファイルに分割する"
second_title: "Document"
linktitle: "複数の Excel ファイルを分割する"
type: docs
url: /ja/split-an-excel-file-to-multi-files/
aliases: [  /ja/split-excel-workbooks/ , /ja/workbook/split/ ]
keywords: "Aspose.Cells, Cloud, Excel, Split, API, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API を使用して、複数のシートを含む Excel ワークブックを個別のファイルに分割します。出力形式として PDF、CSV、JSON をサポートし、Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift の各 SDK から利用できます。"
weight: 32
ArticleTitle: "Excel ファイルを複数のファイルに分割する - Aspose.Cells Cloud ドキュメント"
---

Aspose.Cells Cloud REST API を使用すると、複数のシートを含む Excel ワークブックを個別のファイルに分割できます。

**事前条件**  
API を呼び出す前に、有効な JWT トークンを取得し、各リクエストの `Authorization` ヘッダーに含める必要があります。詳細については、[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。

## PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置       | 説明                                      |
|-------------|--------|------------|-------------------------------------------|
| file        | file   | formData   | アップロードする Excel ワークブック。     |
| format      | string | query      | 期望する出力形式（例: `pdf`, `csv`, `json`）。 |
| password    | string | query      | 暗号化されたワークブックのパスワード（オプション）。 |
| from        | integer| query      | 含める最初のシートのインデックス（1始まり）。   |
| to          | integer| query      | 含める最後のシートのインデックス（含む）。     |

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[file1 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file2 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file3 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|--------|------------------------------|--------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request                  | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足している。             |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えた。   |
| 500    | Internal Server Error        | サーバー側で予期しないエラーが発生した。           |

## SDK を使用した PostSplit API の使い方

### PostSplit API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|--------|------------------------------|--------------------------------------------------|
| 200    | OK                           | ワークブックが正常に分割され、レスポンスにはファイル一覧が含まれる。 |
| 400    | Bad Request                  | パラメータが不足または無効（例: サポートされていない形式）。     |
| 401    | Unauthorized                 | JWT トークンが無効または不足している。             |
| 500    | Internal Server Error        | サーバー側で予期しないエラーが発生した。           |

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# xxxxx1.xlsx と xxxxx2.xlsx を実際の Excel ファイルのパスに置き換えてください
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を大幅に高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを行う方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---