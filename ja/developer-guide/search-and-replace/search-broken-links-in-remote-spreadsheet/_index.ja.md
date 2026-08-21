---
title: "Aspose.Cells Cloud – Excel のリンク切れ検出 API – クラウド上のワークブック内のスプレッドシートリンクをスキャン・検証"
second_title: "ドキュメント"
ArticleTitle: "クラウド上の Excel ファイルのリンク切れを検索・修正 – クラウドスプレッドシートリンクチェッカー"
linktype: "Search Remote Spreadsheets Broken Links"
type: docs
url: /search-broken-links-in-remote-spreadsheet/
keywords: "Excel, リンク切れ, API, クラウド, スプレッドシート, 検証, Aspose.Cells"
description: "Aspose.Cells Cloud API を使用して、クラウド上の Excel ワークブックに含まれるリンク切れの外部参照、無効な数式、欠落したデータソースをスキャンします。"
weight: 100
---

## **クラウド上のスプレッドシートでリンク切れを検索する API**

クラウドストレージに保存された Excel ファイル内のリンク切れを自動的に検出します。この API は、指定された範囲内でリンク切れの外部参照、無効な数式、欠落したデータソースをスキャンします。クラウドストレージプロバイダーとの統合をサポートし、リモートスプレッドシートの監査や自動品質チェック、エンタープライズレベルのワークフロー自动化が可能です。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ名 | 型     | パス／クエリ文字列／HTTPボディ | 説明                                                                                                                                               |
| :----------- | :----- | :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name         | 文字列 | パス                          | **必須。** リンク切れをスキャンする Excel ワークブックファイル名（例: `Quarterly_Report.xlsx`）。                                                 |
| worksheet    | 文字列 | クエリ                        | **必須。** 検索操作を実行するワークシート名。ワークブック内に表示される実際のシート名を正確に指定してください。                                   |
| cellArea     | 文字列 | クエリ                        | **必須。** リンク切れを分析するセル範囲（A1 形式で指定、例: `C5:J50`）。API はこの範囲内のみを検索対象とします。                                   |
| folder       | 文字列 | クエリ                        | **任意。** クラウドストレージ上のワークブックが格納されたディレクトリのパス。省略した場合、ルートディレクトリが前提となります。                   |
| storageName  | 文字列 | クエリ                        | **任意。** カスタムクラウドストレージ設定の名前。省略した場合、システムのデフォルトストレージが使用されます。                                      |
| region       | 文字列 | クエリ                        | **任意。** 処理中に適用されるロケール設定（例: `ja-JP`）。地域固有の数式構文や参照の解釈に影響を与える可能性があります。                          |
| password     | 文字列 | クエリ                        | **任意。** 暗号化されたスプレッドシートを開くために必要なパスワード。ファイルがパスワード保護されていない場合は省略してください。                 |

**cURL リクエストの例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **レスポンス**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**JSON レスポンスの例**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "ファイルが見つかりません"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "クラウドモードでは外部参照がサポートされていません"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### エラーコード

- **400 Bad Request（不正なリクエスト）** – 無効な Aspose.Cells Cloud API URI です。  
- **401 Unauthorized（認証エラー）** – 無効なアクセストークン、クライアント ID、またはクライアントシークレットです。  
- **404 Not Found（ファイルが見つかりません）** – スプレッドシートファイルにアクセスできません。  
- **500 Server Error（サーバーエラー）** – 計算データの取得中に異常が発生しました。

## スプレッドシート内のリンク切れ検索 API の使用例

- **大規模な財務モデルの定期監査** – 月次・四半期レポートの公開前に、多数の外部データ参照を含む重要な計算領域（例: `Dashboard!B5:K50`）をスキャンし、すべてのリンクが有効なソースファイルを指していることを確認します。  
- **買収・合併（M&A）時のデータ統合** – 複数の事業単位を表すスプレッドシートを統合した後、「概要」シートをスキャンし、ファイルパスや権限の変更により無効になったリンクを特定します。  
- **投資家向け資料パッケージの作成** – 外部データベースや市場データソースにリンクされたチャートや表を含む最終プレゼン資料作成前に、すべてのリンクの有効性を検証します。

## スプレッドシート内のリンク切れ検索 API を使用する理由

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供し、充実したドキュメントにより高速開発が可能です。カスタムソリューションの構築と比較して、開発労力を大幅に削減できます。  
- **人件費削減** – リンク検証を自動化することで、ドキュメントを手動で統合・確認するための専任スタッフが不要になります。  
- **ペイ・パー・ユース（従量課金）** – 事前投資は不要で、実際に使用した API コール分のみ課金されます。  
- **メンテナンス不要** – サーバーの管理、ソフトウェアの更新、互換性の懸念が一切ありません。

## SDK を使用したスプレッドシート内のリンク切れ検索 API の利用方法

### OpenAPI 仕様

[OpenAPI 仕様書](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST API を呼び出すことが可能です。

### Aspose.Cells Cloud SDK の利用

SDK を使用することで、開発を最適かつ迅速に進められます。SDK は内部の HTTP 処理を抽象化し、最小限のコードでリンク切れ検出機能を実装できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご参照ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスと連携する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}