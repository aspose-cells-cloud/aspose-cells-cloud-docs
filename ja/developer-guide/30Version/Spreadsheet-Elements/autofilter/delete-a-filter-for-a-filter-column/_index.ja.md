---
title: "Excelワークシートからフィルターを削除する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "フィルターの削除"
type: docs
url: /ja/delete-filter/
aliases: [  /ja/delete-a-filter-for-a-filter-column/ , /ja/delete-auto-filter/ ]
keywords: "Aspose.Cells Cloud フィルター削除, Excel, REST API, SDK"
description: "Aspose.Cells Cloud REST API、cURL、およびSDK（C#、Java、Pythonなど）を使用して、Excelワークシートのオートフィルターを削除する方法を学びます。エンドポイント、パラメーター、認証、およびサンプルコードを含みます。"
weight: 100
---

## REST API

このREST APIは、Excelワークシート上の**オートフィルター**を削除します。

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名           | 型      | 位置     | 必須? | 説明                                                                                   |
| ------------------------ | ------- | -------- | ----- | --------------------------------------------------------------------------------------- |
| **name**                 | 文字列  | パス     | はい   | ワークブック名。                                                                        |
| **sheetName**            | 文字列  | パス     | はい   | ワークシート名。                                                                        |
| **range**                | 文字列  | クエリ   | いいえ | フィルターを適用するセル範囲（例: `A1:C10`）。                                          |
| **fieldIndex**           | 整数    | クエリ   | はい   | フィルターを適用する列の0から始まるインデックス。                                       |
| **dateTimeGroupingType** | 文字列  | クエリ   | いいえ | 日時値のグループ化方法: `Day`、`Hour`、`Minute`、`Month`、`Second`、`Year`のいずれか。 |
| **year**                 | 整数    | クエリ   | いいえ | 日付グループ化用の年コンポーネント。                                                    |
| **month**                | 整数    | クエリ   | いいえ | 日付グループ化用の月コンポーネント。                                                    |
| **day**                  | 整数    | クエリ   | いいえ | 日付グループ化用の日コンポーネント。                                                    |
| **hour**                 | 整数    | クエリ   | いいえ | 日付グループ化用の時間コンポーネント。                                                  |
| **minute**               | 整数    | クエリ   | いいえ | 日付グループ化用の分コンポーネント。                                                    |
| **second**               | 整数    | クエリ   | いいえ | 日付グループ化用の秒コンポーネント。                                                    |
| **matchBlanks**          | 真偽値  | クエリ   | いいえ | `true`／`false` — 空白セルをフィルターに含めるかどうか。                               |
| **refresh**              | 真偽値  | クエリ   | いいえ | `true`／`false` — 削除後にワークシートを更新するかどうか。                             |
| **folder**               | 文字列  | クエリ   | いいえ | 元のワークブックフォルダー。                                                            |
| **storageName**          | 文字列  | クエリ   | いいえ | ストレージ名。                                                                          |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTPステータスコード**

| コード | 意味                         | 説明                                                     |
|--------|------------------------------|----------------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | パラメーターが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized（未承認）         | JWTトークンが無効または不足している。                     |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。    |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。                 |

## SDKを使用してDeleteWorksheetFilter APIを利用する方法

### DeleteWorksheetFilter APIの仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザーから直接REST APIとのやり取りを実行できるようにします。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLを使用してCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
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

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、開発を最も効率的に進められます。SDKが低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

---