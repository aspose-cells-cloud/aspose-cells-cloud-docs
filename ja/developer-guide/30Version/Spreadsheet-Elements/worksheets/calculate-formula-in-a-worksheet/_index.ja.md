---
title: "Excelワークシートで数式を計算する"
second_title: "Document"
linktitle: "Calculate"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, 数式の計算, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内の数式を計算します。複数の SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go、Swift）をサポートし、すぐに利用可能なサンプルを提供します。"
weight: 20
ArticleTitle: "Excelワークシートで数式を計算する – Aspose.Cells Cloud ドキュメント"
---

この REST API は、ワークシート内の**数式の計算結果**を返します。アプリケーションから直接**Excel 数式を評価**するために使用できます。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **リクエストパラメーター**

| パラメーター名 | 型     | 位置   | 説明                                       |
| -------------- | ------ | ------ | ------------------------------------------ |
| name           | string | path   | Excel ファイルの名前。                    |
| sheetName      | string | path   | 数式を含むワークシートの名前。            |
| formula        | string | query  | 評価する数式（例: `SUM(A5:A10)`）。       |
| folder         | string | query  | ドキュメントが保存されているフォルダー。  |
| storageName    | string | query  | ストレージサービスの名前（該当する場合）。|

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) は公開可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できます。

### 認証

すべてのリクエストは `Authorization` ヘッダーに有効な**Bearer JWT トークン**を含める必要があります：

```
Authorization: Bearer <your_jwt_token>
```

トークンの取得については、Aspose.Cells Cloud 認証ガイドで説明されている OAuth 2.0 フローに従ってください。

### Possible response status codes（可能なレスポンスステータスコード）

| コード | 説明                                                  |
|------|-------------------------------------------------------|
| 200  | リクエスト成功；数式の値が返されます。                     |
| 400  | 不正なリクエスト；パラメーターが不足または無効です。          |
| 401  | 認証されていない；JWT トークンが無効または不足しています。     |
| 404  | 見つからない；指定されたファイルまたはワークシートが存在しません。 |
| 500  | サーバー内部エラー；サーバー上で予期せぬ状態が発生しました。   |

**cURL** コマンドラインツールを使用して Aspose.Cells Cloud Web サービスを簡単に呼び出すことができます。以下の例では、cURL を使用して数式の結果をリクエストする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用すると、API の統合が最速で行えます。SDK が低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**関連項目:**  
- [ワークシートの取得](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [ワークシートの更新](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [すべての数式を計算](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---