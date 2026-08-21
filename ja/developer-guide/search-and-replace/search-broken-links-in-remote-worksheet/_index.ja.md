---
title: "Aspose.Cells Cloud – Excel のリンク切れ検出 API – クラウド上のワークシート内のリンクをスキャン・検証"
second title: "ドキュメント"
article title: "クラウド上の Excel ワークシート内のリンク切れを検索・修正 – クラウド スプレッドシート リンク チェッカー"
link title: "クラウド上のワークシートのリンク切れを検索"
type: docs
url: /ja/search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, リンク切れ, Excel API, クラウド スプレッドシート, リンク検証"
description: "クラウド ストレージに保存された Excel ワークシート内の外部リンクのリンク切れを検出し、修正します。Aspose.Cells Cloud API を使用して範囲をスキャンし、リンクの詳細を取得して品質チェックを自動化します。"
weight: 100
---

## **クラウド上のワークシートのリンク切れを検索する API**

クラウド ストレージに保存された Excel ワークシート内のリンク切れを自動検出します。この API は、指定された範囲をスキャンし、リンク切れの外部参照、無効な数式、欠落しているデータ ソースを特定します。クラウド ストレージ プロバイダーとの統合、クラウド スプレッドシートの監査、品質チェックの自動化をサポートします。エンタープライズ ワークフローの自動化向けの RESTful API です。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエスト パラメーター**

| パラメーター名 | 種別 | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                                                                                                                                                                           |
| :------------- | :----- | :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | 文字列 | パス                        | **必須**。リンク切れを検索する Excel ブックのファイル名（拡張子付き、例：`Annual_Report.xlsx`）。                                                                                                                                                                                              |
| worksheet      | 文字列 | パス                        | **必須**。リンク スキャンを実行するワークシートの正確な名前（例：`DataSheet1`）。                                                                                                                                                                                                              |
| folder         | 文字列 | クエリ                      | **任意**。ターゲット ブックが配置されているクラウド ストレージ内のディレクトリ パス。省略した場合、ルート フォルダーが使用されます。                                                                                                                                                          |
| storageName    | 文字列 | クエリ                      | **任意**。カスタム設定されたクラウド ストレージの識別子。指定しない場合、API はアカウントのデフォルト ストレージを使用します。                                                                                                                                                                 |
| region         | 文字列 | クエリ                      | **任意**。検索時に適用するロケール設定（例：`fr-FR`）。一部の数式や地域固有のデータ形式の解釈に影響を与える可能性があります。_サポートされているロケール コードには `en-US`、`fr-FR`、`de-DE`、`es-ES` などがあります。_                                                                   |
| password       | 文字列 | クエリ                      | **任意**。パスワードで保護されたスプレッドシートの復号化パスワード。ファイルが暗号化されていない場合は省略してください。                                                                                                                                                                      |

**cURL リクエストの例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Source file not found"
    }
  ]
}
```

レスポンス オブジェクトは **BrokenLinksResponse** 型で、以下の要素を含みます：

- **BrokenLinks**：`BrokenLink` インスタンスのコレクション。各インスタンスは、問題のある参照（アドレス、エラー コード、エラー メッセージ）を示します。
- **Code**：サービスから返される数値のステータス コード。
- **Status**：結果のテキストによる説明。

**注意事項**：この API は結果をページングしません。1 回のリクエストで最大 10,000 個のリンク切れを返すことができます。アカウントあたりのレート制限は、1 分間に 100 回のリクエストです。

### エラー コード

- **400 Bad Request**：無効な Aspose.Cells Cloud API の URI。
- **401 Unauthorized**：無効または不足しているアクセス トークン。
- **404 Not Found**：スプレッドシート ファイルにアクセスできません。
- **500 Server Error**：計算データの取得中に異常が発生しました。

## どこでスプレッドシートのワークシート内のリンク切れ検索 API を使用すべきか？

- **大規模な財務モデルの定期監査**：月次・四半期ごとのレポートを公開する前に、大量の外部データ参照を含む重要な計算領域（例：`Dashboard!B5:K50`）を自動スキャンし、すべてのリンクが有効なソース ファイルを指していることを確認します。
- **合併・買収時のデータ統合**：事業単位を表す複数のスプレッドシート ファイルを統合した後、「Overview」ワークシートをスキャンし、ソース ファイルのパス変更や権限の問題により無効になったリンクを特定します。
- **投資家向けデータ パッケージの作成**：外部データベースや市場データ ソースにリンクされたチャートや表を含むプレゼンテーション資料を最終確定する前に、すべてのリンクの有効性を検証します。

## なぜスプレッドシートのワークシート内のリンク切れ検索 API を使用すべきか？

- **開発者フレンドリー**：Aspose.Cells Cloud は複数の言語向けの SDK ライブラリを提供しており、迅速な開発が可能で、包括的なドキュメントも整備されています。独自のチャート描画ソリューションを構築する場合と比べ、開発負荷を大幅に削減できます。
- **人件費の削減**：手動での文書統合やリンク検証に専任の人员を割り当てる必要がなくなります。
- **ペイ・パー・ユース**：初期投資は不要で、実際に使用した API コールのみに課金されます。
- **メンテナンスコストゼロ**：サーバーの保守やソフトウェアの更新、互換性の問題の管理が不要です。
- **複雑な Excel 書式を、汎用的にアクセス可能な PDF 形式で保持**。

## SDK を使用してスプレッドシートのワークシート内のリンク切れ検索 API を使用する方法

### OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) はパブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザーから直接 REST 操作を実行できるようにします。

### Aspose.Cells Cloud SDK を使用する

SDK の使用は開発を高速化する最良の方法です。SDK は内部の詳細を処理し、最小限のコードでスプレッドシートのワークシート内のリンク切れを検索する機能を実装できるようになります。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---