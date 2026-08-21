---
title: "Excelワークシートのチャート凡例を非表示にする – Aspose.Cells Cloud API"
type: docs
url: /ja/charts/legend/hide/
aliases: [  /ja/hide-chart-legend-in-a-worksheet/ ]
weight: 110
keywords: "Aspose.Cells, Excel, チャート凡例の非表示, REST API, クラウドSDK, チャート凡例"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシートのチャート凡例を非表示にする方法を学びます。HTTPSエンドポイント、認証要件、リクエスト構文、レスポンス詳細、エラーハンドリング、およびSDKのコード例を含みます。"
---

このREST APIは、チャートの凡例を非表示にします。**チャート凡例**とは、チャートにプロットされたデータ系列を識別するボックスです。

このAPIには、有効なAspose Cloud JWTトークンが必要であり、ワークブックはAspose Cloudストレージにアップロードされている必要があります。また、使用するAPIのバージョンは **v3.0** です。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWTトークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必須です。

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### リクエストパラメータ

| パラメータ名      | 型     | 位置   | 説明                         |
| ----------------- | ------ | ------ | ---------------------------- |
| **name**          | 文字列 | パス   | ワークブック名。             |
| **sheetName**     | 文字列 | パス   | ワークシート名。             |
| **chartIndex**    | 整数   | パス   | チャートのインデックス。     |
| **folder**        | 文字列 | クエリ | ワークブックのフォルダ（省略可）。 |
| **storageName**   | 文字列 | クエリ | ストレージ名（省略可）。     |

このパブリックにアクセス可能なプログラミングインターフェースの詳細は、[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend)をご参照ください。

cURLコマンドラインツールを使用して、APIを簡単に呼び出すことができます。以下の例では、_Sample_Test_Book.xls_ のチャート0の凡例を非表示にするリクエストを示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## レスポンス

| HTTPステータス                | 説明                                         | 例（JSON）                                                    |
| ----------------------------- | -------------------------------------------- | ------------------------------------------------------------ |
| **200 OK**                    | 凡例の非表示に成功しました。                 | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | JWTトークンが不足しているか、無効です。      | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | ワークブック、ワークシート、またはチャートが存在しません。 | `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | 予期せぬサーバーエラーが発生しました。       | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## FAQ

**Q:** _Aspose.Cells Cloud を使ってチャート凡例を非表示にするにはどうすればよいですか？_  
**A:** 有効なJWTトークンを `Authorization` ヘッダに含め、`https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` に対して `DELETE` リクエストを送信してください。`200 OK` レスポンスが返されれば成功です。

**Q:** _チャート凡例を非表示にするAPIにはどのような認証が必要ですか？_  
**A:** `Authorization: Bearer <jwt token>` ヘッダを含める必要があります。トークンは Aspose Cloud OAuth フローで取得してください。

**Q:** _チャートインデックスが無効な場合、どのようなエラーレスポンスが返されますか？_  
**A:** サービスは `404 Not Found` を返し、JSON本文に `Code: 404` と、該当するチャートが見つからない旨のメッセージを含めます。

**Q:** _HTTPSではなくHTTPを使用できますか？_  
**A:** いいえ。Aspose Cloudのすべてのエンドポイントは、セキュリティ上の理由からHTTPSが必須です。

## Cloud SDKファミリー
SDKを使用すると、開発を最速で進めることができます。SDKは低レベルの詳細を抽象化してくれるため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまなSDKを使用してAspose.CellsのWebサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**近日公開予定** – Swift SDKのコード例は、近日中に追加されます。  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Excelワークシートのチャート凡例を非表示にする – Aspose.Cells Cloud API",
  "description": "Aspose.Cells Cloud REST API を使用してExcelワークシートのチャート凡例を非表示にするステップ・バイ・ステップガイド。HTTPSエンドポイント、認証方法、リクエスト構文、レスポンス詳細、エラーハンドリング、およびSDKコード例を含みます。",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "ホーム", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Charts", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "チャート凡例の非表示", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Aspose.Cells Cloud API を使用してチャート凡例を非表示にする"
}
</script>