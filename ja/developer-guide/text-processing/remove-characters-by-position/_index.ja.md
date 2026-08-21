---
title: "Aspose.Cells Cloud 位置指定文字削除 Web API – Excel から特定の位置のテキストを削除"
second_title: "ドキュメント"
ArticleTitle: "Excel 位置ベース文字削除ツール – 特定の位置のテキストを削除 – オンラインショートコード"
linktitle: "位置指定で文字を削除"
type: docs
url: /ja/remove-characters-by-position/
keywords: "Aspose.Cells Cloud, 位置指定で文字を削除, Excel テキストクリーニング, 最初の N 文字を削除, 最後の N 文字を削除, マーカー前のテキストを削除, マーカー後のテキストを削除, 値間のテキスト削除"
description: "Aspose.Cells Cloud Web API を使用して、Excel セル内の位置に基づいて文字を削除します。先頭／末尾の N 文字、または特定のマーカーの前／後のテキストを高精度で削除できます。"
weight: 100
---

位置に基づいて Excel セルの文字を削除：先頭／末尾の N 文字を削除するか、指定したマーカーの前／後のテキストを削除します。Aspose.Cells Cloud Web API を使用した高精度のテキストクリーニング。

## **はじめに**：位置指定で不要な文字を削除

**削除モード**

- `theFirstNCharacters` – 先頭から N 文字を削除
- `theLastNCharacters` – 末尾から N 文字を削除
- `allCharactersBeforeText` – 指定した部分文字列の最初の出現位置より前のすべての文字を削除
- `allCharactersAfterText` – 指定した部分文字列の最初の出現位置より後のすべての文字を削除
- `BetweenValues` – 2 つのユーザー定義値間の部分文字列（およびオプションで区切り文字自体）を削除

**オプション**

- `caseSensitive` – `BeforeText`、`AfterText`、`BetweenValues` の検索において大文字・小文字を区別するかどうかを指定

## **RemoveCharactersByPosition API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>を必要とします。

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveCharactersByPosition** API のリクエストパラメーター

| パラメーター名             | 型      | パス／クエリ文字列／HTTP ボディ | 説明                                                                                                                                                        |
| ------------------------- | ------- | ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet               | ファイル | FormData                        | 処理対象のスプレッドシートファイル。サポートされる形式には XLSX、XLS、ODS、CSV などがあります。                                                              |
| Authorization             | 文字列   | ヘッダー                         | 認証用のベアラートークン（必須）                                                                                                                            |
| theFirstNCharacters       | 整数    | クエリ                          | 各選択セルのテキスト先頭から削除する文字数（例：`3` を指定すると先頭 3 文字を削除）                                                                           |
| theLastNCharacters        | 整数    | クエリ                          | 各選択セルのテキスト末尾から削除する文字数（例：`2` を指定すると末尾 2 文字を削除）                                                                           |
| allCharactersBeforeText   | 文字列   | クエリ                          | 各セル内の指定した文字列より前のすべての文字を削除します。文字列が複数回出現する場合、最初の出現位置を基準に削除します。                                      |
| allCharactersAfterText    | 文字列   | クエリ                          | 各セル内の指定した文字列より後のすべての文字を削除します。文字列が複数回出現する場合、最初の出現位置を基準に削除します。                                      |
| worksheet                 | 文字列   | クエリ                          | _(オプション)_ 文字削除を適用するワークシート名。省略した場合、最初のワークシートに対して操作が適用されます。                                               |
| range                     | 文字列   | クエリ                          | _(オプション)_ 文字削除を適用するセル範囲（例：`"A1:C10"`）。省略した場合、指定されたワークシート内のすべての使用済みセルに対して操作が適用されます。        |
| outPath                   | 文字列   | クエリ                          | _(オプション)_ 処理済みワークブックを保存するクラウドストレージのフォルダー パス。省略した場合、ファイルは元のフォルダーに保存されます。                    |
| outStorageName            | 文字列   | クエリ                          | 出力ファイルを保存するクラウドストレージの名前。                                                                                                            |
| region                    | 文字列   | クエリ                          | _(オプション)_ テキスト処理のロケールを設定します。特に言語固有の文字位置やエンコーディングに重要です（例：`"en-US"`、`"zh-CN"`）。                           |
| password                  | 文字列   | クエリ                          | _(オプション)_ アップロードされたスプレッドシートがパスワード保護されている場合、ファイルを開いて処理するためのパスワードを指定します。                      |

### **レスポンス**

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

- **200 OK** – リクエストが成功し、処理済みファイルが返されます。
- **400 Bad Request**：不正な Aspose.Cells Cloud API URI。
- **401 Unauthorized**：無効なアクセス トークン、または無効なクライアント ID とシークレット。
- **404 Not Found**：スプレッドシートファイルにアクセスできません。
- **500 Server Error**：スプレッドシートの計算データ取得中に異常が発生しました。

## Remove Characters by Position API の使用例

- **データの標準化**：製品コードのクリーニング（先頭のゼロやサフィックスの削除）、電話番号のクリーニング（国番号の削除）
- **テキスト抽出**：ログファイルから重要な情報を抽出（タイムスタンプやプレフィックスの削除）
- **ファイル処理**：ファイル名の整理（一貫したプレフィックスや日付サフィックスの削除）
- **データ解析**：構造化テキストの処理（ブラケットや特定のマーカー間のコンテンツ抽出）
- **データベース管理**：インポートデータのクリーニング（固定書式のヘッダー／トレーラー文字の削除）

## Remove Characters by Position API を使用する理由

- **正確かつ効率的**：位置指定による直接削除により、複雑な正規表現が不要になります。
- **柔軟な設定**：5 種類の位置モードと大文字・小文字の区別オプションにより、多様なシーンに対応。
- **バッチ処理**：単一の呼び出しで全列をクリーニングし、最大 10 倍の効率向上を実現。
- **スマート解析**：2 つの区切り文字間のコンテンツ抽出を簡単に行えます。
- **開発者フレンドリー**：Aspose.Cells Cloud は複数言語用の SDK を提供し、開発を加速し、包括的なドキュメントを提供します。独自のテキスト処理ロジックを構築する場合と比べ、開発工数を大幅に削減できます。
- **コスト効率**：ワークブックをアップロードせずに文字を削除できるため、ストレージ容量を節約し、コストを削減できます。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを可能にします。

### Aspose.Cells Cloud SDK の使用

SDK を使用するのが開発加速の最良の方法です。SDK は下層の詳細を処理し、最小限のコードでセルの文字削除機能を実装できます。  
Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---