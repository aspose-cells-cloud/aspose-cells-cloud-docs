---
title: "Excelワークシートのズーム設定 – Aspose.Cells Cloud API v3.0"
second_title: "ドキュメント"
linktitle: "ズーム"
type: docs
url: /worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel ズーム, ワークシート ズーム, REST API, クラウド SDK, Excel 自動化"
description: "Aspose.Cells Cloud API v3.0 を使用してワークシートのズーム率（10～400 %）を設定する方法を学びます。cURL、SDK の使用例、およびエラー処理を含みます。"
weight: 20
ArticleTitle: "Excelワークシートのズーム設定 – Aspose.Cells Cloud API v3.0"
---

この REST API は、Excel ワークシートのズーム値を設定します。**認証**が必要です。すべてのリクエストの `Authorization` ヘッダーに有効な Bearer JWT トークンを含めてください。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を要求します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **リクエストパラメーター**

| パラメーター   | 型      | 位置     | 説明                                                              |
| ------------- | ------- | -------- | ----------------------------------------------------------------- |
| name          | 文字列  | パス     | Excel ファイル（ワークブック）の名前。                             |
| sheetName     | 文字列  | パス     | 変更対象のワークシートの名前。                                     |
| value         | 整数    | クエリ   | ズーム率（パーセント）。許容範囲は **10～400**（例：`40` で 40 %）。 |
| folder        | 文字列  | クエリ   | ファイルが保存されているフォルダーのパス。                         |
| storageName   | 文字列  | クエリ   | ストレージサービスの名前。                                         |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
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

**エラーレスポンス情報**  
発生する可能性のある HTTP ステータスコードは以下の通りです：

- `400 Bad Request` – パラメーターが不足しているか、無効です。
- `401 Unauthorized` – JWT トークンが不足しているか、無効です。
- `404 Not Found` – 指定されたファイルまたはワークシートが存在しません。
- `500 Internal Server Error` – サーバー側で予期せぬエラーが発生しました。

各エラーレスポンスは、`Code` と説明的な `Message` を含む JSON ボディを返します。

## クラウド SDK ファミリー
SDK を使用することは、開発を高速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリー](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}