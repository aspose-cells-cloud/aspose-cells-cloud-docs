---
title: "チャートの数値軸を取得する"
type: docs
url: /ja/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells、チャートの数値軸、REST API、Excel、クラウド SDK、チャートの数値軸を取得する
description: "Aspose.Cells Cloud REST API - Excelワークシート内のチャートの数値軸を取得します。"
ArticleTitle: "チャートの数値軸を取得する - Aspose.Cells Cloud REST API"
---

この REST API は、チャートの数値軸を取得します。これは **Aspose.Cells Cloud REST API** の一部であり、クラウドに保存された Excel ワークシートを対象に動作します。

関連する操作については、**[チャートのカテゴリ軸を取得する](/charts/category-axis/get/)** エンドポイントをご参照ください。

## GetChartValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                                                |
| -------------- | ------ | ------ | --------------------------------------------------- |
| name           | string | path   | Excel ファイル名（拡張子を含む）。                 |
| sheetName      | string | path   | チャートを含むワークシート名。                     |
| chartIndex     | integer | path  | ワークシート内でのチャートの 0 から始まるインデックス。 |
| folder         | string | query  | ファイルが配置されているクラウドストレージ上のフォルダー。 |
| storageName    | string | query  | ストレージサービス名（例：Aspose Cloud）。          |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST による操作を実行できるようにしています。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
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
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Values",
    "Format": {
      "NumberFormat": "General",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**返される可能性のある HTTP ステータスコード**

| コード | 説明                                                       |
|------|------------------------------------------------------------|
| 200  | 成功 – 数値軸の情報が返されます。                           |
| 400  | 不正リクエスト – 必須パラメーターが不足しているか、無効です。 |
| 401  | 認証エラー – 認証トークンが不足しているか、無効です。        |
| 404  | 見つかりません – 指定されたワークブック、ワークシート、またはチャートが存在しません。 |
| 500  | サーバーエラー – サーバー上で予期しないエラーが発生しました。 |

レスポンスには、`Minimum`、`Maximum`、`MajorUnit`、`MinorUnit`、`Title`、`Format` などのプロパティを持つ詳細な `ValueAxis` オブジェクトが含まれます。完全な実装では、さらに多くのフォーマット詳細が提供される可能性があります。

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用することで、開発を最適化できます。SDK が低レベルの詳細を処理するため、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスにリクエストを行う方法を示しています。

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
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