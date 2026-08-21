---
title: "複数のExcelファイルを1つのスプレッドシートに統合する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
ArticleTitle: "複数のExcelファイルを1つに結合する – 30以上の形式にスプレッドシートを一括統合"
linktype: "スプレッドシートの統合"
type: docs
url: /merge-spreadsheets/
keywords: "Aspose.Cells, スプレッドシートの統合, Excel API, クラウドスプレッドシート, 一括統合, PDF変換, CSV統合, ODS統合, APIリファレンス, SDK"
description: "Aspose.Cells Cloud を使用して、ローカルの Excel、CSV、ODS ファイルを複数統合し、結果を 30 以上の形式（PDF、HTML など）に変換します。エンドポイント、パラメータ、認証ガイド、SDK サンプルを含みます。"
weight: 100
---

Aspose.Cells Cloud API を使用して、複数のローカル Excel、CSV、ODS ファイルを1つのワークブックに統合し、30以上の出力形式に変換します。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名     | 型      | 位置             | 説明                                                                                      |
| ---------------- | ------- | ---------------- | ----------------------------------------------------------------------------------------- |
| Spreadsheet      | ファイル | FormData         | アップロードするローカルスプレッドシートファイル。XLSX、XLS、CSV、ODS などに対応。         |
| outFormat        | 文字列  | クエリ           | 出力形式（例: `XLSX`、`PDF`、`CSV`、`HTML`）。30以上の形式に対応。                          |
| mergeInOneSheet  | 真偽値  | クエリ           | `true` → 全データを1つのワークシートに統合；`false` → 各元シートを保持。                    |
| outPath          | 文字列  | クエリ（オプション） | 統合ファイルを保存するクラウドフォルダのパス。省略した場合、デフォルトの場所が使用されます。 |
| outStorageName   | 文字列  | クエリ           | 使用するクラウドストレージの名前（デフォルトまたはカスタム）。                              |
| fontsLocation    | 文字列  | クエリ（オプション） | 正しい PDF / 画像レンダリングのためのカスタムフォントを含むクラウドフォルダ。               |
| region           | 文字列  | クエリ（オプション） | 数値・日付・通貨の書式設定に使用するロケール（例: `en-US`、`zh-CN`）。                       |
| password         | 文字列  | クエリ（オプション） | 保護されたスプレッドシートを開くためのパスワード。                                          |

### **レスポンス**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

ファイルは `outPath` で指定された場所から直接ダウンロードするか、保存できます。

**成功レスポンスの詳細**

| ステータスコード | コンテンツタイプ           | 説明                             |
| ---------------- | -------------------------- | -------------------------------- |
| 200 OK           | `application/octet-stream` | 統合されたワークブックファイルのバイナリストリーム。 |

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                       |
| ------ | -------------------- | ---------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用された；レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request          | 必須パラメータが不足または不正（例: 非対応ファイル形式）。     |
| 401    | Unauthorized         | JWT トークンが不正または不足。                               |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えた。             |
| 500    | Internal Server Error | 予期しないサーバーエラー。                                   |

## スプレッドシート統合 API の利用シーン

### **教育・学術用途**

- **学生課題の採点** – 複数の学生課題ファイルを統合し、一括でコメントや採点を行う。
- **研究データ収集** – 異なる実験グループからのデータスプレッドシートを統合。
- **教材作成** – 複数章の演習問題を1つの問題集ワークブックに統合。

### **データ処理・分析**

- **小規模データセット統合** – 異なるソースからエクスポートされた CSV または Excel ファイルを統合。
- **データ分析前処理** – 分析前に関連データファイルを統合。
- **テンプレートデータ入力** – 事前設定されたレポートテンプレートに統合データを入力。

### **開発・技術サポート**

- **テストデータ作成** – 複数のテストケースファイルを統合し、自動テストに使用。
- **ログファイル分析** – 異なる期間のシステムログ Excel レポートを統合。
- **設定管理** – 複数の設定スプレッドシートを1つの統合設定ファイルに統合。

## なぜスプレッドシート統合 API を使用すべきなのか？

- **開発者フレンドリー** – 多言語向け SDK ライブラリが提供されており、カスタムソリューション構築に比べて開発負担が軽減されます。
- **人件費削減** – 手動での文書統合作業に専任スタッフを割り当てる必要がなくなります。
- **ペイ・ペア・ユース（使用量課金）** – 実際に実行した API コール分のみ課金；前期費用は不要。
- **メンテナンスコストゼロ** – サーバーのメンテナンス、ソフトウェアアップデート、互換性問題が一切不要。

## SDK を使用したスプレッドシート統合 API の利用方法

### OpenAPI 仕様

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">OpenAPI 仕様</a> により、API の機械可読型の記述が提供され、直接 REST 呼び出しが可能になります。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスへ簡単にアクセスできます。以下の例では、cURL を使ってクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード済み)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速になります。短いコードでスプレッドシートワークシートへのデータインポートが可能です。Aspose.Cells Cloud SDK の完全な一覧は <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}