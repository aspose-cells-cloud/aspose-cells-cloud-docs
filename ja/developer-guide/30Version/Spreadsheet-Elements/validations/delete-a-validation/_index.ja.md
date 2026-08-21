---
title: "ワークシート検証の削除 – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktitle: "削除"
type: docs
url: /ja/validations/delete/
keywords: "削除, ワークシート検証, Aspose.Cells Cloud, Excel API"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイルからワークシート検証を削除する方法を学びます。エンドポイント、パラメータ、認証詳細、cURL の使用例、エラーハンドリング、および SDK のコードスニペットが含まれます。"
weight: 10
---

この REST API は、Excel ワークシート上のゼロベースのインデックスによってワークシート検証を削除します。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **リクエストパラメータ**

| パラメータ名         | タイプ    | 位置   | 説明                                   |
| -------------------- | --------- | ------ | ---------------------------------------- |
| name                 | 文字列    | パス   | Excel ファイルの名前。                   |
| sheetName            | 文字列    | パス   | ワークシートの名前。                     |
| validationIndex      | 整数      | パス   | 削除する検証のゼロベースインデックス。   |
| folder               | 文字列    | クエリ | ドキュメントを含むフォルダ。             |
| storageName          | 文字列    | クエリ | ストレージサービスの名前。               |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスを呼び出すことができます。以下の例は、cURL を使用して検証を削除する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**HTTP ステータスコード**

| コード | 意味                     | 説明                                      |
|--------|--------------------------|-------------------------------------------|
| 200    | OK                       | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request              | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized             | JWT トークンが無効または不足しています。     |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error    | 予期しないサーバーエラーが発生しました。     |

## Cloud SDK Family

SDK を使用すると、この操作をアプリケーションに統合する最も速い方法です。SDK は低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用してワークシート検証を削除する方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}