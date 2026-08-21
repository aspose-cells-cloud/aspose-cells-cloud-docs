---
title: "Excel ワークブックの名前付き範囲を取得する"
second_title: "Document"
linktitle: "Name"
type: docs
url: /ja/ranges/get/name/
aliases: [  /ja/get-named-ranges-inside-the-workbook/ ]
keywords: "名前付き範囲, Excel, Aspose.Cells, Cloud API, ワークシート"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブック内の名前付き範囲を取得します。リクエストの詳細、cURL コマンドのサンプル、および複数のプログラミング言語向けの SDK サンプルを含みます。"
ArticleTitle: "Excel ワークブックの名前付き範囲を取得する – Aspose.Cells Cloud API"
weight: 10
---

この REST API は、ワークシート内に定義された名前付き範囲に関する情報を返します。

**背景** – *名前付き範囲* とは、ワークシート内の特定のセルまたはセル範囲を参照するユーザー定義の識別子です。名前付き範囲を使用すると、数式の作成が簡略化され、可読性が向上し、頻繁に使用するワークブックの範囲へのプログラムによるアクセスが可能になります。

**前提条件** – Aspose.Cells Cloud API にアクセスするには、有効な JWT アクセストークンが必要です。Aspose Cloud のクライアント ID とクライアントシークレットを使用して OAuth 2.0 トークンエンドポイントで認証し、トークンを取得してください。取得したトークンは、すべてのリクエストの `Authorization: Bearer <jwt token>` ヘッダーに含めて送信してください。

## GetNamedRanges API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置         | 説明                                     |
| ------------ | ------ | ------------ | ----------------------------------------- |
| name         | 文字列 | パス         | Excel ドキュメントの名前。               |
| folder       | 文字列 | クエリ文字列 | ドキュメントを含むフォルダ。             |
| storageName  | 文字列 | クエリ文字列 | ドキュメントが配置されているストレージ名。|

**HTTP ステータスコード**

| コード | 意味              | 説明                                           |
|------|-------------------|------------------------------------------------|
| 200  | OK                | フィルターの適用に成功。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request       | パラメータが不足している、または無効（例：サポートされていないファイル形式）です。 |
| 401  | Unauthorized      | JWT トークンが無効または不足しています。        |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | サーバーで予期せぬエラーが発生しました。        |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) は、パブリックに利用可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 操作を実行できます。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスを呼び出すことができます。以下の例では、cURL を使用して名前付き範囲を取得する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**レスポンスモデル**

| フィールド名      | 型      | 説明                                               |
|------------------|---------|----------------------------------------------------|
| `ColumnCount`    | 整数    | 範囲内の列数。                                      |
| `ColumnWidth`    | 数値    | 各列の幅（ポイント単位）。                          |
| `FirstColumn`    | 整数    | 範囲内の最初の列の 0 から始まるインデックス。       |
| `FirstRow`       | 整数    | 範囲内の最初の行の 0 から始まるインデックス。       |
| `Name`           | 文字列  | 範囲のユーザー定義名。                              |
| `RefersTo`       | 文字列  | セル参照を定義する数式（例：`=Sheet1!$B$10:$H$10`）。|
| `RowCount`       | 整数    | 範囲内の行数。                                      |
| `RowHeight`      | 数値    | 各行の高さ（ポイント単位）。                        |
| `Worksheet`      | 文字列  | 範囲を含むワークシートの名前。                      |

## Cloud SDK ファミリー

SDK を使用すると、この機能を最速で統合できます。SDK は低レベルの詳細を処理するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}