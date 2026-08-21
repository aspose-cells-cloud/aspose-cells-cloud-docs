---
title: "ピボットテーブルのセルスタイルの更新"
second_title: "Document"
linktype: "書式設定"
type: docs
url: "/pivot-tables/format/"
aliases: [/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, ピボットテーブル スタイル, セルスタイル更新 API, REST API, Excel API, スプレッドシート書式設定, クラウド SDK, セルスタイル, ピボットテーブル"
description: "Aspose.Cells Cloud の REST API を使って、ピボットテーブル内の特定のセルのスタイルを更新する方法を学習します。エンドポイント、パラメータ、認証、cURL の例、Go SDK のコードスニペット、SEO 最適化されたガイドを含みます。"
weight: 90
ArticleTitle: "ピボットテーブルのセルスタイルの更新 - Aspose.Cells Cloud API ドキュメント"
---

この REST API は、ピボットテーブル内のセルの**スタイル**を更新します。

**前提条件 / 認証**  
このエンドポイントを呼び出すには、有効な Aspose Cloud JWT アクセストークンが必要です。OAuth 2.0 フローを使用してトークンを取得し、[認証ガイド](/authentication/)に従ってください。リクエストヘッダーにトークンを含めてください：

```http
Authorization: Bearer <jwt token>
```

JWT トークンは、すべての Aspose.Cells Cloud API の呼び出しに必要です。

## PostPivotTableCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### **リクエストパラメータ**

| パラメータ名       | タイプ    | 位置   | 説明                                                                                               |
| ------------------ | --------- | ------ | --------------------------------------------------------------------------------------------------- |
| name               | 文字列    | パス   | ドキュメント名（必須）。                                                                            |
| sheetName          | 文字列    | パス   | シート名（必須）。                                                                                  |
| pivotTableIndex    | 整数      | パス   | ピボットテーブルのインデックス（必須）。                                                            |
| column             | 整数      | クエリ | スタイルを適用するセルの 0 から始まる列インデックス（必須）。                                         |
| row                | 整数      | クエリ | スタイルを適用するセルの 0 から始まる行インデックス（必須）。                                         |
| style              | オブジェクト | 本文   | 新しいセルスタイルを定義する Style DTO（データ転送オブジェクト）。                                  |
| needReCalculate    | 真偽値    | クエリ | スタイル適用後にピボットテーブルを再計算するかどうかを示します。既定値は **false** です。            |
| folder             | 文字列    | クエリ | ドキュメントが保存されているフォルダー（オプション）。                                              |
| storageName        | 文字列    | クエリ | ストレージの名前（オプション）。                                                                    |
| Method             | 文字列    | N/A    | リクエストに使用される HTTP メソッド (**POST**)。                                                  |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**レスポンス**  
成功すると、サービスは空のボディと共に HTTP 200 を返し、スタイルが適用されたことを示します。エラーが発生した場合は、エラーコードとメッセージを含む JSON ペイロードが返されます。

| HTTP ステータス | 説明                                                                 |
|-----------------|----------------------------------------------------------------------|
| 200             | スタイルが正常に適用されました。                                     |
| 400             | 不正なリクエスト（例：無効な列/行インデックスなど）。                |
| 401             | 認証エラー（JWT トークンが不足している、または無効です）。           |
| 404             | 要求されたドキュメント、シート、またはピボットテーブルが存在しません。 |
| 500             | サーバー内部エラー（予期しない条件）。                               |

成功時のレスポンスボディは空です。

詳細については、**Get Pivot Table** API のドキュメントをご参照ください。

## クラウド SDK ファミリー

SDK を使用すると、開発が最も迅速になります。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、**Go** SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "ピボットテーブルのセルスタイルの更新",
  "description": "Aspose.Cells Cloud ピボットテーブルの特定のセルのスタイルを REST API で更新するためのガイド。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, ピボットテーブル, セルスタイル, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>