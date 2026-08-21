---
title: "Excelワークシート内の複数行を自動調整する"
second_title: "Document"
linktitle: "Rows"
type: docs
url: /ja/worksheets/autofit/rows/
aliases: [  /ja/autofit-multiple-rows-of-worksheet/ ]
keywords: "行の自動調整、Excel、Aspose.Cells Cloud、REST API、ワークシート、スプレッドシート"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内の複数行を自動調整する方法を学びます。リクエスト構文、パラメーター、cURL の例、SDK スニペット、エラー処理を含みます。"
weight: 40
ArticleTitle: "Excelワークシート内の複数行を自動調整する – Aspose.Cells Cloud API ドキュメント"
---

この REST API は、Excel ワークシート内の行の高さを自動的に調整します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **リクエストパラメーター**

| パラメーター名        | 型      | 位置   | 説明                                                                                                                          | 必須   |
| --------------------- | ------- | ------ | ---------------------------------------------------------------------------------------------------------------------------- | ------ |
| **name**              | 文字列  | パス   | Excel ファイルの名前。                                                                                                        | ✔      |
| **sheetName**         | 文字列  | パス   | ワークシートの名前。                                                                                                          | ✔      |
| **autoFitterOptions** | オブジェクト | 本文   | 行の自動調整方法を制御するオプション（例：非表示行を無視）。下記のフィールド説明を参照。                                        | ✖      |
| **startRow**          | 整数    | クエリ | 自動調整を開始する最初の行（1 から始まるインデックス）。                                                                      | ✔      |
| **endRow**            | 整数    | クエリ | 自動調整を終了する最後の行（inclusive）。                                                                                     | ✔      |
| **onlyAuto**          | 真偽値  | クエリ | `true` の場合、API は Excel によって自動的に計算された高さの行のみを調整します。`false` の場合、完全な自動調整が実行されます。 | ✖      |
| **folder**            | 文字列  | クエリ | ドキュメントを含むフォルダー。                                                                                                | ✖      |
| **storageName**       | 文字列  | クエリ | ストレージサービスの名前。                                                                                                    | ✖      |

**autoFitterOptions** のフィールド（すべて任意）：

- `AutoFitMergedCells` _(真偽値)_ – `true` の場合、行の高さを計算する際に結合セルが考慮されます。
- `IgnoreHidden` _(真偽値)_ – `true` の場合、自動調整中に非表示行が無視されます。
- `OnlyAuto` _(真偽値)_ – クエリパラメーター `onlyAuto` と同様の動作をします。設定された場合、クエリ値を上書きします。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) は公開可能なプログラミングインタフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

一般的なエラーレスポンスは以下の通りです：

- **400 Bad Request** – 無効なパラメータ値または不正な JSON ボディ。
- **401 Unauthorized** – JWT トークンが不足しているか無効。
- **404 Not Found** – 指定されたファイルまたはワークシートが存在しません。
- **500 Internal Server Error** – 予期せぬサーバーエラーが発生しました。

**HTTP ステータスコード**

| コード | 意味                         | 説明                                           |
|------|-----------------------------|------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメーターが不足しているか無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期せぬサーバーエラーが発生しました。 |

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー
SDK を使用すると、開発が最速になります。SDK が低レベルの詳細を処理するため、プロジェクトに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---