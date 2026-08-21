---
title: "水平改ページの削除"
ArticleTitle: "Aspose.Cells Cloud – 水平改ページの削除（REST API）"
second_title: "ドキュメント"
linktitle: "水平改ページの削除"
type: docs
url: /page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, 水平改ページの削除, Excelワークシート, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートから水平改ページを削除します。C#、Java、PHP、Ruby、Node.js、Python、Perl、Go 向けの SDK が利用可能です。"
weight: 50
---

この REST API は、**水平**改ページを削除します。

**前提条件**：このエンドポイントを呼び出すには、有効な Aspose Cloud JWT アクセストークンが必要です。[認証ガイド](https://docs.aspose.cloud/cells/authentication/)に従って取得してください。

## DeleteHorizontalPageBreak API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*すべての API 呼び出しは **HTTPS** 経由で行う必要があります。*

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### リクエストパラメータ

| パラメータ名     | 型       | 位置   | 説明                                                       |
| ---------------- | -------- | ------ | ---------------------------------------------------------- |
| `name`           | 文字列   | パス   | Excel ファイル（ワークブック）の名前。                     |
| `sheetName`      | 文字列   | パス   | 改ページを含むワークシートの名前。                         |
| `index`          | 整数     | パス   | 削除する水平改ページの 0 から始まるインデックス。          |
| `folder`         | 文字列   | クエリ | オプション：ファイルが存在するストレージ内のフォルダーパス。 |
| `storageName`    | 文字列   | クエリ | オプション：ストレージサービスの名前。                     |

### エラーレスポンス

| HTTP コード | 説明                                                                      |
| ----------- | ------------------------------------------------------------------------- |
| 401         | 認証エラー：トークンが不足しているか、無効です。                          |
| 404         | 見つかりません：指定されたファイル、ワークシート、または改ページインデックスが存在しません。 |
| 400         | 不正リクエスト：リクエスト構文が不正、またはパラメータが無効です。        |
| 500         | サーバーエラー：予期しない状態が発生しました。                            |

**関連項目:**  
- [水平改ページの追加](/page-breaks/add-horizontal-page-break/)  
- [水平改ページの取得](/page-breaks/get-horizontal-page-breaks/)  
- [垂直改ページの削除](/page-breaks/delete-vertical-page-break/)

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak)はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してこの API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
  -X DELETE \
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

**レスポンススキーマ**

| フィールド | 型     | 説明                                 |
|-----------|--------|--------------------------------------|
| Code      | 整数   | HTTP ステータスコード（例: 200）。   |
| Status    | 文字列 | ステータスのテキストメッセージ（例: "OK"）。 |
| Message   | 文字列 | オプション：エラー発生時の追加情報。 |

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細な処理を自動で行い、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d) で表示してください。*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f) で表示してください。*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152) で表示してください。*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca) で表示してください。*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0) で表示してください。*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1) で表示してください。*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca) で表示してください。*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*例が読み込まれない場合は、[GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185) で表示してください。*

{{< /tab >}}

{{< /tabs >}}