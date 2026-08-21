---
title: "ピボットテーブルのスタイルを更新する"
second_title: "Document"
linktitle: "すべてをフォーマット"
type: docs
url: /ja/pivot-tables/format-all/
aliases: [  /ja/update-style-for-pivot-table/ ]
keywords: "ピボットテーブル、スタイルの更新、Aspose.Cells Cloud、REST API、Excel、スプレッドシート、API、ピボットテーブルのスタイル、すべてをフォーマット"
description: "Aspose.Cells Cloud REST API を使用して、ピボットテーブル全体のスタイルを更新する方法を学びます。リクエストの詳細、cURL の例、複数のプログラミング言語向けの SDK スニペットを含みます。"
weight: 100
ArticleTitle: "ピボットテーブルのスタイルを更新する - Aspose.Cells Cloud API"
---

この REST API は、ピボットテーブルのスタイルを更新します。

## PostPivotTableStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**前提条件 / 認証**  
`Authorization` ヘッダーに有効な JWT アクセストークン（例：`Bearer <jwt token>`）を指定する必要があります。トークンには、指定されたワークブックおよびワークシートにアクセスする権限があることを確認してください。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### **リクエストパラメーター**

| パラメーター名     | 型       | 位置   | 説明                                                                                      |
| ------------------ | -------- | ------ | ----------------------------------------------------------------------------------------- |
| name               | 文字列   | パス   | ワークブックファイルの名前。                                                              |
| sheetName          | 文字列   | パス   | ピボットテーブルを含むワークシート。                                                      |
| pivotTableIndex    | 整数     | パス   | フォーマット対象のピボットテーブルの 0 から始まるインデックス。                           |
| style              | オブジェクト | 本文 | 適用するフォーマットを定義するスタイル DTO。                                              |
| needReCalculate    | 真偽値   | クエリ | フォーマット後にピボットテーブルを再計算する場合は **true** を設定します。デフォルトは **false** です。 |
| folder             | 文字列   | クエリ | ワークブックが保存されているフォルダー。                                                  |
| storageName        | 文字列   | クエリ | ストレージサービスの名前。                                                                |

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
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

**HTTP ステータスコード**

| コード | 意味                           | 説明                                                             |
| ------ | ------------------------------ | ---------------------------------------------------------------- |
| 200    | OK                             | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request                    | パラメーターが不足しているか無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                   | JWT トークンが無効または不足しています。                           |
| 413    | Payload Too Large              | アップロードされたファイルがサイズ制限を超えています。             |
| 500    | Internal Server Error          | サーバー側で予期しないエラーが発生しました。                       |

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用すると、API に対する開発を最速で行えます。SDK は低レベルの詳細を抽象化するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリー</a>をご覧ください。

以下のコード例は、Go SDK を使用して API を呼び出す方法を示しています。

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
---