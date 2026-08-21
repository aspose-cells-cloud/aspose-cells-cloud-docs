---
title: "Excelワークシートにワークシート検証を追加する"
second_title: "Document"
linktitle: "Add"
type: docs
url: /ja/validations/add/
keywords: "ワークシート検証の追加, Excel, Aspose.Cells Cloud, REST API, スプレッドシート, 検証ルール"
description: "Aspose.Cells Cloud REST APIを使用してExcelファイルにワークシート検証を追加します。SDKはC#、Java、PHP、Ruby、Node.js、Python、Perl、Go、およびSwiftで利用可能です。"
weight: 10
---

このREST APIは、Excelワークシートにワークシート検証を追加します。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **リクエストパラメーター**

| パラメーター名 | 型     | 位置   | 説明                                                   |
| -------------- | ------ | ------ | ------------------------------------------------------ |
| name           | string | path   | Excelドキュメントの名前。                              |
| sheetName      | string | path   | ワークシートの名前。                                   |
| range          | string | query  | 検証を適用するセル範囲（例：A1:B10）。                |
| validation     | object | body   | 検証ルールの定義。                                     |
| folder         | string | query  | ドキュメントを含むフォルダー。                         |
| storageName    | string | query  | ストレージサービスの名前。                             |

[OpenAPI仕様書](https://apireference.aspose.cloud/cells/#/WorksheetValidations/PutWorksheetValidation)は、公開可能なプログラミングインタフェースを定義し、ウェブブラウザから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用して、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLを使用してCloud APIへの呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X PUT \
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

## Cloud SDKファミリー

SDKを使用することが開発を最適化する最良の方法です。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストは[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}