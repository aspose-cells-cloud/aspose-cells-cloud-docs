---
title: "Excel にテキストを追加: スプレッドシート Web API を使用して効率的にデータを挿入"
second_title: "ドキュメント"
linktitle: "テキストの追加"
type: docs
url: /excel-add-text/
keywords: "Excel, Aspose.Cells, テキスト追加, スプレッドシート API, REST API, Office Cloud, テキスト挿入, Excel API"
description: "Aspose.Cells Cloud API を使用して Excel スプレッドシート内の指定された場所にテキストを追加します。"
weight: 100
---

スプレッドシート内の指定された場所にテキスト コンテンツを追加します。これには、追加するテキストと挿入位置を定義するオブジェクトが必要です。

## **Excel API: PostAddTextContent**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **機能の説明**

このメソッドは、指定されたセルに新しいテキストを安全に追加し、複数の挿入モードとフォーマット処理をサポートします。

- **選択したセルの先頭にテキストを追加**  
  選択したすべてのセルの先頭にテキストを追加し、データ入力の一貫性を確保します。製品コード、カテゴリ、プレフィックスなどの共通識別子やラベルを追加するのに最適です。

- **特定のテキストの前後に文字を挿入**  
  選択したセル内の対象テキストの前後に文字を配置し、構造的で整理されたコンテンツを簡単に作成できます。

- **選択したすべてのセルの末尾に同じテキストを追加**  
  複数のセルに対して同じテキストを一括で末尾に追加し、データ入力を簡略化し、一貫した外観を保証します。

- **指定された文字数の前後にテキストを挿入**  
  対象範囲内の各セルの先頭または末尾から指定された文字数の位置にテキストを挿入します。典型的な使用例には、コード、タイムスタンプ、カスタムデリミタの書式設定などがあります。

### **リクエストパラメータ**

| パラメータ名       | 型    | 位置   | 説明                                                        |
| ------------------ | ----- | ------ | ----------------------------------------------------------- |
| addTextOptions     | クラス | 本文   | 追加するテキストコンテンツと、テキストを追加する位置を指定します。 |

### **レスポンス**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

**HTTP ステータスコード**

| コード | 意味                   | 説明                                         |
| ------ | ---------------------- | -------------------------------------------- |
| 200    | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request            | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized           | JWT トークンが無効、または不足しています。 |
| 413    | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error  | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した PostAddTextContent API の利用方法

### PostAddTextContent API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST のやり取りを実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最も効率的に加速できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}