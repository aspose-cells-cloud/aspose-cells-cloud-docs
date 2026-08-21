---
title: "チャート領域の塗りつぶし形式を取得 – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /charts/chart-area/fill-format/get/
aliases: [/get-fill-format-of-a-chart-area-from-a-worksheet/]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Chart Area"
  - "Fill Format"
  - "REST API"
  - "Excel"
description: "Aspose.Cells Cloud API を使用して、Excelワークシート内のチャート領域の塗りつぶし形式（色、パターン、グラデーション）を取得します。cURLの例、SDKコードスニペット、認証手順、応答の詳細を含みます。"
ArticleTitle: "Get Chart Area Fill Format Aspose.Cells Cloud API v3.0"
---

この REST API は、**Chart Area**（チャート領域）の塗りつぶし形式情報を取得します。

**前提条件**  
このエンドポイントを呼び出すには、有効な OAuth/JWT アクセストークンが必要です。Aspose.Cells Cloud の認証フローを使用してトークンを取得し、`Authorization` ヘッダーに `Bearer <jwt token>` の形式で含めてください。SDK のいずれかを使用している場合は、メソッドを呼び出す前に、SDK が `client_id` および `client_secret` で正しく設定されていることを確認してください。

## GetChartAreaFillFormat API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                           |
|------------|------|------|------------------------------|
| name       | string | path | ワークブック名。                  |
| sheetName  | string | path | ワークシート名。                  |
| chartIndex | integer | path | チャートのインデックス。            |
| folder     | string | query | ワークブックが格納されているフォルダ。 |
| storageName | string | query | ストレージ名。                   |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) は、パブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスにアクセスできます。以下は、cURL を使用して API を呼び出す例です。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**注意事項**  
- 成功した呼び出しは HTTP 200 と塗りつぶし形式の詳細情報を返します。  
- HTTP 401 は認証失敗（無効または不足しているトークン）を示します。  
- 指定されたワークブック、ワークシート、またはチャートインデックスが存在しない場合、HTTP 404 が返されます。  
- HTTP 500 はサーバーサイドエラーを示します。問題が続く場合はリクエストを再試行するか、サポートにお問い合わせください。

| コード | 意味                                                  |
|------|-----------------------------------------------------|
| 200  | 成功 – 塗りつぶし形式が返されました                      |
| 401  | 認証エラー – 無効または不足しているトークン               |
| 404  | 見つかりません – ワークブック、ワークシート、またはチャートが見つかりません |
| 500  | サーバーエラー                                      |

関連する操作については、**Get Chart Area Border** および **Get Chart Title** エンドポイントを参照してください。

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}