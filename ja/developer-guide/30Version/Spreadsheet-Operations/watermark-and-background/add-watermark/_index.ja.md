---
title: "Excel ファイルに透かしを追加する"
second_title: "ドキュメント"
linktitle: "Excel ファイルに透かしを追加する"
type: docs
url: /ja/add-watermark-into-excel-files/
aliases: [  /ja/watermark/ ]
keywords: "Excel に透かしを追加, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークブックにテキスト透かしを追加する方法を学習します。cURL の例、必要なパラメータ、およびレスポンスの詳細を含みます。"
weight: 39
ArticleTitle: "Excel ファイルに透かしを追加する – Aspose.Cells Cloud ドキュメント"
---

この REST API は、Excel ファイルに**透かし**を追加します。

**前提条件:** 有効な JWT アクセストークンを取得し、Excel ファイルがサポートされる形式（例：`.xlsx`、`.xls`）であることを確認してください。  
**背景:** 透かしとは、各ワークシートに適用される半透明のテキストオーバーレイで、所有権や機密性を示すために使用されます。

## PostWatermark API

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### **リクエストパラメータ**

| パラメータ名 | 型     | 位置                     | 説明                                               |
| ------------ | ------ | ------------------------ | -------------------------------------------------- |
| `file`       | ファイル | formData (multipart body) | 透かしを適用する Excel ファイル。                   |
| `text`       | 文字列  | クエリ                   | 表示する透かしテキスト。                           |
| `color`      | 文字列  | クエリ                   | ARGB 16進数形式（例：`004433ff`）で指定する透かしの色。 |

### **レスポンス**

JSON レスポンスには **Files** 配列が含まれます。各ファイルオブジェクトについて：

- **Filename** – 処理されたワークブックのファイル名。  
- **FileSize** – バイト単位のファイルサイズ。  
- **FileContent** – 透かしが適用された Excel ファイルの Base64 エンコードされたコンテンツ。実際のファイルを取得するにはこれをデコードします。

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
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した PostWatermark API の利用方法

### PostWatermark API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark)はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用して Aspose.Cells Web サービスを呼び出すことができます。以下の例では、認証ヘッダーを含む完全なリクエストを示しています。`<your-jwt-token>` を Aspose 認証エンドポイントから取得した有効な JWT アクセストークンに置き換えてください。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発が最も速く行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}