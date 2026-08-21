---
title: "ワークシートのプロパティを更新する – Aspose.Cells Cloud API リファレンス (v3.0)"
second_title: "ドキュメント"
linktitle: "更新"
type: docs
url: /ja/worksheets/update-properties/
aliases: [  /ja/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "worksheet",
    "update properties",
    "REST API",
    "cloud",
    "v3.0",
  ]
description: "Aspose.Cells Cloud REST API v3.0 を使用して、Excel ワークシートの基本プロパティ（例：ゼロの表示、ルーラーの表示状態）を更新する方法を学びます。cURL リクエスト、SDK サンプル、パラメーター、エラー処理を含みます。"
ArticleTitle: "ワークシートのプロパティを更新する – Aspose.Cells Cloud API リファレンス (v3.0)"
---

この REST API は、ワークシートの基本プロパティを更新します。

## REST API

**前提条件:** 有効な Aspose Cloud アカウントが必要であり、JWT アクセストークンを取得済みであること、および対象のワークブックが対応するストレージ場所に保存されている必要があります。すべてのリクエストは **HTTPS** を通じて行う必要があります。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **リクエストパラメーター**

| パラメーター名 | 型     | パス／クエリ文字列／HTTP ボディ | 説明                                                                                   |
| -------------- | ------ | ------------------------------- | -------------------------------------------------------------------------------------- |
| name           | string | path                            | ワークブックのファイル名（拡張子を含む）。                                              |
| sheetName      | string | path                            | 更新するワークシートの名前。                                                            |
| sheet          | object | body                            | ワークシートのプロパティのキー／値ペアを含む JSON オブジェクト（例：`DisplayZeros`, `IsRulerVisible`）。 |
| folder         | string | query                           | ワークブックが配置されているストレージ内のフォルダーパス。                            |
| storageName    | string | query                           | 使用するストレージの名前。                                                              |

**sheet** オブジェクトは、リクエストボディに JSON 形式で送信されます。変更可能なプロパティの例として `DisplayZeros`、`IsRulerVisible`、`IsGridlinesVisible` など、API 仕様で定義された他のプロパティがあります。

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST によるやり取りを実行できます。

cURL コマンドラインツールを使用することで、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

代表的なレスポンスコード：

- **200** – 成功。ワークシートのプロパティが更新されました。
- **400** – 不正なリクエスト（例：不正な形式の JSON、必須パラメーターの不足）。
- **401** – 認証エラー（JWT トークンが不足している、または無効です）。
- **404** – ワークブックまたはワークシートが見つかりません。
- **500** – サーバー内部エラー。

| コード | 意味 |
|------|------|
| 200 | 成功 – ワークシートのプロパティが更新されました。 |
| 400 | 不正なリクエスト – 不正な形式の JSON、または必須パラメーターの不足。 |
| 401 | 認証エラー – JWT トークンが不足している、または無効です。 |
| 404 | 見つかりません – ワークブックまたはワークシートが存在しません。 |
| 500 | サーバー内部エラー。 |

## Cloud SDK ファミリー

SDK を使用することで、開発を最速で加速できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}