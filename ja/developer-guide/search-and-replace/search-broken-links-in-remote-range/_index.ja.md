---
title: "Aspose.Cells Cloud – Excel 範囲内の壊れたリンクを検出する API"
second_title: "ドキュメント"
ArticleTitle: "リモート Excel 範囲内の壊れたリンクを検索・修正する – クラウドスプレッドシートリンクチェッカー"
linktitle: "リモート範囲の壊れたリンクを検索"
type: docs
url: /ja/search-broken-links-in-remote-range/
keywords: "Aspose, Cells, 壊れたリンク, API, Excel 範囲, 検証, クラウド, スプレッドシート, 外部参照, チェッカー"
description: "Aspose.Cells Cloud API を使用して、Excel 範囲内の壊れた外部リンク、無効な数式、欠落しているデータソースをスキャンします。安全で高速なクラウドベースの機能です。"
weight: 100
---

## **リモート範囲の壊れたリンクを検索する API**

クラウドストレージに保存された Excel ファイルの範囲データ内に存在する壊れたリンクを自動的に検出します。当社の API は、指定された範囲内に存在する壊れた外部参照、無効な数式、欠落しているデータソースをスキャンします。クラウドスプレッドシートの監査、自動品質チェック、クラウドストレージプロバイダーとの統合をサポートします。エンタープライズ向けワークフロー自動化のための RESTful API です。

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                                                                                                                                                                          |
| -------------- | ------ | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | 文字列 | パス   | **必須。** クラウドストレージに保存されている Excel ワークブックファイルの名前（例: `financial_report.xlsx`）で、このファイル内で壊れたリンクをスキャンします。                     |
| worksheet      | 文字列 | パス   | **必須。** ワークブック内の、壊れたリンクを検索する対象となる特定のワークシート名（例: `Sheet1`, `Q4_Data`）。                                                               |
| cellArea       | 文字列 | パス   | **必須。** 指定されたワークシート内の、壊れた外部参照、数式、リンクをスキャンする対象セル範囲のアドレス（例: `A1:F100`）。                                                     |
| folder         | 文字列 | クエリ | **オプション。** 対象ワークブックが配置されているクラウドストレージ内のディレクトリパス。省略した場合、ルートディレクトリが前提とされます。                                    |
| storageName    | 文字列 | クエリ | **オプション。** 設定済みのクラウドストレージサービスの名前（例: `DropboxBusiness`, `S3Bucket`）。指定されない場合、API はアカウントのデフォルトストレージを使用します。      |
| region         | 文字列 | クエリ | **オプション。** スキャン時に適用するロケール設定（例: `en-GB`, `de-DE`）で、地域固有のデータ解釈に使用されます。                                                              |
| password       | 文字列 | クエリ | **オプション。** パスワードで保護されたワークブックにアクセスするために必要な復号化パスワード。ファイルが暗号化されていない場合は空欄のままにしてください。                   |

**リクエストボディの例**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### 応答

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

`BrokenLinks` コレクションは **BrokenLink** 型のオブジェクトを格納します。各オブジェクトには以下のプロパティが含まれます：

- **CellName** – 壊れた参照を含むセルのアドレス（例: `B12`）。
- **LinkType** – 壊れているリンクの種類（例: `ExternalReference`, `Formula`）。
- **ErrorMessage** – リンクが壊れていると判断された理由の説明。

**注意**: 本 API はレート制限の対象となります。詳細は [価格設定とレート制限](https://www.aspose.cloud/pricing) ページをご参照ください。

### エラーコード

- **400 Bad Request（不正なリクエスト）** – 不正な Aspose.Cells Cloud API URI。
- **401 Unauthorized（未承認）** – 不正なアクセストークン、クライアント ID、またはクライアントシークレット。
- **404 Not Found（見つかりません）** – スプレッドシートファイルにアクセスできません。
- **500 Server Error（サーバーエラー）** – 数式計算データの取得中にスプレッドシートに異常が発生しました。

## いつスプレッドシート範囲内の壊れたリンクを検索する API を使用すべきか？

- **大規模な財務モデルの定期監査** – 月次または四半期報告書を公開する前に、多数の外部データ参照を含む重要な計算領域（例: `Dashboard!B5:K50`）を自動スキャンし、すべてのリンクが有効なソースファイルを指していることを確認します。
- **企業合併・買収時のデータ統合** – 複数の事業単位を表すスプレッドシートファイルを統合した後、「Overview」ワークシートをスキャンし、ファイルパスや権限の変更により無効になったリンクを特定します。
- **投資家向け資料パッケージの作成** – 外部データベースや市場データソースにリンクされたチャートや表を含むプレゼンテーション資料を最終確定する前に、すべてのリンクの有効性を検証します。

## なぜスプレッドシート範囲内の壊れたリンクを検索する API を使用すべきか？

- **開発者にやさしい** – Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供し、包括的なドキュメントにより迅速な開発を実現します。カスタムソリューションの構築と比較して、開発工数を大幅に削減できます。
- **人的コストの削減** – 文書の手動集約に専任の担当者を配置する必要がなくなります。
- **ペイ・パー・ユース** – 初期投資不要。実際に実行した API コール分のみ課金されます。
- **メンテナンスコストゼロ** – サーバーの管理やソフトウェアの更新、互換性の懸念がありません。
- **複雑な Excel 書式を保持** – 結果は書式を保持したまま、汎用的にアクセス可能な PDF 形式でエクスポートできます。

## SDK を使用してスプレッドシート範囲内の壊れたリンクを検索する API を使用する方法

### OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) はパブリックに利用可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 通信を実行できます。

### Aspose.Cells Cloud SDK の使用

SDK の使用は開発を加速する最良の方法です。SDK は内部の詳細を処理し、「範囲内の壊れたリンクを検索」機能を最小限のコードで実装できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご参照ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}