---
title: "Aspose.Cells Cloud – ローカルの Excel ファイル内のテキストを置換（検索と置換 API）"
second_title: "ドキュメント"
ArticleTitle: "ローカル Excel ファイルの一括テキスト置換 – 検索と置換 API"
linktitle: "スプレッドシートのコンテンツを置換"
type: docs
url: /ja/replace-spreadsheet-content/
keywords: "Excel のテキストを置換, Aspose.Cells の検索と置換, ローカルスプレッドシート API, Excel ファイルを置換, API でコンテンツを置換"
description: "クラウドへのアップロードなしでローカルの Excel ワークブック内のテキストを置換します。Aspose.Cells Cloud の検索と置換 API を使用して、特定の範囲、ワークシート、またはファイル全体を 1 回の呼び出しで更新します。"
weight: 100
---

クラウドへのアップロードなしで、ローカルの Excel スプレッドシートファイル内に指定されたテキストを置換します。Aspose.Cells Cloud の検索と置換 API を使用して、オフライン編集を効率的に実行し、ワークブックのコンテンツを更新します。

## **スプレッドシートのコンテンツ置換 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ:**

| パラメータ名 | 型     | パス/クエリ文字列/HTTPボディ | 説明                                                                                                                                                                                                 |
| :----------- | :----- | :--------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet  | ファイル | FormData                     | 処理対象のローカルスプレッドシートファイル。サポートされる形式には、XLSX、XLS、ODS、CSV などがあります。                                                                                             |
| searchText   | 文字列   | クエリ                         | 指定されたワークシートおよびセル範囲内で検索するテキスト文字列。                                                                                                                                     |
| replaceText  | 文字列   | クエリ                         | 指定された範囲内で `searchText` のすべての出現箇所を置換するテキスト文字列。                                                                                                                         |
| worksheet    | 文字列   | クエリ                         | _(オプション)_ 検索と置換操作を実行するワークシート名。省略した場合、操作は最初のワークシートに適用されます。                                                                                          |
| cellArea     | 文字列   | クエリ                         | _(オプション)_ テキスト検索と置換を実行する特定のセル範囲（例: `"A1:D20"`、`"B5:F15"`）。省略した場合、操作は指定されたワークシート内のすべての使用済みセルに適用されます。                           |
| region       | 文字列   | クエリ                         | _(オプション)_ テキスト処理用のロケールを設定し、検索操作における大文字・小文字の区別や文字エンコーディングに影響を与える可能性があります（例: `"en-US"`、`"fr-FR"`）。                              |
| password     | 文字列   | クエリ                         | _(オプション)_ アップロードされたスプレッドシートがパスワード保護されている場合は、ファイルを開いて処理するためにパスワードを指定します。                                                            |

### **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

レスポンスは更新されたワークブックを含むバイナリストリームです。適切なファイル拡張子（例: `.xlsx`）で保存してください。

### **エラーコード**

- **400 Bad Request（不正なリクエスト）** – 無効な Aspose.Cells Cloud API URI、または不正な形式のパラメータ。
- **401 Unauthorized（認証エラー）** – 無効または不足しているアクセストークン。新しいトークンを取得してください。
- **404 Not Found（ファイルが見つかりません）** – スプレッドシートファイルにアクセスできない、または指定されたワークシートが存在しません。
- **500 Server Error（サーバーエラー）** – スプレッドシートの内部処理中にエラーが発生しました。問題が続く場合はサポートにお問い合わせください。

## どのような場面でスプレッドシートのコンテンツ置換 API を使用すべきですか？

- **ローカル Excel ファイルの一括処理** – オンプレミスに保存された多数のワークブックに対して、検索と置換を自動化します。
- **オンプレミスデータパイプライン** – レポートをアーカイブまたは配布する前に、スケジュールされたジョブに API を統合して内容を変更します。
- **ローカルレポート生成** – クラウドにアップロードせずに、テンプレートワークブックに動的に値を挿入します。

## なぜスプレッドシートのコンテンツ置換 API を使用すべきですか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語向けの SDK ライブラリを提供し、迅速な開発と包括的なドキュメントを可能にします。カスタムソリューションを構築する場合と比較して、開発効率が大幅に向上します。
- **人件費削減** – 手動でのドキュメント集約作業を行う専任スタッフの必要性を低減します。
- **従量課金制** – 前払い投資は不要で、実際に使用した API 呼び出し分のみを支払います。
- **メンテナンスコストゼロ** – サーバーのメンテナンス、ソフトウェア更新、互換性の心配が一切ありません。
- **複雑な Excel 書式を保持** – 置換後も、元のワークブックの書式、数式、チャートがそのまま維持されます。

## SDK を使用してスプレッドシートのコンテンツ置換 API を使用する方法

### **OpenAPI 仕様**

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) はパブリックに利用可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 操作を実行できます。

### **Aspose.Cells Cloud SDK の使用**

SDK を使用すると、開発を最速で加速できます。SDK が内部の詳細を処理するため、最小限のコードでコンテンツ置換操作を実装できます。サポートされている言語の完全な一覧については、公式の **Aspose.Cells Cloud SDK GitHub リポジトリ** をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスと対話する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}