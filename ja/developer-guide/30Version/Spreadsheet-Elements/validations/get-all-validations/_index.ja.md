---
title: "Excelワークシートからすべての検証ルールを取得する"
second_title: "Document"
linktitle: "すべて取得"
type: docs
url: /ja/validations/get-all/
keywords: "Aspose.Cells Cloud, Excel, ワークシート検証, REST API, すべての検証を取得, SDK"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシートからすべてのワークシート検証を取得します。複数のSDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go）をサポートし、迅速な統合を実現します。"
weight: 10
---

ワークシート検証では、セルに入力できるデータのタイプや範囲を制限するルールを定義できます。これらは主にデータの整合性を保つために使用され、例えば、入力を特定の値のリスト、特定の範囲内の日付、または数値の制限に限定するなどの用途があります。

このREST APIは、Excelワークシート上のすべてのワークシート検証を取得します。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **リクエストパラメータ**

| パラメータ名 | 型     | 位置   | 説明                               |
| ------------ | ------ | ------ | ----------------------------------- |
| name         | string | path   | Excelドキュメントの名前です。       |
| sheetName    | string | path   | ワークシートの名前です。            |
| folder       | string | query  | ドキュメントが保存されているフォルダのパスです。 |
| storageName  | string | query  | ストレージサービスの名前です。      |

**レスポンスステータスコード**

| コード | 説明                                     |
|------|------------------------------------------|
| 200  | 成功：検証のリストを返します。           |
| 401  | 認証エラー：無効または不足しているトークン |
| 404  | 見つかりません：ドキュメントまたはワークシートが存在しません |
| 500  | サーバー内部エラー                       |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations)はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST APIとのやり取りを実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cells Cloudウェブサービスに簡単にアクセスできます。**前提条件：** `Authorization` ヘッダーに有効なJWTトークンを含める必要があります。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "値は1から100の間である必要があります。"
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "リストから値を選択してください。"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウドSDKファミリー

SDKを使用することが開発を迅速化する最良の方法です。SDKは低レベルの詳細な処理を処理してくれるため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストは[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}
---