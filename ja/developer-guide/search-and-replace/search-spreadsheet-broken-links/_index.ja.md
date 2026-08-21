---
title: "スプレッドシートのリンク切れを検索 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
ArticleTitle: "Excelのリンク切れを検索・修正 – クラウドスプレッドシートリンクチェッカー"
linktitle: "スプレッドシートのリンク切れを検索"
type: docs
url: /search-spreadsheet-broken-links/ja/
keywords: "Aspose Cells, リンク切れ, スプレッドシート監査, Excel API, クラウドスプレッドシート, リンクチェッカー"
description: "Aspose.Cells Cloud API を使用して Excel ワークブック内のリンク切れを検出し、修正します。範囲をスキャンし、詳細な JSON 結果を取得し、任意の言語の SDK と統合できます。"
weight: 100
---

## **スプレッドシートのリンク切れを検索 API**

Excel ファイル内のリンク切れを自動的に検出します。この API は、指定された範囲内のリンク切れの外部参照、無効な数式、および欠落しているデータソースをスキャンします。リモートスプレッドシート監査、自動品質チェック、およびクラウドストレージプロバイダーとの統合をサポートします。エンタープライズワークフロー自動化向けの RESTful API。

**概要:** このエンドポイントを使用して、ワークブック内の無効なリンクを迅速に特定・修正し、財務モデル、M&A データセット、投資家向けパッケージなどのデータ整合性を保証します。

### **Web API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### セキュリティと認証

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/ja/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### リクエストパラメータ

| パラメータ名 | 型     | 位置                  | 説明                                                                                                           |
|------------|--------|---------------------|---------------------------------------------------------------------------------------------------------------|
| Spreadsheet | ファイル | FormData (multipart) | **必須。** 分析対象の Excel ワークブックファイル（`.xlsx`、`.xls` など）。                                      |
| worksheet   | 文字列   | クエリ                 | **オプション。** 分析するワークシート名。指定しない場合、最初のワークシートが使用されます。                         |
| cellArea    | 文字列   | クエリ                 | **オプション。** A1 表記法でのターゲットセル範囲（例: `B2:D10`）。指定しない場合、使用されている全範囲が分析されます。   |
| region      | 文字列   | クエリ                 | **オプション。** ロケール設定（例: `ja-JP`）で、日付・数値・通貨の解釈に影響を与える可能性があります。                |
| password    | 文字列   | クエリ                 | **オプション。** 暗号化されたワークブック用のパスワード。ファイルが保護されていない場合は空のままにしてください。         |

### レスポンス

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "ファイルが見つかりません",
      "Status": "Broken"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Not Found",
      "Status": "Broken"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### エラーコード

| コード | 説明 |
|-------|------|
| **400 Bad Request** | 無効な Aspose.Cells Cloud API URI。 |
| **401 Unauthorized** | 無効なアクセストークン、クライアント ID、またはクライアントシークレット。 |
| **404 Not Found** | スプレッドシートファイルにアクセスできません。 |
| **429 Too Many Requests** | レート制限（1 分あたり 60 回の呼び出し）を超えました。 |
| **500 Server Error** | 数式計算データの取得中にスプレッドシートに異常が発生しました。 |


## いつスプレッドシートのリンク切れ検索 API を使用すべきか？

- **大規模な財務モデルの定期監査**: 月次・四半期報告書を公開する前に、多くの外部データ参照を含む重要な計算エリア（例: `Dashboard!B5:K50`）を自動スキャンし、すべてのリンクが有効なソースファイルを指していることを確認します。  
- **合併・買収（M&A）時のデータ統合**: 事業単位を表す複数のスプレッドシートファイルを統合した後、「Overview」ワークシートをスキャンし、ファイルパスの変更や権限の問題により無効になったリンクを特定します。  
- **投資家向けデータパッケージの作成**: 外部データベースや市場データソースにリンクされたチャートや表を含むプレゼンテーション資料を最終化する前に、すべてのリンクの有効性を検証します。

## なぜスプレッドシートのリンク切れ検索 API を使用すべきか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語で SDK ライブラリを提供しており、迅速な開発と包括的なドキュメントが可能です。カスタムソリューションの構築と比較して、開発作業を大幅に削減します。  
- **人件費の削減** – 文書リンクを手動で検証するための専任スタッフの必要性を排除します。  
- **従量課金制** – 前払い投資は不要で、実際に使用した API 呼び出しのみに課金されます。  
- **メンテナンスコストゼロ** – サーバーのメンテナンス不要、ソフトウェアの更新不要、互換性の問題もありません。  
- **複雑な Excel 書式を維持** – 結果は広く利用可能な JSON 形式で返され、元のワークブックのレイアウトが保持されます。

## SDK を使用したスプレッドシートのリンク切れ検索 API の利用方法

### OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} により、パブリックに利用可能なプログラミングインターフェースが定義され、Web ブラウザから直接 REST アクセスが可能になります。

### Aspose.Cells Cloud SDK の利用

SDK を使用することで、開発を最大限に高速化できます。SDK は下層の詳細を処理し、最小限のコードでリンク切れ検索機能を実装できます。Aspose.Cells Cloud SDK の完全な一覧については [GitHub リポジトリ](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}


---