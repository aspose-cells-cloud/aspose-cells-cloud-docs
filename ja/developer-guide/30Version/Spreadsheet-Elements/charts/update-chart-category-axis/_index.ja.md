---
title: "チャートのカテゴリ軸を更新する"
type: docs
url: /ja/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, チャート, カテゴリ軸, REST API, Excel, クラウドSDK"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のチャートのカテゴリ軸を更新します。"
ArticleTitle: "チャートのカテゴリ軸を更新する – Aspose.Cells Cloud API"
---

この REST API は、チャートのカテゴリ軸を更新します。

## PostChartCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明 |
| ------------ | ------ | ------ | ---- |
| name         | 文字列 | パス   | Excel ファイルの名前。 |
| sheetName    | 文字列 | パス   | チャートを含むワークシートの名前。 |
| chartIndex   | 整数   | パス   | 更新するチャートの 0 から始まるインデックス。 |
| axis         | オブジェクト | 本文 | カテゴリ軸のプロパティを定義する JSON オブジェクト。 |
| folder       | 文字列 | クエリ | ファイルが配置されているクラウドストレージ内のフォルダ（オプション）。 |
| storageName  | 文字列 | クエリ | ストレージの名前（オプション）。 |

**リクエストボディのスキーマ – `axis` オブジェクト**

| プロパティ | 型      | 説明 |
|-----------|---------|------|
| IsAutomaticMajorUnit | ブール値 | 主目盛り間隔を自動計算するかどうかを指定します。 |
| MajorUnit | 数値 | `IsAutomaticMajorUnit` が `false` の場合の主目盛り間隔の値。 |
| IsAutomaticMinorUnit | ブール値 | 微小目盛り間隔を自動計算するかどうかを指定します。 |
| MinorUnit | 数値 | `IsAutomaticMinorUnit` が `false` の場合の微小目盛り間隔の値。 |
| Title | オブジェクト | 軸のタイトル設定（例: `Text`, `Font`, `Visible`）。 |
| TickLabelPosition | 文字列 | 目盛りラベルの位置（例: `Low`, `High`, `NextToAxis`）。 |
| ... | ... | API 仕様で定義されたその他の軸プロパティ。 |

**HTTP ステータスコード**

| コード | 意味                     | 説明 |
|--------|--------------------------|------|
| 200    | OK（成功）               | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | 不正なリクエスト         | パラメータが不足または無効です（例: サポートされていないファイル形式）。 |
| 401    | 認証エラー               | JWT トークンが無効または不足しています。 |
| 413    | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | サーバー内部エラー       | 予期しないサーバーエラーが発生しました。 |

**前提条件 / 認証**

このエンドポイントを呼び出すには、Aspose.Cells Cloud 認証サービス (`/connect/token`) から JWT アクセストークンを取得し、以下に示す例のように `Authorization` ヘッダーにトークンを含める必要があります。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Category Axis",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**レスポンスの例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

### 注釈

* エンドポイントは HTTPS を必要とします。HTTP を使用すると、ブラウザで混合コンテンツ警告が発生する可能性があります。
* すべてのプレースホルダー値（`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`）は、実際の識別子に置き換える必要があります。
* カテゴリ軸の更新がサポートされているチャートの種類については、API リファレンスをご覧ください。

## クラウド SDK ファミリー

SDK を使用すると、開発を最も効率的に進められます。SDK は低レベルの詳細な処理を担当し、プロジェクトのタスクに集中できるようになります。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}