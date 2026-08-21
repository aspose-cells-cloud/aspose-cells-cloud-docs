---
title: "Aspose.Cells Cloud Web API - Excel のテキストを数値に変換し、特殊文字をクリーンアップ"
second_title: "ドキュメント"
ArticleTitle: "Excel データクリーナー - テキストを数値に変換し、不要な文字を削除"
linktype: "テキストの変換"
type: docs
url: /ja/convert-text/
keywords: "Aspose.Cells テキスト変換、Excel のテキストを数値に変換、Excel の特殊文字削除、Excel の改行置換、アクセント文字の正規化、Excel データクリーニング API"
description: "Aspose.Cells Cloud API を使用して、Excel ファイル内のテキスト形式の数値を数値に変換し、不要な文字や改行を置換し、アクセント付き文字を標準的な文字に正規化します。"
weight: 100
---

Aspose.Cells API を使用して、Excel データをクリーンアップします。具体的には、テキスト形式の数値を数値に変換し、不要な文字や改行を置換し、アクセント付き文字を標準的な文字に正規化します。

## 概要

**テキストとして格納された数値を数値に変換、不要な文字を削除、アクセントを置換——1回の呼び出しで、数式は一切不要。**

- **テキストとして格納された数値を数値に変換**: テキストとして保存された数値データを真の数値に変換し、正確な計算と適切なデータ表現を保証します。
- **特定の文字を置換**: 選択したセル範囲内の指定された文字を一括で置換し、データを標準化します。
- **改行をスペース、コンマ、またはセミコロンに変換**: 読みやすさを向上させるために、セル内の改行をスペース、コンマ、またはセミコロンに変換し、より整理され視覚的に見やすい形式に整えます。
- **アクセント付き文字を置換**: データが多言語の場合、「é」や「ü」などのアクセント付き文字を非アクセントの対応する文字に置換し、一貫性と明確性を高めます。

## ConvertText API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **convertText** API のリクエストパラメータ

| パラメータ名     | 型     | Path/Query String/HTTPBody | 説明                                                                                                                                                           |
| ---------------- | ------ | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ファイル | FormData                   | 処理するスプレッドシートファイル。対応するフォーマットは XLSX、XLS、ODS、CSV などです。                                                                             |
| convertTextType  | 文字列 | クエリ                     | 適用するテキスト変換の種類を指定します。例：テキスト形式の数値を数値に変換、アクセント付き文字を非アクセントの同等文字に変換など。  |
| sourceCharacters | 文字列 | クエリ                     | 置換または削除する文字、文字列、パターンを指定します（例：`"é,è,ê"`、`"#N/A"`、改行には `"\\n"`）。                          |
| targetCharacters | 文字列 | クエリ                     | ソース文字を置換するための置換文字または文字列を指定します（例：アクセント付き文字には `"e"`、削除には `""`、改行には `" "`）。  |
| worksheet        | 文字列 | クエリ                     | _(オプション)_ テキスト変換を適用するワークシート名。省略した場合、最初のワークシートに適用されます。                               |
| range            | 文字列 | クエリ                     | _(オプション)_ テキスト変換を適用するセル範囲（例：`"A1:C10"`）。省略した場合、指定されたワークシートのすべての使用セルに適用されます。 |
| outPath          | 文字列 | クエリ                     | _(オプション)_ 処理済みのワークブックを保存するクラウドストレージのフォルダーパス。省略した場合、ファイルは元のフォルダーに保存されます。                            |
| outStorageName   | 文字列 | クエリ                     | 出力ファイルを保存するクラウドストレージの名前。                                                                                                   |
| region           | 文字列 | クエリ                     | _(オプション)_ テキスト変換ルールのロケールを設定します。特に言語固有の文字処理に有効です（例：`"en-US"`、`"fr-FR"`）。                  |
| password         | 文字列 | クエリ                     | _(オプション)_ アップロードされたスプレッドシートがパスワードで保護されている場合、ファイルを開いて処理するためのパスワードを指定します。                                                    |

### 応答

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### エラーコード

- **400 Bad Request**: 無効な Aspose.Cells Cloud API の URI。
- **401 Unauthorized**: 無効なアクセストークン、または無効なクライアント ID とシークレット。
- **404 Not Found**: スプレッドシートファイルにアクセスできません。
- **500 Server Error**: スプレッドシートで計算データの取得中に異常が発生しました。

## Convert Text API の使用例

- **数値フォーマットの修正**: 「123.45」などテキストとして格納された数値を、計算に適した数値形式に変換します。
- **特殊文字のクリーンアップ**: データから不要な特殊記号、余分なスペース、不可視文字を削除します。
- **改行の処理**: セル内の改行をスペースやその他の区切り文字に置換します。
- **アクセント文字の正規化**: 「é」や「ñ」などのアクセント付き文字を標準的な文字（「e」や「n」）に変換します。
- **CSV ファイルの前処理**: Excel に CSV ファイルをインポートする前に、テキスト形式を標準化します。

## Convert Text API を使用する理由

- **自動フォーマット変換**: 1回のリクエストで、テキスト形式の数値を一括で計算可能な値に変換します。
- **文字の標準化**: 特殊文字、記号、アクセント記号、エンコーディングの問題を一括で処理します。
- **データの一貫性**: 全データセット全体でテキスト形式を完全に統一します。
- **開発者フレンドリー**: Aspose.Cells Cloud は複数の言語向けの SDK ライブラリを提供しており、迅速な開発を可能にし、包括的なドキュメントも整っています。独自のテキスト処理ソリューションを構築する場合と比較して、開発作業を大幅に削減できます。
- **コスト効率**: ワークブックを事前にアップロードせずにテキストを変換できるため、ストレージ容量を節約し、コストを削減できます。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText) は公開可能なプログラミングインタフェースを定義し、Web ブラウザから REST 操作を直接実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用することで、開発を最適化できます。SDK は下層の詳細を処理するため、最小限のコードでセルのテキスト変換機能を実装できます。  
Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---