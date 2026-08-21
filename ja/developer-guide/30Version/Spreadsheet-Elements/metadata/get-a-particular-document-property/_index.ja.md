---
title: "特定のドキュメント プロパティを取得する"
second_title: "ドキュメント"
linktitle: "取得"
type: docs
url: /document-properties/get/
aliases: [/get-a-particular-document-property/]
keywords: "Aspose.Cells, Cloud API, Get Document Property, Excel metadata, REST GET, SDK examples"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイルから名前付きドキュメント プロパティ（例：Author、Title）を取得します。cURL の例、SDK スニペット、レスポンス スキーマを含みます。"
weight: 20
---

この REST API は、名前でドキュメント プロパティを読み取ります。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### リクエスト パラメータ

| パラメータ名       | タイプ   | 位置   | 説明                                        |
| ------------------ | -------- | ------ | --------------------------------------------- |
| name               | string   | path   | Excel ファイルの名前。                        |
| propertyName       | string   | path   | 取得するドキュメント プロパティの名前。       |
| folder             | string   | query  | ファイルを含むフォルダ（オプション）。         |
| storageName        | string   | query  | ストレージ名（オプション）。                   |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) は公開可能なプログラミング インターフェースを定義し、Web ブラウザから直接 REST によるやり取りを実行できるようにします。

**cURL コマンドライン ツール** を使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### レスポンスの詳細

API が返す JSON オブジェクトには、以下のフィールドが含まれます：

| フィールド                       | タイプ    | 説明                                                      |
| ------------------------------- | --------- | ----------------------------------------------------------- |
| **DocumentProperty.Name**       | string    | プロパティの名前（例：`Author`）。                          |
| **DocumentProperty.Value**      | string    | プロパティの値。設定されていない場合は空になることがあります。 |
| **DocumentProperty.BuiltIn**    | boolean   | プロパティが組み込みの Excel プロパティかどうかを示します。  |
| **DocumentProperty.link.Href**  | string    | プロパティ リソースへの相対 URL。                           |
| **DocumentProperty.link.Rel**   | string    | リレーションタイプ。通常は `self`。                         |
| **DocumentProperty.link.Title** | string    | 人間が読めるタイトル（`null` の場合があります）。            |
| **DocumentProperty.link.Type**  | string    | リンクされたリソースの MIME タイプ（`null` の場合があります）。|
| **Code**                        | integer   | サービスが返す HTTP ステータス コード。                      |
| **Status**                      | string    | ステータスのテキストによる説明（例：`OK`）。                 |

### エラー レスポンス

| HTTP ステータス | コード                   | 説明                                      |
| --------------- | ------------------------ | ------------------------------------------- |
| 400             | `InvalidParameter`       | 1 つ以上のリクエスト パラメータが無効です。  |
| 401             | `AuthenticationFailed`   | JWT トークンが不足しているか、無効です。      |
| 404             | `PropertyNotFound`       | 指定されたドキュメント プロパティが存在しません。 |
| 500             | `InternalError`          | サーバー上で予期しないエラーが発生しました。    |

典型的なエラー本文は以下のようになります：

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Cloud SDK Family

SDK を使用することが開発を高速化する最良の方法です。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスに呼び出しを行う方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 用語集

| 用語                  | 定義                                                                                   |
| --------------------- | ---------------------------------------------------------------------------------------- |
| **Document Property** | Excel ワークブックに関連付けられたメタデータの一部（例：Author、Title、Created など）。 |
| **Metadata**          | 他のデータを説明するデータの総称。この文脈ではドキュメント プロパティを指します。         |
| **Custom Property**   | 組み込みセットに含まれないユーザー定義のプロパティ。                                     |

### よくあるご質問

**Q:** _Excel ファイルの Author プロパティを Aspose Cloud に保存されたファイルから取得するにはどうすればよいですか？_  
**A:** 有効なベアラー トークンを使用して `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` に GET リクエストを送信します。レスポンス JSON には `DocumentProperty.Name = "Author"` およびその `Value` が含まれます。

**Q:** _リクエストされたプロパティが存在しない場合、どのようなエラーが返されますか？_  
**A:** API は HTTP 404 を返し、JSON 本文に `Code: 404` および `Status: "Property not found"` を含めます。

**Q:** _ファイルがデフォルト ストレージにある場合、`storageName` を指定する必要がありますか？_  
**A:** いいえ。`storageName` クエリ パラメータはオプションです。アカウントに設定されたデフォルト ストレージを使用するには、指定を省略してください。