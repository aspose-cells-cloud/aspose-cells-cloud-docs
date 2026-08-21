---
title: "Excelファイルの列を自動調整する"
second_title: "Document"
linktitle: "Columns"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    "/auto-fit-columns-in-excel-workbooks",
    "/autofit-columns-in-excel-workbooks/",
    "/columns/autofit/",
    "/workbook/autofit/columns/",
  ]
keywords: "列の自動調整, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックの列を自動調整する方法を学びます。リクエストの詳細、cURL の例、複数のプログラミング言語向けの SDK コードサンプルを含みます。"
weight: 90
---

この REST API は、Excel ワークブック内の列を自動調整することをサポートしています。

## PostAutofitWorkbookColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

リクエストパラメータは以下の通りです：

| パラメータ名          | 型      | 位置     | 説明                                           |
| --------------------- | ------- | -------- | ---------------------------------------------- |
| **name**              | 文字列  | パス     | ワークブックファイルの名前。                   |
| **autoFitterOptions** | オブジェクト | 本文     | 自動調整動作を制御するオプション。             |
| **startColumn**       | 整数    | クエリ   | 自動調整する最初の列の 0 から始まるインデックス。 |
| **endColumn**         | 整数    | クエリ   | 自動調整する最後の列の 0 から始まるインデックス。 |
| **folder**            | 文字列  | クエリ   | ワークブックが格納されているフォルダ。         |
| **storageName**       | 文字列  | クエリ   | ストレージサービスの名前。                     |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **注意:** 本番環境では常に HTTPS エンドポイントを使用し、JWT トークンを機密情報として扱ってください。

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

### 前提条件
この操作を呼び出す前に、有効な Aspose Cloud API キー、生成された JWT トークン、および対象のワークブックが指定されたストレージの場所に既に存在することを確認してください。

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                  | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                 | JWT トークンが無効または不足しています。          |
| 413  | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error        | 予期しないサーバーエラーが発生しました。          |

API は以下の HTTP ステータスコードを返すことができます：

| コード | 説明                         |
|------|------------------------------|
| 200  | 成功 – 列が自動調整されました |
| 400  | Bad request – パラメータが不足または無効です |
| 401  | Unauthorized – 無効または期限切れの JWT です |
| 500  | Server error – 内部処理に失敗しました |

## Cloud SDK Family

SDK を使用するのは、開発を最速で加速する最も効率的な方法です。SDK が低レベルの詳細を処理するため、プロジェクトのロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}