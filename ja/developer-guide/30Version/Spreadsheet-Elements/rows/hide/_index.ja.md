---
title: "Excelワークシートの行を非表示にする"
second_title: "Document"
linktitle: "Hide"
type: docs
url: /ja/rows/hide/
aliases: [  /ja/hide-rows-in-excel-worksheet/ ]
keywords: "行を非表示にする, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートの1行または複数行を非表示にする方法を学びます。cURL の例、SDK スニペット、パラメータ、認証、レスポンス詳細、エラーハンドリングを含みます。"
weight: 40
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートの行を非表示にする"
---

この REST API は、Excel ワークシート上の行を非表示にします。

**前提条件:** Aspose Cloud OAuth エンドポイントから取得した有効な JWT Bearer トークン、Aspose Cloud ストレージに保存されたワークブック、および非表示にする行を含むワークシートの名前。この API は、XLS、XLSX など、サポートされる形式の Excel ファイルで動作します。

## PostHideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### リクエストパラメータ

| パラメータ名      | 型      | 位置   | 説明                                                         |
| ---------------- | ------- | ------ | ------------------------------------------------------------ |
| **name**         | 文字列  | パス   | ワークブックファイルの名前。                                  |
| **sheetName**    | 文字列  | パス   | 非表示にする行を含むワークシートの名前。                      |
| **startrow**     | 整数    | クエリ | 非表示にする最初の行の 0 から始まるインデックス。             |
| **totalRows**    | 整数    | クエリ | **startrow** から始まる連続して非表示にする行数。             |
| **folder**       | 文字列  | クエリ | ワークブックが配置されているストレージ内のフォルダ。         |
| **storageName**  | 文字列  | クエリ | ストレージサービスの名前。                                    |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) は、パブリックにアクセス可能なプログラミングインタフェースを提供し、Web ブラウザから直接 REST 通信を実行できるようにしています。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスを呼び出すことができます。API は Aspose Cloud OAuth エンドポイントから取得した JWT Bearer トークンを必要とし、それを `Authorization` ヘッダーに含める必要があります。以下の例は、cURL を使用して行を非表示にする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
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

**レスポンスステータスコード**

| コード | 説明                         |
|------|------------------------------|
| 200  | 成功 – 行が非表示にされた     |
| 400  | 不正なリクエスト – 無効なパラメータ |
| 401  | 認証エラー – JWT が欠如または無効 |
| 404  | 見つからない – ワークブックまたはワークシートが存在しない |
| 500  | サーバーエラー – 内部処理失敗 |

正常な呼び出しは、`Code` と `Status` フィールドを含む JSON オブジェクトを返します。エラー発生時は、`Message` などの追加フィールドと適切な HTTP ステータスコード（例：400、401、404、500）がレスポンスに含まれます。

**注意:** `startrow` の値がワークシートの行範囲内にあることを確認してください。そうでない場合、API は 400 エラーを返します。行インデックスは 0 から始まるため、`startrow=0` は最初の行を指します。

## Cloud SDK ファミリー

SDK を使用すると、この機能をアプリケーションに統合する最も早い方法です。SDK は低レベルの詳細を処理するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、 various SDK を使用して行を非表示にする方法を示しています。（ファイル名は「Unhide」を参照していますが、これは過去の命名規則によるものであり、各 gist 内のコードは **Hide** 操作を実行します。）

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}