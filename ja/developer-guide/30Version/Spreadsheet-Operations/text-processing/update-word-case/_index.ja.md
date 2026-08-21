---
title: "Aspose.Cells – 単語の大文字・小文字を更新する API"
second_title: "ドキュメント"
linktitle: "単語の大文字・小文字"
type: docs
url: /post-update-word-case/
keywords: "Aspose.Cells, 単語の大文字・小文字を更新する API, テキストの大文字小文字変換, Excel, CSV, Google スプレッドシート, REST API"
description: "Aspose.Cells Cloud の単語の大文字・小文字を更新する API を使用して、Excel、CSV、または Google スプレッドシートファイル内のテキストの大文字・小文字を変換します。大文字・小文字の変換、タイトルケース、および先頭文字の大文字化をサポートします。"
weight: 100
ArticleTitle: "Aspose.Cells – 単語の大文字・小文字を更新する API ドキュメント"
---

**API バージョン:** 3.0

スプレッドシート（Excel、Google スプレッドシート、CSV）内のテキストの大文字・小文字の不整合を管理するのは、特に大規模なデータセットでは面倒です。**PostUpdateWordCase Web API** は、テキストの大文字・小文字変換を自動化し、最小限の労力でクリーンで標準化されたデータを実現します。

## **Excel Web API – 単語の大文字・小文字を更新する API**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **機能説明**

PostUpdateWordCase Web API は、スプレッドシート内のテキストの大文字・小文字の不整合という一般的な問題に対処します。この不整合は、データ分析や処理に大きな影響を与える可能性があります。この API は大文字・小文字の変換を自動化し、データをクリーンで標準化された状態に保ち、后续の操作や分析に備えます。

- **自動テキストの大文字・小文字変換**
  - **大文字から小文字へ** – すべての大文字を小文字に変換します。
  - **小文字から大文字へ** – すべての小文字を大文字に変換します。
  - **先頭文字を大文字化** – 各単語の先頭文字を大文字にします。
  - **タイトルケース** – 主要な単語の先頭文字を大文字とするタイトルケースに変換します。

- **複数の形式をサポート** – この API は Excel、OpenOffice、JSON、CSV など、幅広いスプレッドシート形式で動作します。この多様性により、さまざまなデータ処理ニーズに対応可能です。

### **リクエストパラメータ**

| パラメータ名        | 型     | 位置         | 説明                                                                                                               |
| ------------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------ |
| `wordCaseOptions`   | オブジェクト | リクエストボディ | 変換対象の範囲、変換後のケースタイプ、その他の設定など、希望の大文字・小文字変換オプションを定義します。 |

**`wordCaseOptions` スキーマ**

```json
{
  "Range": "A1:B10", // 処理する Excel スタイルの範囲（必須）
  "CaseType": "Upper", // 列挙型: Upper（大文字）、Lower（小文字）、Capitalize（先頭大文字）、Title（タイトルケース）（必須）
  "IgnoreBlank": true // 論理値、オプション – true の場合、空白セルは変更されません
}
```

**リクエストボディの例**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – 大文字・小文字の変換を適用するセル範囲（例: `A1:C5`）。
- **CaseType** – 変換のタイプ。許可される値は `Upper`、`Lower`、`Capitalize`、`Title` です。
- **IgnoreBlank** – `true` の場合、空白セルは無視されます。デフォルトは `false` です。

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[結合されたファイル名]",
    "Filesize" : [ファイルサイズ],
    "FileContent" : "[Base64 文字列]"
}
```

- **Filename** – 処理されたファイルの名前。
- **FileSize** – ファイルサイズ（バイト単位）。
- **FileContent** – 変換されたファイルの Base64 エンコードされた内容。

**HTTP ステータスコード**

| コード | 意味               | 説明                                         |
| ------ | ------------------ | -------------------------------------------- |
| 200  | OK                    | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | リクエストエラー        | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401  | 認証されていません        | JWT トークンが無効または不足しています。                 |
| 413  | ペイロードが大きすぎます    | アップロードされたファイルがサイズ制限を超えています。         |
| 500  | サーバーエラー          | 予期しないサーバーエラーが発生しました。                 |

## SDK を使用した PostUpdateWordCase API の使用方法

### PostUpdateWordCase API の仕様

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---