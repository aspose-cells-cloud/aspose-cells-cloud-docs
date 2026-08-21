---
title: "Aspose Cells Cloud Excelテキスト検索API – リモートスプレッドシート範囲内のテキストを検索"
second_title: "ドキュメント"
ArticleTitle: "リモートExcelスプレッドシートのテキストを検索 – 特定の範囲でデータを検出"
linktype: "検索範囲内のリモートコンテンツ"
type: docs
url: /ja/search-content-in-remote-range/
keywords: "Aspose.Cells, Excel API, テキスト検索, リモート範囲, クラウドスプレッドシート, REST API, データ検出"
description: "Aspose Cloudに保存されたExcelワークブックの特定範囲内で、テキスト、数値、または数式を検索します。"
weight: 100
---

## **リモート範囲内でのコンテンツ検索**

Aspose.Cells Cloud API を使用して、Excelスプレッドシートの任意の範囲内で特定のテキストをプログラムで検索します。クラウドストレージに保存されたリモートファイル内から、テキスト、数値、または数式を検索します。自動化されたデータ検出、コンテンツ分析、スプレッドシート監査ワークフローのためのRESTful APIです。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```


**cURLの例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### リクエストパラメータ

| パラメータ名 | 型      | Path/Query/String/HTTPBody | 説明                                                                                                                                                 |
| :----------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| name         | 文字列  | Path                       | **必須**。検索対象のExcelワークブックのファイル名（拡張子を含む）。例：`customer_data.xlsx`。                                                       |
| worksheet    | 文字列  | Path                       | **必須**。ワークブック内の検索対象ワークシートの正確な名前。例：`Orders_2024`。                                                                    |
| cellArea     | 文字列  | Path                       | **必須**。検索対象のセル範囲。A1表記法（例：`B2:H100`）で指定します。この範囲内でのみ検索が実行されます。                                             |
| searchText   | 文字列  | Query                      | **必須**。定義されたセル範囲内で検索する特定のテキスト文字列、数値、または部分的な内容。                                                             |
| ignoreCase   | 真偽値  | Query                      | **任意**。`true`に設定すると、大文字・小文字の違いを無視して検索します（例：「Report」は「report」にもマッチ）。デフォルトは`false`（大文字・小文字を区別）。 |
| folder       | 文字列  | Query                      | **任意**。ワークブックが配置されているクラウドストレージ内のディレクトリパス。省略された場合、ルートディレクトリが使用されます。                   |
| storageName  | 文字列  | Query                      | **任意**。カスタムクラウドストレージ設定の識別子。指定されない場合、アカウントのデフォルトストレージが使用されます。                               |
| region       | 文字列  | Query                      | **任意**。検索中に地域固有の文字や形式の解釈に影響を与える可能性があるカルチャ/地域設定（例：`en-AU`）。                                            |
| password     | 文字列  | Query                      | **任意**。パスワードで保護されたスプレッドシートファイルの復号化とアクセスに使用するパスワード。ファイルが暗号化されていない場合は指定不要です。   |

### レスポンス

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

### エラーコード

- **400 Bad Request** – 無効なAspose.Cells Cloud API URI。  
- **401 Unauthorized** – 無効なアクセストークン、クライアントID、またはクライアントシークレット。  
- **404 Not Found** – スプレッドシートファイルにアクセスできません。  
- **500 Server Error** – 予期せぬ条件により、サーバーがリクエストを処理できませんでした。

## スプレッドシートの範囲内でのコンテンツ検索APIは、どこで使用すべきですか？

- **大規模なデータ品質チェック** – データウェアハウスETLプロセスの受入段階で、データマッピングテーブル（`DataDictionary!B2:F1000`）内に欠落したフィールド説明、未定義の略語、またはプレースホルダーテキスト（例：`"TBD"` または `"NULL"`）がないか検索し、不完全なデータ定義を特定します。  
- **動的レポート生成とコンテンツ抽出** – 自動レポートシステムでは、混合データを含むテンプレートワークシート（`Monthly_Metrics!C10:G50`）内から、特定の識別子（例：`"[KPI]"`）でマークされた当期データブロックを智能的に検索・抽出し、最終レポートを作成します。  
- **契約および法的文書分析** – 多くの条項を含むスプレッドシートの付録をレビューする際、特定の法的用語（例：`"liability limit"`）、当事者名、日付を定義された範囲（`Contract_Terms!A:A`）内で効率的に検索し、レビュープロセスを高速化します。

## なぜスプレッドシートの範囲内でのコンテンツ検索APIを使用すべきですか？

- **開発者フレンドリー** – Aspose.Cells Cloudは、複数の言語向けのSDKライブラリを提供しており、迅速な開発と包括的なドキュメントにより、カスタムソリューションを構築する場合と比べて開発作業を大幅に削減します。  
- **人件費の削減** – 文書集約作業を担当する専任ポジションの必要性を排除します。  
- **ペイ-per-use（利用量課金）** – 初期投資不要。実際に使用したAPI呼び出しのみに課金されます。  
- **メンテナンスコストゼロ** – サーバーのメンテナンス不要、ソフトウェアの更新不要、互換性の懸念もありません。

## SDKを使用してスプレッドシートの範囲内でのコンテンツ検索APIを利用する方法

### OpenAPI仕様

[OpenAPI仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange)は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

### Aspose.Cells Cloud SDKの使用

SDKを使用することで、開発を最適化できます。SDKが底层の詳細を処理するため、スプレッドシートのセル範囲内でのコンテンツ検索を最小限のコードで実装できます。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、 various SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---