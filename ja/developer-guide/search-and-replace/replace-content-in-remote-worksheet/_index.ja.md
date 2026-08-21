---
title: "Aspose.Cells Cloud 置換 Web API – リモートワークシート内のテキストを更新"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud API を使用してリモートワークシートのテキストを検索して置換"
linktitle: "リモートワークシートの内容を置換"
type: docs
url: /replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, テキスト置換, リモートワークシート, Excel API, クラウド表計算, 検索と置換, REST API"
description: "Aspose Cloud に保存された Excel ファイルの特定ワークシート内のテキストを置換します。パスワードで保護されたワークブック、地域設定に配慮した検索、一括更新をサポートします。"
weight: 100
---

リモート Excel ファイルの特定ワークシート内にある指定したテキストを置換します。Aspose.Cells の検索と置換 API を使用して、リモートスプレッドシートの指定されたシートの内容を効率的に更新し、正確なワークシート編集を実現します。

## **リモートワークシートの内容を置換する API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ名 | 型     | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                                                  |
| :----------- | :----- | :-------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name         | 文字列 | パス                              | クラウドストレージに保存され、変更対象となるワークブックファイルの名前 (例: `"sales_report.xlsx"`, `"budget_2024.xls"`）。                                               |
| worksheet    | 文字列 | パス                              | 検索と置換操作を実行する特定のワークシートの名前 (例: `"Q1_Sales"`, `"Sheet1"`）。                                                                                      |
| searchText   | 文字列 | クエリ                            | 指定されたワークシート内で検索するテキスト文字列。ワークシート内のすべてのセルに対して検索が適用されます (ただし、さらに条件を絞り込むことは可能です)。               |
| replaceText  | 文字列 | クエリ                            | 指定されたワークシート内で見つかった `searchText` のすべての出現箇所を置換するテキスト文字列。                                                                        |
| folder       | 文字列 | クエリ                            | ソースワークブックが配置されているクラウドストレージのフォルダパス (例: `"/reports/monthly/"`, `"/finance/"`).                                                         |
| storageName  | 文字列 | クエリ                            | _(任意)_ カスタムクラウドストレージの名前 (例: `"CorporateS3"`, `"AzureArchive"`). 省略した場合、アカウントのデフォルトクラウドストレージが使用されます。              |
| region       | 文字列 | クエリ                            | _(任意)_ テキスト処理のロケールを設定します。これにより、ワークシート内の文字エンコーディングや言語固有の検索動作に影響を与える可能性があります (例: `"en-GB"`, `"es-ES"`). |
| password     | 文字列 | クエリ                            | _(任意)_ ワークブックがパスワードで保護されている場合、ファイルを開いて変更するためにパスワードを指定します。                                                            |

**リクエストの例 (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/sales_report.xlsx/worksheets/Sheet1/replace/content?searchText=OldValue&replaceText=NewValue&folder=/reports" \
     -H "Authorization: Bearer {access_token}"
```

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### **エラーコード**

| コード | 説明                     | 発生状況                                                         |
|--------|--------------------------|------------------------------------------------------------------|
| 400    | 不正リクエスト (Bad Request) | リクエスト URI が不正、または必須パラメータが不足しています。         |
| 401    | 認証エラー (Unauthorized)  | アクセストークンが不足・無効、またはクライアント認証情報が誤っています。 |
| 404    | 見つからない (Not Found)   | 指定されたワークブックまたはワークシートが見つかりません。           |
| 500    | サーバー内部エラー (Internal Server Error) | リクエスト処理中に予期しないエラーが発生しました。                |

## リモートスプレッドシートのワークシート内容を置換する API の使用例

- **バッチクラウドファイル更新**: AWS S3 や Azure Blob などのクラウドストレージに保存された複数の Excel ファイルの内容を一括で変更します。
- **クラウドテンプレートの動的データ展開**: クラウドに保存されたレポートテンプレートに対して、動的データを一括で展開します。
- **地域横断ファイル同期**: 異なる地理的地域にまたがるクラウドストレージ内の Excel ファイルの内容の一貫性を同期します。

## なぜリモートスプレッドシートのワークシート内容を置換する API を使用すべきか

- **開発者フレンドリー**: Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供しており、迅速な開発が可能で、包括的なドキュメントも整備されています。独自のチャート描画ソリューションを構築する場合と比較して、開発負担を大幅に軽減します。
- **人件費削減**: 文書の統合作業を行う担当者の必要性を低減します。
- **従量課金制**: 初期投資は不要で、実際に使用した API コールのみに課金されます。
- **メンテナンスコストゼロ**: サーバーの保守、ソフトウェアの更新、互換性問題への対応が不要です。

## SDK を使用してリモートスプレッドシートのワークシート内容を置換する API を利用する方法

### **OpenAPI 仕様**

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) はパブリックに利用可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 操作を実行できます。

### **Aspose.Cells Cloud SDK を使用する**

SDK を使用することが開発を加速する最良の方法です。SDK は低レベルの詳細を処理するため、最小限のコードでスプレッドシートのワークシート内容置換を実装できます。  
Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスと連携する方法を示しています。