---
title: "Excelワークシートの検証ルールを更新する"
second_title: "ドキュメント"
linktitle: "更新"
type: docs
url: /validations/update/
keywords: "Aspose.Cells Cloud, Excel 検証ルールの更新, REST API, ワークシート検証ルール, Excel API"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイル内のワークシート検証ルールを更新する方法。cURL の例および複数のプログラミング言語向けの SDK コードスニペットを含みます。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API を使用してワークシート検証ルールを更新する"
---

この REST API は、Excel ワークシート上の指定されたインデックスを持つ検証ルールを更新します。

このエンドポイントを呼び出す前に、適切なスコープ（例：`Cells.ReadWrite`）で JWT アクセストークンを取得し、以下の例のように `Authorization` ヘッダーにトークンを含めてください。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **リクエストパラメーター**

| パラメーター名    | 型      | 位置   | 説明                                                       |
| ----------------- | ------- | ------ | ---------------------------------------------------------- |
| name              | string  | path   | ワークブックファイルの名前。                               |
| sheetName         | string  | path   | 検証ルールを含むワークシートの名前。                       |
| validationIndex   | integer | path   | 更新対象の検証ルールの 0 から始まるインデックス。          |
| validation        | object  | body   | 更新後の検証ルール設定を定義する JSON オブジェクト。       |
| folder            | string  | query  | ワークブックが存在するクラウドストレージ内のフォルダー。   |
| storageName       | string  | query  | 使用するストレージサービスの名前（カスタムストレージ使用時）。 |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">OpenAPI スペック</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できます。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスを簡単に呼び出せます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**返される可能性のある HTTP ステータスコード**

| コード | 意味                                     | 説明                                         |
| ------ | ---------------------------------------- | -------------------------------------------- |
| 200    | OK                                       | 検証ルールが正常に更新されました。           |
| 400    | Bad Request                              | リクエストが不正な形式、または必須パラメーターが不足しています。 |
| 401    | Unauthorized                             | JWT トークンが無効、または不足しています。   |
| 403    | Forbidden                                | トークンに十分なスコープがありません。       |
| 404    | Not Found                                | 指定されたワークブック、ワークシート、または検証インデックスが存在しません。 |
| 500    | Internal Server Error                    | サーバー上で予期せぬエラーが発生しました。   |

エラー処理の詳細については、<a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud のエラードキュメント</a> を参照してください。

また、新しい検証ルールの追加や既存の検証ルールの削除など、関連する操作もご参照ください：

- [ワークシート検証ルールを追加する](https://docs.aspose.cloud/cells/validations/add/)
- [ワークシート検証ルールを削除する](https://docs.aspose.cloud/cells/validations/delete/)

## Cloud SDK ファミリー

SDK を使用すると、開発を最も迅速に進められます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、 various SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}