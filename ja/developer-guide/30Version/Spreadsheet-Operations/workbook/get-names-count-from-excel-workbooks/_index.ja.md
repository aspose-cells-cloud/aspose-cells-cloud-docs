---
title: "Excel ワークブックから名前を取得する"
second_title: "Document"
linktitle: "Names"
type: docs
url: /ja/get-names-from-an-excel-file/
aliases:
  [
    /get-names-count-from-excel-workbooks/,
    /workbook/names/,
    /workbook/get/names/,
  ]
keywords: "Aspose.Cells, クラウド, Excel, Workbook, 名前, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックから定義済み名前をすべて取得します。認証ガイド、cURL の例、応答スキーマ、エラーハンドリング、SDK サンプルを含みます。"
weight: 120
ArticleTitle: "Excel ワークブックから名前を取得する – Aspose.Cells Cloud API"
---

この REST API は、Excel ワークブックから定義済み名前を取得します。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

## GetWorkbookNames API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

リクエストパラメータは以下の通りです。

| パラメータ名 | 型     | 位置   | 説明                       |
| ------------ | ------ | ------ | --------------------------- |
| name         | string | path   | ワークブックファイル名       |
| folder       | string | query  | ワークブックを含むフォルダ   |
| storageName  | string | query  | 使用するストレージの名前     |

リクエストには以下の HTTP ヘッダーを含める必要があります。

| ヘッダー        | 型     | 説明                                  |
|---------------|--------|---------------------------------------|
| Authorization | string | Bearer JWT トークン（必須）            |
| Accept        | string | `application/json`                    |
| Content-Type  | string | `application/json`（ボディを伴うリクエストの場合） |

**認証** – API は OAuth2/JWT ベアラートークンを必要とします。`https://api.aspose.cloud/connect/token` からクライアント ID およびクライアントシークレットを使用してトークンを取得し、各リクエストで `Authorization: Bearer <jwt token>` ヘッダーを含めてください。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 通信を実行できます。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスにアクセスできます。以下の例は、cURL を使用して Aspose.Cells Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_応答フィールド_

- **Status** _(string)_ – 処理のステータスメッセージ
- **Names.link** _(object)_ – コレクションのハイパーリンク情報
- **Names.Count** _(integer)_ – 返された定義済み名前の合計数
- **Names.NameList** _(array)_ – 名前オブジェクトのリスト。各オブジェクトはナビゲーション情報を持つ **link** オブジェクトを含む

**エラーハンドリング** – サービスは以下の HTTP ステータスコードを返す可能性があります。

| コード | 意味                 | 推奨アクション                                             |
| ------ | -------------------- | ---------------------------------------------------------- |
| 401    | 認証されていません   | 有効な JWT トークンが提供されていることを確認してください   |
| 404    | 見つかりません       | ワークブック名、フォルダ、ストレージが正しいことを確認してください |
| 500    | サーバー内部エラー   | 後でもう一度試すか、問題が続く場合は Aspose サポートにお問い合わせください |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}