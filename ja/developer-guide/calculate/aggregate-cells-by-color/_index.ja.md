---
title: "Aspose.Cells Cloud Web API – Excel の色による合計とカウント"
second_title: "ドキュメント"
ArticleTitle: "スプレッドシート／Excel で色ごとの合計、カウント、平均、最大値、最小値"
LinkTitle: "色ごとにセルを集計"
type: docs
url: /ja/aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregate, color, sum, count, average, min, max"
description: "Aspose.Cells Cloud API を使用して、Excel のセルを背景色またはフォント色で集計（合計、カウント、平均、最小値、最大値）。エンドポイント、パラメータ、認証、SDK の例を学習します。"
weight: 100
---

## 概要

この API は、セルの**色**に基づいてデータ演算を実行できます。Excel スプレッドシートにおいて、セルの塗りつぶし色またはフォント色に基づき、合計、カウント、平均、最大値、最小値を算出できます。

| 演算種別 | 説明 |
| :------- | :----------------------------------------------------------- |
| Count（カウント） | 同じ色のセルの数を算出します。 |
| Sum（合計） | 同じ色のセルの値の合計を算出します。 |
| Max Value（最大値） | 同じ色のセルの中で最も大きな値を特定します。 |
| Min Value（最小値） | 同じ色のセルの中で最も小さな値を特定します。 |
| Average Value（平均値） | 同じ色のセルの平均値を算出します。 |

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置       | 説明 |
| :----------- | :----- | :--------- | :--------------------------------------------------------------- |
| Spreadsheet  | File   | FormData   | 処理対象の Excel ワークブック。 |
| Worksheet    | String | Query      | 範囲を含むワークシート名。 |
| Range        | String | Query      | A1 形式の範囲（例: `A1:B10`）。 |
| Operation    | String | Query      | 計算方法 — `Sum`（合計）、`Count`（カウント）、`Average`（平均）、`Min`（最小値）、`Max`（最大値）。 |
| ColorPosition| String | Query      | 評価する色 — `Background`（背景色）、`Font`（フォント色）。 |
| Region       | String | Query      | スプレッドシートの地域設定（例: `us-east-1`）。 |
| Password     | String | Query      | パスワード保護されたワークブックを開くためのパスワード（オプション）。 |

#### 列挙型

- **ColorPosition**

  | 値         | 意味                     |
  | :--------- | :----------------------- |
  | Background | セルの塗りつぶし色を使用。 |
  | Font       | セルのフォント色を使用。 |

**例：multipart/form-data リクエスト**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### レスポンス

以下のスキーマはレスポンスオブジェクトを定義します。その下に具体例を示します。

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**例：レスポンス（実際の値）**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明 |
| ------ | ---------------- | ----------------------------------------------------------------- |
| 200    | OK               | フィルタが正常に適用され、レスポンスに演算詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または不正（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが不正または不足しています。 |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバーで予期しないエラーが発生しました。 |

## 色ごとの集計 API の使用例

スプレッドシートでは、異なるカテゴリのデータがしばしば色分けされています。この API を使えば、各色ごとに合計、カウント、平均、最小値、最大値を算出し、色に基づくデータ分析を簡略化できます。

## 色ごとの集計 API を使うべき理由

この API は、カスタム解析ロジックを記述することなく、高速かつ信頼性の高い色ベース演算を実行できます。Aspose.Cells Cloud SDK とシームレスに連携し、数行のコードで色による集計を実装できます。

## SDK を使用した色ごとの集計 API の利用方法

### 色ごとの集計 API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">色ごとの集計 API の仕様</a> は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行可能にします。

### Aspose.Cells Cloud SDK を使用

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速になります。短いコード片でセルの色に基づく集計演算を実行できます。  
Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示します。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**注意事項：**

- パスワード保護されたワークブックを扱う場合は、オプションの `Password` クエリパラメータを含めてください。そうでないと、401 エラーでリクエストが失敗します。
- `Spreadsheet` ファイルの最大リクエストサイズは 100 MB です。それより大きなファイルを処理する必要がある場合は、まずワークブックを Aspose Cloud ストレージにアップロードし、`Path` パラメータで参照することを検討してください（ここでは示していません）。