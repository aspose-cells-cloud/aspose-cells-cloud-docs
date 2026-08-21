---
title: "チャートの第2値軸を取得する"
type: docs
url: /ja/charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, チャートの第2値軸, Excel, REST API, クラウド, API, Excelチャート軸
description: Aspose.Cells Cloud REST API を使用して、Excelワークシート内の指定されたチャートの第2値軸を取得します。
ArticleTitle: "チャートの第2値軸を取得する – Aspose.Cells Cloud API"
---

この REST API は、チャートの第2値軸を取得します。

## GetChartSecondValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型      | 位置   | 説明                                       |
| ------------ | ------- | ------ | ------------------------------------------- |
| name         | string  | path   | Excel ファイルの名前。                      |
| sheetName    | string  | path   | チャートを含むワークシートの名前。          |
| chartIndex   | integer | path   | チャートの 0 から始まるインデックス。       |
| folder       | string  | query  | ファイルが保存されているフォルダ。          |
| storageName  | string  | query  | Aspose Cloud ストレージの名前。              |

**前提条件**: 各リクエストの `Authorization` ヘッダーには、Aspose Cloud OAuth2 フローを通じて取得した有効な JWT アクセストークンを指定する必要があります。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis)は、パブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 操作を実行できます。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。Aspose Cloud のすべてのエンドポイントは HTTPS を使用する必要があります。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Second Value Axis"
  }
}
```

**レスポンスフィールド**

- **Code** – 操作の HTTP ステータスコード（例: 成功時は `200`）。  
- **Status** – ステータスのテキスト記述（例: 成功時は `"OK"`）。  
- **Axis** – 第2値軸の詳細情報を含むオブジェクト:  
  - **AxisId** – 軸の識別子。  
  - **IsVisible** – 軸が表示されているかどうかを示すブール値。  
  - **MinimumScale** – 軸に表示される最小値。  
  - **MaximumScale** – 軸に表示される最大値。  
  - **MajorUnit** – 主目盛り間の間隔。  
  - **MinorUnit** – 従目盛り間の間隔。  
  - **Title** – 軸のタイトルテキスト。

**エラーレスポンス**（200 以外）

- `400 Bad Request` – 無効なパラメータ、または不正な形式のリクエスト。  
- `401 Unauthorized` – JWT トークンが不足している、または無効。  
- `404 Not Found` – 指定されたファイル、ワークシート、またはチャートが存在しない。  
- `500 Internal Server Error` – サーバー側で予期せぬエラーが発生。

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用することで、開発を最速で進めることが可能です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}
---