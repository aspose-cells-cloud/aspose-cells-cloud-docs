---
title: "Aspose.Cells Cloud 置換 Web API – リモートスプレッドシート内のテキストを更新"
second_title: "ドキュメント"
ArticleTitle: "クラウド Excel ファイルのテキストを一括置換 – Find & Replace API"
linktitle: "リモートスプレッドシートのコンテンツを置換"
type: docs
url: /ja/replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, コンテンツ置換, リモートスプレッドシート, Find & Replace API, クラウド Excel, 一括テキスト置換"
description: "Aspose.Cells Cloud Find & Replace API を使用して、クラウド上の Excel ワークブック内のテキストを一括で更新します。HTTPS エンドポイント、OAuth2 認証、およびすぐに利用できる SDK サンプルで、迅速な統合が可能です。"
weight: 100
---

クラウド上に保存されたリモート Excel ファイルに対して、一括テキスト置換を実行します。Aspose.Cells Find & Replace API を使用して、クラウドスプレッドシート内の特定のテキスト文字列を効率的に検索・更新します。


## **リモートスプレッドシートのコンテンツ置換 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### リクエストパラメータ

| パラメータ名     | 型     | 位置     | 説明                                                                                                                                                 |
| ---------------- | ------ | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**         | 文字列 | パス     | クラウドストレージに保存されている、変更対象のワークブックファイル名（例: `"report.xlsx"`）。                                                       |
| **searchText**   | 文字列 | クエリ   | ワークブック全体から検索する文字列。検索は大文字・小文字を区別し、他のパラメータで制限されない限りすべてのワークシートに適用されます。              |
| **replaceText**  | 文字列 | クエリ   | `searchText` のすべての出現箇所を置換する文字列。                                                                                                   |
| **folder**       | 文字列 | クエリ   | ソースワークブックを含むクラウドストレージのフォルダパス（例: `"/documents/quarterly/"`）。                                                         |
| **storageName**  | 文字列 | クエリ   | _(オプション)_ カスタムクラウドストレージの名前（例: `"MyS3Bucket"`）。省略された場合、アカウントに設定されたデフォルトストレージが使用されます。   |
| **region**       | 文字列 | クエリ   | _(オプション)_ 文字エンコーディングや言語固有の検索動作に影響する可能性のあるロケール識別子（例: `"en-US"`）。                                      |
| **password**     | 文字列 | クエリ   | _(オプション)_ 保護されたワークブックを開くためのパスワード。                                                                                       |

### レスポンス

正常なレスポンスの例として、操作のステータスと実行された置換数が返されます：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### エラーコード

- **400 Bad Request（不正なリクエスト）** – 無効な Aspose.Cells Cloud API URI。
- **401 Unauthorized（認証されていない）** – OAuth 2.0 アクセストークンが不足している、または無効です。
- **404 Not Found（見つかりません）** – 指定されたスプレッドシートファイルにアクセスできませんでした。
- **500 Server Error（サーバーエラー）** – リクエスト処理中に予期せぬサーバー側の問題が発生しました。

## リモートスプレッドシートのコンテンツ置換 API を使用するタイミング

- **バッチクラウドファイル更新** – AWS S3 や Azure Blob などのクラウドストレージに保存された複数の Excel ファイルの内容を一括で変更します。
- **クラウドテンプレートの動的埋め込み** – クラウド上に保存されたレポートテンプレートに最新のデータを動的に入力します。
- **クロスリージョンファイル同期** – 異なる地理的リージョンにまたがる Excel ファイルの内容を一貫して保ちます。

## リモートスプレッドシートのコンテンツ置換 API を使用する理由

- **開発者フレンドリー** – Aspose.Cells Cloud は多数のプログラミング言語向けの SDK ライブラリを提供しており、カスタムソリューションを構築する場合と比べて開発工数を大幅に削減できます。
- **人件費削減** – ドキュメントを手動で統合するための専任スタッフの必要性を排除します。
- **従量課金制** – 前払い投資は不要で、実際に実行した API コールのみに課金されます。
- **メンテナンス不要** – サーバーの管理やソフトウェアの更新、互換性の問題が一切不要です。
- **セルの書式、数式、チャートをすべて保持** – テキスト置換後も、元のワークブックのレイアウトや計算結果をそのまま維持します。

## SDK を使用してリモートスプレッドシートのコンテンツ置換 API を利用する方法

### OpenAPI スペック

[OpenAPI スペック](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できます。

### Aspose.Cells Cloud SDK の利用

SDK を使用することで、開発を最適化できます。SDK は内部の詳細処理を自動で処理するため、スプレッドシートのコンテンツ置換機能を最小限のコードで実装できます。Aspose.Cells Cloud SDK の完全な一覧については [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：


---