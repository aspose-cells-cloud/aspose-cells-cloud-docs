---
title: "ListObject から重複行を削除する – Aspose.Cells Cloud API ドキュメント"
second_title: "ドキュメント"
linktitle: "重複の削除"
type: docs
keywords: "重複の削除、ListObject、Aspose.Cells Cloud API、Excel、REST"
url: /list-objects/remove-duplicates/
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のListObjectから重複行を削除する方法を学びます。エンドポイント、パラメータ、認証、およびサンプルのリクエストとレスポンスを含みます。"
weight: 20
---

この REST API は、Excelワークシート内の **ListObject** から重複行を削除します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates
```

### **リクエストパラメータ**

| パラメータ名        | 型      | 位置   | 説明                                                     |
| ------------------- | ------- | ------ | -------------------------------------------------------- |
| **name**            | 文字列  | パス   | Excelファイルの名前。                                   |
| **sheetName**       | 文字列  | パス   | ListObject を含むワークシートの名前。                  |
| **listObjectIndex** | 整数    | パス   | 処理するListObjectの0から始まるインデックス。          |
| **folder**          | 文字列  | クエリ | (オプション) ファイルが格納されているフォルダパス。     |
| **storageName**     | 文字列  | クエリ | (オプション) ストレージサービスの名前。                 |

### サンプルリクエスト (cURL)

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
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
  "Status": "OK",
  "DuplicateRowsRemoved": 12,
  "Message": "重複行が正常に削除されました。"
}
```

{{< /tab >}}
{{< /tabs >}}

### レスポンス

成功した場合、サービスは上記の例と同様の JSON オブジェクトを返します。フィールドは以下の通りです：

- **Code** – HTTP ステータスコード（成功時は `200`）。
- **Status** – ステータスのテキストによる説明。
- **DuplicateRowsRemoved** – 削除された行数。
- **Message** – 処理に関する追加情報。

**HTTP ステータスコード**

| コード | 意味           | 説明                                                  |
|------|----------------|-------------------------------------------------------|
| 200  | OK             | フィルターが正常に適用され、レスポンスに処理内容が含まれます。 |
| 400  | Bad Request    | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized   | JWT トークンが無効または不足しています。               |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | サーバーで予期しないエラーが発生しました。            |

## Cloud SDK Family

SDK を使用すると、開発を最適化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、GitHub リポジトリを確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectRemoveDuplicates.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectRemoveDuplicates.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectRemoveDuplicates.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectRemoveDuplicates.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectRemoveDuplicates.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectRemoveDuplicates.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectRemoveDuplicates.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectRemoveDuplicates.go" >}}

{{< /tab >}}

{{< /tabs >}}