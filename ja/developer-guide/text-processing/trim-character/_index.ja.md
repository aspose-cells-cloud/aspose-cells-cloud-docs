---
title: "Aspose.Cells Cloud Text Trimming Web API - 余分なスペースと改行の削除"
second_title: "ドキュメント"
ArticleTitle: "Excel データクリーナー - 文字、スペース、改行を自動でトリム – オンライン、ショートコード"
linktitle: "文字のトリム"
type: docs
url: /trim-character/
keywords: "Excel、テキストトリム、スペース削除、改行削除、Aspose.Cells、データクリーニング、スプレッドシート、セル書式の正規化"
description: "Aspose.Cells Cloud API を使用して Excel セルから余分なスペース、改行、不要な文字をトリムします。クリーンで一貫性のあるスプレッドシートデータを実現します。"
weight: 100
---

Aspose.Cells Trim Character API を使用して、Excel セルから不要な文字、余分なスペース、改行を自動的にトリムします。データエントリをクリーンにし、スプレッドシート全体で一貫した書式を維持します。

## **概要**

- **先頭と末尾のスペースをトリム**
  - テキストの先頭と末尾にある余分なスペースを削除
  - データの見た目や読みやすさを向上
- **単語間の余分なスペースの処理**
  - 単語間の余分なスペースを削除
  - 複数のデータソースから得られるデータによる書式の混雑を解消
- **特殊スペースの削除**
  - 特に非改行スペース（ノーブレークスペース）を明確に削除
  - データの正確性と一貫性を確保
- **改行の管理**
  - 余分な改行またはすべての改行を削除
  - セル内容を整理され、プロフェッショナルな見た目に保つ

## **TrimCharacter API**

API を呼び出す前に、有効な Aspose Cloud アカウント、`client_id`/`client_secret`、および **Cells** スコープを持つアクセストークンを取得しておく必要があります。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

```bash
-H "Authorization: Bearer {access_token}"
```

### **trimCharacter** API のリクエストパラメーター

| パラメーター名          | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                                                         |
| :---------------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet             | ファイル | FormData                   | 処理対象のスプレッドシートファイル。サポートされる形式は XLSX、XLS、ODS、CSV など。                                                                           |
| trimContent             | 文字列  | クエリ                      | セル内容からトリムする特定の文字または文字列を指定。単一文字、複数文字、またはカスタムパターンを指定可能。                  |
| trimLeading             | 真偽値  | クエリ                      | `true` の場合、各セルの内容の先頭から指定された文字を削除。                                                                            |
| trimTrailing            | 真偽値  | クエリ                      | `true` の場合、各セルの内容の末尾から指定された文字を削除。                                                                                  |
| trimSpaceBetweenWordTo1 | 真偽値  | クエリ                      | `true` の場合、各セル内で単語間の連続する複数のスペースを1つのスペースに圧縮。                                                                  |
| trimNonBreakingSpaces   | 真偽値  | クエリ                      | `true` の場合、セル内容から非改行スペース文字（Unicode U+00A0）を削除。                                                                          |
| removeExtraLineBreaks   | 真偽値  | クエリ                      | `true` の場合、各セル内で連続する複数の改行を1つの改行に圧縮。                                                                      |
| removeAllLineBreaks     | 真偽値  | クエリ                      | `true` の場合、セル内容からすべての改行文字を削除。                                                                                               |
| worksheet               | 文字列  | クエリ                      | _（オプション）_ 文字列トリムを適用するワークシート名。指定しない場合、最初のワークシートに操作が適用されます。                               |
| range                   | 文字列  | クエリ                      | _（オプション）_ 文字列トリムを適用するセル範囲（例: `"A1:C10"`）。指定しない場合、指定されたワークシート内のすべての使用済みセルに操作が適用されます。 |
| outPath                 | 文字列  | クエリ                      | _（オプション）_ 処理済みのワークブックを保存するクラウドストレージのフォルダーパス。指定しない場合、ファイルはソースフォルダーに保存されます。                          |
| outStorageName          | 文字列  | クエリ                      | 出力ファイルを保存するクラウドストレージの名前。                                                                                                 |
| region                  | 文字列  | クエリ                      | _（オプション）_ テキスト処理用のロケールを設定。特定の言語（例: `"en-US"`、`"ar-SA"`）におけるスペースや改行の処理に影響を与える可能性があります。               |
| password                | 文字列  | クエリ                      | _（オプション）_ アップロードされたスプレッドシートがパスワード保護されている場合、ファイルを開いて処理するためにパスワードを指定。                                                  |

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

**成功例（HTTP 200）**: API は、トリムされたワークブックを含むファイルストリームを返します。

### エラーコード

- **400 Bad Request**: 無効な Aspose.Cells Cloud API URI。
- **401 Unauthorized**: 無効なアクセストークン。または無効な client id および secret。
- **404 Not Found**: スプレッドシートファイルにアクセスできません。
- **500 Server Error**: スプレッドシートで計算データの取得中に異常が発生しました。

## Trim Character API の使用場面

- **ユーザー入力の正規化**: 手動で入力された表データをクリーンアップし、余分なスペースや改行を削除。
- **顧客データベースの保守**: 顧客名、住所、連絡先情報などの冗長なスペースや書式の問題をクリーンアップ。
- **自動レポートのクリーンアップ**: 自動レポート生成前にデータソースの書式をクリーンアップ。
- **データ移行準備**: データを新しいシステムに移行する前に書式の問題をクリーンアップ。

## Trim Character API を使用すべき理由

- **労務コスト削減**: 手作業によるデータクリーニングに要する時間と手間を削減
- **エラー発生コスト削減**: 書式の問題による分析エラーを回避
- **従量課金制**: 固定費用はなく、実際のスループットのみが課金されます
- **インフラ投資不要**: サーバーまたはソフトウェアの運用が不要
- **多形式サポート**: XLSX、XLS、CSV、ODS など複数の形式の処理をサポート
- **開発者フレンドリー**: Aspose.Cells Cloud は複数言語の SDK ライブラリを提供しており、短時間での開発が可能で、包括的なドキュメントも整っています。カスタムのチャート描画ソリューションを構築する場合と比較して、開発負荷を大幅に削減できます。
- **コスト効率**: ワークブックを事前にアップロードせずに重複文字を削除でき、ストレージ容量の節約とコスト削減が可能です。

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを可能にします。

### Aspose.Cells Cloud SDK の使用

SDK の使用は開発加速の最良の方法です。SDK は内部の詳細を処理し、最小限のコードでセルの文字列トリムを実装できます。
Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}