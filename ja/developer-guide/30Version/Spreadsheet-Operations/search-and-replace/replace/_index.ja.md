---
title: "Excel ファイル内のテキストを置換する"
second_title: "ドキュメント"
linktitle: "ストレージを使用せずに置換"
type: docs
url: /replace/
keywords: "Excel テキスト置換、Aspose.Cells Cloud、REST API、スプレッドシート置換、API、Excel ファイルテキスト置換"
description: "Aspose.Cells Cloud REST API を使用して、Excel ファイル内の既存のテキストを新しい値に置換します。C#、Java、Python、Node.js、PHP、Ruby、Go、Perl の SDK をサポートしています。"
weight: 80
---

## REST API

この REST API は、Excel ファイル内のデータを置換します。

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

### リクエストパラメータ

| パラメータ名 | 型     | 位置             | 説明                                      |
| ------------ | ------ | ---------------- | ----------------------------------------- |
| **file**     | file   | formData (multipart) | 処理対象の Excel ファイル。               |
| **text**     | string | クエリ           | 置換対象のテキスト文字列。                |
| **newtext**  | string | クエリ           | 置換後のテキスト。                        |
| **password** | string | クエリ           | パスワードで保護されたワークブックのパスワード（オプション）。 |
| **sheetname**| string | クエリ           | 対象とするワークシート名（オプション）。  |

### **レスポンス**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[file1 name]",
      "Filesize" : [file size],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[file2 name]",
      "Filesize" : [file size],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[file3 name]",
      "Filesize" : [file size],
      "FileContent" : "[Base64String]"
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                           |
|--------|--------------------------|------------------------------------------------|
| 200    | OK                       | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request              | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized             | JWT トークンが無効または不足しています。       |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error    | 予期しないサーバーエラーが発生しました。        |

## SDK を使用した PostReplace API の利用方法

### PostReplace API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) は、パブリックに公開されたプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクションを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

SDK を使用することで、開発スピードを最大化できます。SDK は低レベルの詳細な処理を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}