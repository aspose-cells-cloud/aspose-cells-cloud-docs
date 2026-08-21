---
title: "チャートのカテゴリ軸を取得する"
type: docs
url: /ja/charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, チャートのカテゴリ軸, Excel, REST API, クラウドストレージ, OAuth2, APIドキュメント"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のチャートのカテゴリ軸を取得します。"
ArticleTitle: "チャートのカテゴリ軸を取得する – Aspose.Cells Cloud API ドキュメント"
---

この REST API は、チャートの**カテゴリ軸**を取得します。  
このエンドポイントを呼び出すには、有効な OAuth 2.0 アクセストークンを提供する必要があり、ワークブックは Aspose Cloud ストレージ内に保存されている必要があります。

**前提条件**  
このエンドポイントを使用する前に、以下の条件を満たしていることを確認してください。  

- OAuth 2.0 トークンが取得されており、Aspose Cloud サービスで有効であること。  
- ワークブックファイルが Aspose Cloud ストレージ（デフォルトまたは指定されたフォルダ）にアップロードされていること。  
- リクエスト URL に示されているように、API バージョン **v3.0** を使用していること。  
- 呼び出し元のアプリケーションがワークブックを読み取り、そのワークシートにアクセスする権限を持っていること。

## GetChartCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**背景** – ワークシートからすべてのチャートを削除することは、シートのビジュアルレイアウトをリセットしたり、古いビジュアライゼーションを置き換えたり、以前のチャートデータを保持せずにワークブックを再利用できるように準備したりする必要がある場合に便利です。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型      | 位置   | 説明                                               |
| ------------ | ------- | ------ | -------------------------------------------------- |
| name         | string  | path   | ワークブックファイルの名前。                       |
| sheetName    | string  | path   | チャートを含むワークシートの名前。                 |
| chartIndex   | integer | path   | 軸を要求するチャートの 0 から始まるインデックス。  |
| folder       | string  | query  | ワークブックが存在するストレージ内のフォルダパス。 |
| storageName  | string  | query  | ストレージサービスの名前（デフォルトでない場合）。  |

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**HTTP ステータスコード**

| コード | 意味                          | 説明                                             |
| ------ | ----------------------------- | ------------------------------------------------ |
| 200    | OK                            | フィルターが正常に適用された；レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request                   | パラメータが不足している、または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                  | JWT トークンが無効または不足している。           |
| 413    | Payload Too Large             | アップロードされたファイルがサイズ制限を超えた。 |
| 500    | Internal Server Error         | 予期しないサーバーエラー。                       |

## SDK を使用した GetChartCategoryAxis API の利用方法

### GetChartCategoryAxis API 仕様

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">OpenAPI 仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
-X GET \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go の例のプレースホルダー -->

{{< /tab >}}

{{< /tabs >}}
---